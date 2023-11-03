<template>
  <Transition>
    <div
      :aria-label="label"
      class="tabs__content"
      :id="id"
      role="tabpanel"
      :hidden="!active"
      tabindex="0"
      v-show="active"
    >
      <slot />
    </div>
  </Transition>
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
    display: block !important;
  }
}

.v-enter-active,
.v-leave-active {
  transition: all 0.5s ease;
}
.v-enter-from,
.v-leave-to {
  opacity: 0;
}
.v-enter-from {
  translate: 2rem 0;
}
</style>
