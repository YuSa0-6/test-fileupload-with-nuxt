<template>
  <div>
    <h1>Get file</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">{{ post.title }}</li>
    </ul>
  </div>
</template>

<script setup>
const { data: posts } = await useFetch(
  'https://jsonplaceholder.typicode.com/posts/'
);
</script>