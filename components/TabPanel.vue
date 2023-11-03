<template>
  <div
    :aria-label="label"
    class="tabs__content"
    :id="id"
    role="tabpanel"
    :hidden="!active"
    tabindex="0"
  >
    <slot />
  </div>
</template>

<script setup>
const props = defineProps({
  active: Boolean,
  label: String,
  id: String,
});
</script>

<style lang="scss">
@media print {
  .tabs__content[hidden] {
    display: block;
  }
}
</style>
