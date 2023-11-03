<template>
  <li class="card">
    <div class="card__ribbon" v-if="logo">
      <img :src="logo" alt="Logo" class="card__logo" />
    </div>
    <div class="card__content">
      <header class="card__title">{{ title }}</header>
      <slot />
    </div>
  </li>
</template>

<script setup>
defineProps({
  title: String,
  logo: String,
});
</script>

<style>
.card p {
  margin: 0;
}

.card a {
  color: var(--accent);
}
</style>

<style lang="scss" scoped>
.card {
  --accent: var(--purple);
  display: grid;
  gap: 1rem;
  background: var(--accent);
  box-shadow: inset 0 0 0 999rem rgba(255, 255, 255, 0.8),
    inset 0 0 0 999rem rgba(127, 127, 127, 0.6);
  color: black;
  padding: 1rem;
  border-radius: 0.5rem;
  margin: 3rem 0;
  grid-template-columns: auto 1fr;
  min-height: 6rem;

  @media print {
    page-break-inside: avoid;
  }

  &:hover {
    .card__ribbon {
      box-shadow: 0 0 1rem rgba(0, 0, 0, 0.6);
      margin: -2rem 0.2rem -2rem -0.7rem;
      width: 8.5rem;

      &::before,
      &::after {
        scale: 1;
      }
    }

    .card__logo {
      width: 5.5rem;
    }
  }

  &__ribbon {
    width: 8rem;
    background: var(--accent);
    margin: -1.4rem 0;
    position: relative;
    display: grid;
    justify-items: center;
    align-items: center;
    transition: 0.2s ease;

    @media (max-width: 500px) {
      display: none;
    }

    &::before,
    &::after {
      @media screen {
        content: "";
      }
      width: 0;
      height: 0;
      border-style: solid;
      position: absolute;
      filter: brightness(60%);
      scale: 0.4;
      transition: 0.2s ease;
    }
    &::before {
      border-width: 1rem 0 0 1rem;
      border-color: transparent transparent transparent var(--accent);
      left: 100%;
      top: 0;
      transform-origin: 0 0;
    }
    &::after {
      border-width: 1rem 1rem 0 0;
      border-color: var(--accent) transparent transparent transparent;
      left: 100%;
      bottom: 0;
      transform-origin: 0 100%;
    }
  }

  &__logo {
    padding: 0.5rem;
    background: white;
    margin: 1rem;
    width: 5rem;
    transition: 0.2s ease;
    aspect-ratio: 1 / 1;
    object-fit: contain;
  }

  &__title {
    font-weight: 600;
    font-size: 1.2rem;
    color: var(--accent);
  }

  &__content {
    gap: 1rem;
    display: grid;
  }
}
</style>
