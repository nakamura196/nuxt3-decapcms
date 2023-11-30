<script setup lang="ts">


const items = [
  {
    title: "Blog (Nuxt Content and Netlify CMS)",
    to: "blog"
  },
];

useHead({
  script: [
    { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
  ],
});
</script>
<template>
  <v-container>
    <v-list>
      <v-list-item class="mb-2" v-for="(item, key) in items" :key="key">
        
          <NuxtLink :to="item.to">
            {{ item.title }}
          </NuxtLink>
      </v-list-item>
    </v-list>
  </v-container>
</template>
