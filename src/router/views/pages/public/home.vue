<script>
import appConfig from '@src/app.config'
import Layout from '@layouts/main'

/**
 * Starter component
 */
export default {
  page: {
    title: 'Home',
    meta: [{ name: 'description', content: appConfig.description }],
  },
  components: { Layout },
  data() {
    return {
      title: 'Home',
      items: [],
    }
  },
}
</script>

<template>
  <Layout>
    <div class="jumbotron jumbotron-fluid mt-5">
      <div class="container-fluid">
        <div class="row">
          <div class="col-sm-12 col-md-7">
            <h1 class="display-4">Factor in your fertilizer</h1>
            <p class="lead">
              Salt Smarts is a new hosted solution for agriculture enthusiasts,
              hobbyists, and professionals. Learn how to:</p>
            <ul>
              <li>Make your own fertilizer</li>
              <li><em>Save money on nutrients</em></li>
              <li>Gain flexibility over your feeding regimen</li>
              <li><em>Repond better to your crop</em></li>
            </ul>
            <div class="">
              <button class="btn btn-primary mr-3">Jump Right In &raquo;</button>
              <button class="btn btn-secondary">Learn More...</button>
            </div>
          </div>
          <div class="col-sm-12 col-md-5 text-center">
            <img src="@assets/images/growing_plant_01.jpg" alt="Salt Smarts" />
          </div>
        </div>
      </div>
    </div>

    <div class="row">

      <div class="col-sm-12 col-md-4">
        <div class="card">
          <div class="card-body">
            <h2>About</h2>
            <p>
              Want to learn more about what <strong>Salt Smarts</strong> is and
              what it can do? Maybe want to find out more about the powerful
              tools available to registered members? Take a look around, we got
              bomber jackets, manuals, even a few videos.
            </p>
            <div>
              <button class="btn btn-primary mr-3">About &raquo;</button>
              <button class="btn btn-secondary">FAQs</button>
            </div>
          </div>
        </div>
      </div>

      <div class="col-sm-12 col-md-4">
        <div class="card">
          <div class="card-body">
            <h2>Raw Salts</h2>
            <p>Raw Salts are fertilizer components, and in combining them you can tailor your own fertilizers, adjusted to <em>your</em> water, and create concentrates for a <em>fraction</em> of the cost of store-bought nutrients.<br><strong>No</strong> High School Diploma required.  We even have an <em>unofficial</em> For Dummies guide.</p>
            <div>
              <button class="btn btn-primary mr-3">Raw Salts for Dummies &raquo;</button>
              <button class="btn btn-secondary">Shop Salts</button>
            </div>
          </div>
        </div>
      </div>

      <div class="col-sm-12 col-md-4">
        <div class="card">
          <div class="card-body">
            <h2>Stats</h2>
            <p>
              Coming soon...
            </p>
          </div>
        </div>
      </div>

    </div>

  </Layout>
</template>

<style scoped>
.jumbotron-fluid {
  background: #fff;
}
</style>
