<template>
  <div>
    <h1 class="display-4" align="center">Sci - Tings</h1>
		<p class="lead" align="center">An open-source, collaborative data science laboratory aimed at expanding <em>access</em> to data and information.</p>
		<hr class="my-4">
    <b-container>
      <b-card-group class="card-group" deck>
        <home-card header="Open Source">At Sci-Tings we aim to make data accessible and transparent. This includes auditing the veracity of data sets. The end goal is for users to justify their data workflows and conclusions.</home-card>
        <home-card header="Collaborative Data Workflows">All data analyses are free to use and shareable with the public. Additionally, users can seek help when trying to analyze data and creating data visualizations in order to foster an open discussion.</home-card>
        <home-card header="Guided Data Science Pipelines">Get started by uploading a data set and we'll help you get started with your data analyses. Learn to analyze data from start to finish.</home-card>
      </b-card-group>
      <div class="row justify-content-center">
        <home-card header="Welcome to Sci-Tings" title="Start exploring data sets today....">
          <b-button href="explore" variant="primary">Get Started</b-button>
        </home-card>
      </div>
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeCard from '../components/HomeCard.vue';

export default {
  name: 'Home',
  components: {
    homeCard: HomeCard
  }
}
</script>

<style scoped>
  .card-group{
    margin-bottom:25px;
  }
</style>