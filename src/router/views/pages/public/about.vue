<script>
import appConfig from '@src/app.config'
import Layout from '@layouts/main'
import PageHeader from '@components/page-header'

/**
 * Starter component
 */
export default {
  page: {
    title: 'About',
    meta: [{ name: 'description', content: appConfig.description }],
  },
  components: { Layout, PageHeader },
  data() {
    return {
      title: 'About',
      items: [
        {
          text: 'Home',
          href: '/',
        },
        {
          text: 'Information',
          href: '#',
        },
        {
          text: 'About',
          active: true,
        },
      ],
    }
  },
}
</script>

<template>
  <Layout>

    <PageHeader :title="title" :items="items" />

    <div class="row">

      <div class="col-sm-12">

      </div>

    </div>

  </Layout>
</template>

<style scoped>

</style>
