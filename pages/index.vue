<template>
  <section class="container is-fluid">
    <Search></Search>
    <JobsList></JobsList>
  </section>
</template>

<script>
import Search from '~/components/Search';
import JobsList from '~/components/JobsList';

export default {
  components: {
    Search,
    JobsList
  }
};
</script>

<style>

</style>
