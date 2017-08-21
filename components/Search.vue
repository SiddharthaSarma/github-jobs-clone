<template>
  <div class="container is-fluid">
    <form>
      <div class="columns">
        <div class="column field">
          <label class="label">Name</label>
          <div class="control">
            <input class="input" type="text" placeholder="e.g Alex Smith">
          </div>
        </div>
        <div class=" column">
          <label class="label">Email</label>
          <div class="control">
            <input class="input" type="email" placeholder="e.g. alexsmith@gmail.com">
          </div>
        </div>
        <div class="column is-2">
          <label class="checkbox">
            <input type="checkbox">
            Remember me
          </label>
        </div>
        <div class="column is-2">
          <button class="button is-primary" type="submit">Search</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'search'
  };
</script>

<style>

</style>
