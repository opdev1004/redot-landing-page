<script setup lang="ts">
const { small } = defineProps<{
  small?: boolean;
}>();

const classSmall = computed(() => small ? "section-title--small" : "");
</script>

<template>
  <div :class="classSmall" class="section-title">
    <slot />
  </div>
</template>

<style scoped lang="scss">
.section-title {
  font-weight: 800;
  font-size: 32px;

  &--small {
    font-size: 24px;
  }
}
</style>
