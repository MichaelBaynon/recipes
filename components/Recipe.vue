<template lang="">
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div
        class="thumbnail"
        :style="{
          backgroundImage: 'url(' + thumbnail + ' )'
        }"
      ></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>
<script>
export default {
  props: ["thumbnail", "title", "previewText", "id"]
};
</script>
<style>
a {
  text-decoration: none;
  color: black;
}

.thumbnail {
  transition: 0.3s;
  opacity: 85%;
}
.thumbnail:hover {
  opacity: 100%;
}
</style>
