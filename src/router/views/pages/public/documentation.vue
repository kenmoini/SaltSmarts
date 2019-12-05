<script>
import appConfig from '@src/app.config'
import Layout from '@layouts/main'


export default {
  page: {
    title: 'Documentation',
    meta: [{ name: 'description', content: appConfig.description }],
  },
  components: { Layout },
  data() {
    return {
      title: 'Documentation',
      items: [],
    }
  },
}
</script>

<template>
  <Layout>

    <div class="row">

      

    </div>

  </Layout>
</template>

<style scoped>

</style>
