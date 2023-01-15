<script type="ts">
import { computed } from 'vue'

export default {
  props: {
    initialTab: String
  },
  data() {
    return {
      currentTab: null,
    };
  },
  provide() {
    return {
      selectTab: this.selectTab,
      currentTab: computed(() => this.currentTab || this.initialTab)
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
