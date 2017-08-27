<template>
  <div class="container is-fluid">
    <Spinner v-if="showLoader"></Spinner>
    <div class="box" v-if="!showLoader" v-for="job in jobsList" v-bind:key="job.id">
      <article class="media">
        <div class="media-left">
          <figure class="image is-64x64">
            <img :src="job.company_logo" alt="logo">
          </figure>
        </div>
        <div class="media-content">
          <div class="content">
              <h4>
                {{job.title}}
                <span class="media-right is-pulled-right tag is-dark">{{job.type}}</span>
              </h4>
            <!--<p v-html="job.description"></p>-->
            <p class="location"><i class="fa fa-map-marker"></i> {{job.location}}</p>
          </div>
          <nav class="level is-mobile">
            <div class="level-left">
              <a :href="job.url" target="_blank">View more...</a>
            </div>
          </nav>
        </div>
      </article>
    </div>
  </div>
</template>

<script>
  import axios from 'axios';
  import Spinner from './Spinner.vue'
  export default {
    name: 'jobslist',
    components: {
      Spinner
    },
    props:['description', 'location'],
    data() {
      return {
          jobsList: [],
          showLoader: true
      }
    },
    methods: {
        fetchJobs() {
          this.showLoader = true;
          axios.get(`https://jobs.github.com/positions.json?description=${this.description}&location=${this.location}`).then(function(response) {
            this.showLoader = false;
            this.jobsList = response.data;
          }.bind(this));
        }
    },
    mounted() {
      this.fetchJobs();
    },
    watch: {
        description: function(val) {
            this.description = val;
            this.fetchJobs();
        },
        location: function(val) {
            this.location = val;
            this.fetchJobs();
        }
    }
  };
</script>
<style scoped>
  .image img {
    width: 64px;
    height: 64px;
  }
  .location i {
    line-height: 24px;
  }
</style>
