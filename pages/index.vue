<template>
  <section class="container is-fluid">
    <Navbar></Navbar>
    <Search @jobSearch="inputSearch"></Search>
    <JobsList v-bind:description="description" v-bind:location="location"></JobsList>
  </section>
</template>

<script>

import Navbar from '~/components/Navbar';
import Search from '~/components/Search';
import JobsList from '~/components/JobsList';
export default {
  components: {
    Navbar,
    Search,
    JobsList
  },
  data() {
      return {
          description: '',
          location: '',
          fullTime: ''
      }
  },
  methods: {
      inputSearch(value) {
          this.description = value.description;
          this.location = value.location;
          this.fullTime = value.fullTime;
      }
  }
};
</script>

<style>
  a {
    color: #2B7FC3;
  }
  .button.is-primary {
    background-color: #2B7FC3;
  }
</style>
