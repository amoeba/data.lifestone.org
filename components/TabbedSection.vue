<script type="ts">
import { computed } from 'vue'

export default {
  data() {
    return {
      currentTab: "changeme",
    };
  },
  provide() {
    return {
      selectTab: this.selectTab,
      currentTab: computed(() => this.currentTab)
    }
  },
  methods: {
    selectTab(event) {
      this.currentTab = event;
    }
  }
}
</script>

<template>
  <div class="tabbed-section">
    <Tabs>
      <slot name="tabs">
        No tabs provided
      </slot>
    </Tabs>
    <TabContents>
      <slot name="content">
        No content provided
      </slot>
    </TabContents>
  </div>
</template>
