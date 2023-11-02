<template>
  <div class="tabs">
    <ul class="tabs__tabs">
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'essentials' }"
        @click="activeTab = 'essentials'"
      >
        Essentials
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'tools' }"
        @click="activeTab = 'tools'"
      >
        Tools and technologies
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'beyond' }"
        @click="activeTab = 'beyond'"
      >
        Beyond the desk
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'contact' }"
        @click="activeTab = 'contact'"
      >
        Contact me
      </li>
    </ul>
    <div class="tabs__contents">
      <div class="tabs__content" v-show="activeTab === 'essentials'">
        <h2>Essentials</h2>
      </div>
      <div class="tabs__content" v-show="activeTab === 'tools'">
        <h2>Tools and technologies</h2>
      </div>
      <div class="tabs__content" v-show="activeTab === 'beyond'">
        <h2>Beyond the desk</h2>
      </div>
      <div class="tabs__content" v-show="activeTab === 'contact'">
        <h2>Contact me</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
const activeTab = ref("essentials");
</script>

<style lang="scss" scoped>
.tabs {
  &__tabs {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    border-bottom: 1px solid var(--purple);
  }
  &__tab {
    padding: 0.5rem 1rem;
    font-weight: bold;
    font-size: 1.2rem;
    cursor: pointer;
    background: linear-gradient(to bottom, transparent, transparent);

    &--active {
      background: linear-gradient(45deg, var(--yellow), var(--orange));
      color: black;
    }

    &:not(&--active):hover {
      background: linear-gradient(to bottom, transparent, var(--purple));
    }
  }
}
</style>
