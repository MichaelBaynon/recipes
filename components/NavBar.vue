<template lang="">
  <div class="nav-bar">
    <nuxt-link to="/">Home</nuxt-link>
    <nuxt-link to="/recipes">Recipes</nuxt-link>
    <nuxt-link to="/about">About</nuxt-link>
  </div>
</template>
<script>
export default {};
</script>
<style>
.nav-bar {
  width: 100%;
  margin: 0;
  padding: 3px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-bottom: 1px solid lightgrey;
  background: #e3e3e3;
}

.nav-bar a {
  display: flex;

  margin: 10px 15px;
  justify-content: center;
  align-items: center;
  align-content: center;
  border-radius: 5px;
  transition: 0.3s;
}

.nav-bar a:hover {
  color: #0091eb;
}
</style>
