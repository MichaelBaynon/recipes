<template>
  <div class="about">
    <p>Site was made using Vue/Nuxt</p>
    Site was made and maintained by
    <a href="https://github.com/MichaelBaynon" target="_">Michael Baynon</a>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "About"
    };
  }
};
</script>

<style>
.about {
  font-size: 25px;
  margin: 0 auto;
  width: fit-content;
  margin-top: 22%;
}
.about p {
  color: #6c4685;
  margin-bottom: 30px;
}
.about a:hover {
  color: purple;
}
</style>
