<template>
  <nav>
    <router-link to="/">
        <img :src="logo" :alt="alt" id="logo">
    </router-link>
    <router-link to="/">Home</router-link> |
    <router-link to="/pedidos">Pedidos</router-link>
  </nav>
</template>
<script>
export default {
    name: "Navbar",
    props: ["logo", "alt"]
};
</script>
<style scoped>
    nav {
        background-color: #222;
        border-bottom: 4px solid #111;
        padding: 15px 50px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }
</style>