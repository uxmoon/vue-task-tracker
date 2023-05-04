<template>
  <footer>
    <p>Copyright &copy; 2023</p>
    <!-- <a href="/about">About</a> -->
    <router-link to="/about">About</router-link>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style>
footer {
  text-align: center;
  margin-top: 2rem;
}
a {
  color: #333;
}
</style>
