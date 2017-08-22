<template>
  <div class="container is-fluid">
    <form>
      <div class="columns">
        <div class="column field">
          <label class="label">Job description</label>
          <div class="control">
            <input class="input" type="text" placeholder="Filter by title, benefits, companies, expertise">
          </div>
        </div>
        <div class=" column">
          <label class="label">Location</label>
          <div class="control">
            <input class="input" type="text" placeholder="Filter by city, state, zip code or country">
          </div>
        </div>
        <div class="column is-2 checkbox-container">
          <label class="checkbox">
            <input type="checkbox">
            Remember me
          </label>
        </div>
        <div class="column is-2 submit-container">
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

<style scoped>
.submit-container {
  display: flex;
  align-items: center;
  -webkit-align-items: center;
}
  .checkbox-container label{
    line-height: 104px;
  }
</style>
