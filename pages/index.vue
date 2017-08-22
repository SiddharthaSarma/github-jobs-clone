<template>
  <section class="container is-fluid">
    <Navbar></Navbar>
    <Search></Search>
    <JobsList></JobsList>
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
  }
};
</script>

<style>

</style>
