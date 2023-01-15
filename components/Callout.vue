<template>
  <div class="callout">
    <div class="callout-left">
      <slot>
        <!-- https://phosphoricons.com/ -->
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="#ffffff" viewBox="0 0 256 256">
          <rect width="256" height="256" fill="none"></rect>
          <circle cx="128" cy="128" r="96" fill="none" stroke="#ffffff" stroke-linecap="round" stroke-linejoin="round"
            stroke-width="16"></circle>
          <polyline points="120 120 128 120 128 176 136 176" fill="none" stroke="#ffffff" stroke-linecap="round"
            stroke-linejoin="round" stroke-width="16"></polyline>
          <circle cx="126" cy="84" r="12"></circle>
        </svg>
      </slot>
    </div>
    <div class="callout-content">
      <slot name="content"></slot>
    </div>
  </div>
</template>
