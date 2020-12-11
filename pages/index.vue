<template>
  <div class="home-container">
    <h1 class="welcome">Welcome to the best spot for Recipes</h1>
    <nuxt-link class="call-to-action" to="/recipes"
      >Click here to see recipes</nuxt-link
    >
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home"
    };
  }
};
</script>

<style>
body {
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
}
.welcome {
  margin-top: 30px;
  font-size: 50px;
  width: fit-content;
  color: black;
}
.call-to-action {
  color: white;
  background: #183585;
  text-decoration: none;
  padding: 10px;
  border-radius: 5px;
  font-size: 20px;
  width: fit-content;
  border: 2px solid white;
  margin-top: 5%;
  transition: 0.3s;
}
.call-to-action:hover {
  color: white;
  background: green;
}
.home-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding-top: 10%;
  align-items: center;
}
</style>
