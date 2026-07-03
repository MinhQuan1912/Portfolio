<template>
   <component :is="tag" ref="target" :class="[baseClass, { 'is-visible': isVisible }]"
      :style="delay ? { transitionDelay: `${delay}ms` } : {}">
      <slot />
   </component>
</template>

<script setup lang="ts">
const props = defineProps({
   tag: { type: String, default: 'section' },   
   effect: { type: String, default: 'fade-up' },    
   delay: { type: Number, default: 0 },             
   threshold: { type: Number, default: 0.15 },      
})

const target = ref(null)
const isVisible = ref(false)

const baseClass = computed(() => `reveal reveal-${props.effect}`)

const { stop } = useIntersectionObserver(
   target,
   ([entry]) => {
      if (entry?.isIntersecting) {
         isVisible.value = true
         stop()
      }
   },
   { threshold: props.threshold }
)
</script>

<style scoped>
.reveal {
   opacity: 0;
   transition: opacity 0.8s ease, transform 0.8s ease;
   will-change: opacity, transform;
}

.reveal.is-visible {
   opacity: 1;
   transform: translate(0, 0) !important;
}

.reveal-fade-up {
   transform: translateY(40px);
}

.reveal-fade-in {
   transform: translateY(0);
}

.reveal-fade-left {
   transform: translateX(-40px);
}

.reveal-fade-right {
   transform: translateX(40px);
}
</style>