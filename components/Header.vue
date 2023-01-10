<template>
  <header>
    <div class="header-top">
      <div class="header-left">
        <Icon />
        <h1>
          <NuxtLink to="/">data</NuxtLink>
          <NuxtLink to="/">.lifestoned.org</NuxtLink>
        </h1>
      </div>
      <div class="header-right">
        <div class="search-container">
          <input class="search" type="text" placeholder="Search" />
        </div>
      </div>
    </div>
    <Nav />
  </header>
</template>
