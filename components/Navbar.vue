<template>
  <nav class="navbar ">
    <div class="navbar-brand">
      <a class="navbar-item" href="http://bulma.io">
        <img src="https://jobs.github.com/images/layout/logo.png" alt="logo" width="112" height="28">
      </a>

      <a class="navbar-item is-hidden-desktop" href="https://github.com/jgthms/bulma" target="_blank">
      <span class="icon" style="color: #333;">
        <i class="fa fa-github"></i>
      </span>
      </a>

      <a class="navbar-item is-hidden-desktop" href="https://twitter.com/jgthms" target="_blank">
      <span class="icon" style="color: #55acee;">
        <i class="fa fa-twitter"></i>
      </span>
      </a>

      <div class="navbar-burger burger" data-target="navMenubd-example">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </nav>
</template>
<script>
  export default{
    name: 'navbar'
  };
</script>
<style scoped>
  .navbar {
    background-color: #2B7FC3;
    color: #c9e2f1;
  }
</style>
