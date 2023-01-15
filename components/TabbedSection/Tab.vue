<script type="ts">
export default {
  props: {
    id: String
  },
  inject: ['currentTab', 'selectTab'],
  computed: {
    isSelected() {
      // FIXME: This will break in future Vue versions
      return this.id === this.currentTab.value
    }
  }
}
</script>

<template>
  <div class="tab" :class="{ selected: isSelected }">
    <button @click="selectTab(id)">
      <slot></slot>
    </button>
  </div>
</template>
