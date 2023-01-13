<template>
  <div class="section">
    <div class="section-head">
      <slot name="head">Section head fallback</slot>
    </div>
    <div class="section-body">
      <slot>Section body fallback</slot>
    </div>
    <div class="section-foot">
      <slot name="foot">Section foot fallback</slot>
    </div>
  </div>
</template>
