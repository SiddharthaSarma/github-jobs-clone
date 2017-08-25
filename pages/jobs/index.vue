<template>
  <div class="user">
    <h3>{{ name }}</h3>
    <h4>@{{ username }}</h4>
    <p>Email : {{ email }}</p>
  </div>
</template>

<script>
  import axios from 'axios';

  export default {

//    async asyncData ({ params, error }) {
//      try {
//        const { data } = await axios.get(`https://jobs.github.com/positions/87461912-8741-11e7-9123-2e5a5789abc2.json`);
//        return data
//      } catch (e) {
//        error({ message: 'Job not found', statusCode: 404 })
//      }
//    }

    created() {
      axios.get(`https://jobs.github.com/positions/87461912-8741-11e7-9123-2e5a5789abc2.json`).then(function(response) {
          console.log(response);
      })
    }
  }
</script>

<style scoped>
  .user {
    text-align: center;
    margin-top: 100px;
    font-family: sans-serif;
  }
</style>
