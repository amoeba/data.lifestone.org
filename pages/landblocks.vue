<script type="js" setup>
const url = 'https://dungeonmapsdb.treestats.net/dungeonmaps/dungeons.json';
const { data: landblocks } = await useFetch(url)
</script>

<template>
  <h2>Landblocks</h2>
  <p>Just testing data fetch using <code>useFetch</code></p>
  <p>Fetch a sample of landblocks from <a href="{{ url }}">{{ url }}</a></p>
  <ul>
    <li v-for="landblock in landblocks['rows']" :v-key="landblock[0]">{{ landblock[2] }}</li>
  </ul>
  <NuxtLink to="/">↩ Go Home</NuxtLink>
</template>
