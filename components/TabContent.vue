<script type="ts">
export default {
  props: {
    id: String
  },
  inject: ['currentTab'],
  computed: {
    isVisible() {
      // FIXME: This will break in future Vue versions
      return this.id === this.currentTab.value
    }
  }
}
</script>

<template>
  <div v-show="isVisible" class="tab-content">
    <slot></slot>
  </div>
</template>
