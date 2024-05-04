<script setup lang="ts">

defineProps<{
  msg: string
}>();
// const pageTitle = ref('Hello World!');

// // 當組件掛載時設置標題
// onMounted(() => {
//   document.title = pageTitle.value;
// });

// // 監聽 pageTitle 的變化，並更新標題
// watch(pageTitle, (newTitle) => {
//   document.title = newTitle;
// });
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>. What's next?
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>onMounted, , watch
