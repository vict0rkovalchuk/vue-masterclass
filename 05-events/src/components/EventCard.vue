<template>
  <SectionedCard>
    <template #header>
      {{ title }}
    </template>
    {{ when }}
    <template #footer>
      <div class="space-y-4">
        <p>{{ description }}</p>
        <div class="flex justify-end">
          <BaseButton @click="$emit('register')">
            Register
          </BaseButton>
        </div>
      </div>
    </template>
  </SectionedCard>
</template>

<script setup>
import BaseButton from './BaseButton.vue';
import SectionedCard from './SectionedCard.vue';

  defineProps({
    title: {
      type: String,
      required: true,
      default: ''
    },
    when: {
      type: String,
      required: true,
      default: ''
    },
    description: {
      type: String,
      required: true,
      default: ''
    },
  });
  defineEmits(['register']);
</script>