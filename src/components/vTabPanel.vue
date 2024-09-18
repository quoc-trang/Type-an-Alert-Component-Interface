<script setup lang="ts">
import { inject, computed } from "vue";
import { injectionKey } from "./vTabs.vue";

const props = defineProps<{
  title: string;
}>();

const tabsProvider = inject(injectionKey);

if (!tabsProvider) {
  throw new Error("vTab must be used within a vTabs component");
}

tabsProvider.registerTab(props.title);

if (!tabsProvider.activeTab.value) {
  tabsProvider.activateTab(props.title);
}

const isActive = computed(() => tabsProvider.activeTab.value === props.title);
</script>
<template>
  <div class="tab-content" v-show="isActive">
    <slot></slot>
  </div>
</template>
