<template>
  <div class="tabs">
    <div
      class="tabs__tabs"
      role="tablist"
      aria-label="Tabs"
      @keydown.left="selectPreviousTab"
      @keydown.right="selectNextTab"
    >
      <button
        v-for="(tab, index) in tabs"
        :key="index"
        role="tab"
        class="tabs__tab"
        :aria-selected="activeTab === tab.id"
        :aria-controls="tab.id"
        @click="activeTab = tab.id"
        :tabindex="activeTab === tab.id ? 0 : -1"
        ref="tabsRefs"
      >
        {{ tab.label }}
      </button>
    </div>

    <div class="tabs__contents">
      <TabPanel
        label="Essentials"
        id="essentials"
        :active="activeTab === 'essentials'"
      >
        <TabEssentials @select-tab="activeTab = $event" />
      </TabPanel>

      <TabPanel
        label="Tools and technologies"
        id="tools"
        :active="activeTab === 'tools'"
      >
        <TabTools />
      </TabPanel>

      <TabPanel
        label="Other interests"
        id="beyond"
        :active="activeTab === 'beyond'"
      >
        <TabBeyond />
      </TabPanel>

      <TabPanel
        label="Contact me"
        id="contact"
        :active="activeTab === 'contact'"
      >
        <TabForm />
      </TabPanel>
    </div>
  </div>
</template>

<script setup>
const activeTab = ref("essentials");
const tabs = [
  { id: "essentials", label: "Essentials" },
  { id: "tools", label: "Tools and technologies" },
  { id: "beyond", label: "Beyond the desk" },
  { id: "contact", label: "Contact me" },
];
const tabsRefs = ref([]);

/**
 * Get the index of the currently selected tab
 *
 * @return  {number}
 */
function getCurrentTabIndex() {
  return tabs.findIndex((tab) => tab.id === activeTab.value);
}

/**
 * Focus on the currently selected tab
 *
 * @return  {void}
 */
function selectCurrentTab() {
  tabsRefs.value[getCurrentTabIndex()].focus();
}

/**
 * Focus on the previous tab
 *
 * @return  {void}
 */
function selectPreviousTab() {
  activeTab.value =
    tabs[getCurrentTabIndex() - 1]?.id || tabs[tabs.length - 1].id;
  selectCurrentTab();
}

/**
 * Focus on the next tab
 *
 * @return  {void}
 */
function selectNextTab() {
  activeTab.value = tabs[getCurrentTabIndex() + 1]?.id || tabs[0].id;
  selectCurrentTab();
}
</script>

<style lang="scss" scoped>
.tabs {
  &__tabs {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 1px solid var(--purple);

    @media print {
      display: none;
    }
  }

  &__tab {
    padding: 0.5rem 1rem;
    font: inherit;
    font-weight: bold;
    cursor: pointer;
    background: linear-gradient(to bottom, transparent, transparent);
    text-decoration: none;
    border: 0;

    &[aria-selected="true"] {
      background: linear-gradient(45deg, var(--yellow), var(--orange));
      color: black;
    }

    &:not(&[aria-selected="true"]):hover {
      background: linear-gradient(to bottom, transparent, var(--purple));
    }
  }
}
</style>

<style>
.cards {
  padding: 0;
  margin: 0;
  list-style: none;
}
</style>
