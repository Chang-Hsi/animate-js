<script setup>
import { ref, onMounted } from 'vue'
import { animate } from 'animejs'
import { useCounterStore } from '../stores/counter'

const counter = useCounterStore()
const box = ref(null)

onMounted(() => {
  if (!box.value) return

  animate(box.value, {
    x: ['0rem', '12rem', '0rem'],
    rotate: '1turn',
    scale: [1, 1.15, 1],
    duration: 1800,
    ease: 'inOut(3)',
  })
})
</script>

<template>
  <section class="space-y-6">
    <h1 class="text-3xl font-bold text-slate-900">Vue 3 + Vite Setup</h1>

    <div class="rounded-xl border border-slate-200 bg-white p-4 shadow-sm">
      <p class="text-slate-700">Pinia count: <strong>{{ counter.count }}</strong></p>
      <p class="text-slate-500">Doubled: {{ counter.doubled }}</p>
      <button
        class="mt-3 rounded-md bg-slate-900 px-4 py-2 text-sm font-semibold text-white hover:bg-slate-700"
        @click="counter.increment"
      >
        Increment
      </button>
    </div>

    <div class="space-y-3">
      <p class="text-sm text-slate-600">animejs demo:</p>
      <div ref="box" class="h-14 w-14 rounded-lg bg-emerald-500" />
    </div>
  </section>
</template>
