<!-- three-cols-mine.vue -->
<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
})
</script>

<template>
  <div class="slidev-layout w-full h-full" :class="props.layoutClass">
    <slot />
    <div class="grid grid-cols-3 gap-4">
      <div class="col-left" :class="props.class">
        <slot name="left" />
      </div>
      <div class="col-middle" :class="props.class">
        <slot name="middle" />
      </div>
      <div class="col-right" :class="props.class">
        <slot name="right" />
      </div>
    </div>
  </div>
</template>

