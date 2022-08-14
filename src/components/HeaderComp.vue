<script>
export default {
  data() {
    return {
      h1: "jojoca",
    };
  },
};
</script>

<template>
  <header>
    <router-link to="/">
      <h1>{{ h1 }}</h1>
    </router-link>
  </header>
</template>
<style>
header {
  background-color: rgb(58, 160, 185);
  width: 100%;
  height: 4em;
}
a {
  text-decoration: none;
}
h1 {
  font-size: 2.5rem;
  display: flex;
  justify-content: center;
  color: white;
}
</style>
