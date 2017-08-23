<template>
  <div class="container is-fluid">
    <form v-on:submit.prevent="getJobs">
      <div class="columns">
        <div class="column field">
          <label class="label">Job description</label>
          <div class="control">
            <input class="input" v-model="description" type="text" placeholder="Filter by title, benefits, companies, expertise">
          </div>
        </div>
        <div class=" column">
          <label class="label">Location</label>
          <div class="control">
            <input class="input" v-model="location" type="text" placeholder="Filter by city, state, zip code or country">
          </div>
        </div>
        <div class="column is-2 checkbox-container has-text-centered">
          <label class="checkbox">
            <input type="checkbox" v-model="fullTime">
            Full time only
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
    name: 'search',
    data() {
        return {
            description: '',
          location: '',
          fullTime: false
        }
    },
    methods: {
      getJobs () {
        let input = {
            description: this.description,
            location: this.location,
            fullTime: this.fullTime
        }
        this.$emit('jobSearch', input);
      }
    }
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
