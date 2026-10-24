<template>
  <SectionedCard>
    <div class="flex justify-between items-center">
      <div>Booking to Vue Conference</div>
      <BaseButton variant="danger" @click="$emit('register')">
        Cancel
      </BaseButton>
    </div>
  </SectionedCard>
</template>

<script setup>
import SectionedCard from './SectionedCard.vue';
import BaseButton from './BaseButton.vue';
  
defineEmits(['register']);
</script>