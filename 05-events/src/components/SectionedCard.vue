<template>
  <BaseCard>
    <h3 v-if="$slots.header" class="p-4 font-medium text-xl border-b border-gray-200">
      <slot name="header" />
    </h3>
    <div 
      v-if="$slots.default" 
      :class="{ 'p-4': true, 'border-b border-gray-200': $slots.footer }"
    >
      <slot />
    </div>
    <div v-if="$slots.footer" class="p-4">
      <slot name="footer" />
    </div>
  </BaseCard>
</template>

<script setup>
import BaseCard from './BaseCard.vue';
</script>