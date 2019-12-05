<script>
import appConfig from '@src/app.config'
import Layout from '@layouts/main'
import PageHeader from '@components/page-header'

export default {
  page: {
    title: 'FAQs',
    meta: [{ name: 'description', content: appConfig.description }],
  },
  components: { Layout, PageHeader },
  data() {
    return {
      title: 'FAQs',
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
          text: 'FAQs',
          active: true,
        },
      ],
      questions: [
        {
          id: 1,
          question: "What is Salt Smarts?",
          answer: "Salt Smarts is a hosted service that allows anyone to easily and quickly compute fertilizer requirements for any crop, in any geography, running on any system."
        },
        {
          id: 2,
          question: "What technology is this service built on?",
          answer: "Salt Smarts is built as a scalable microservice architecture that runs on top of an Enterprise Kubernetes OpenShift cluster.  The front-end is built as a Single Page Application (SPA) in <a href=\"https://vuejs.org/\">Vue.js</a> with Progressive Web Applcation (PWA) technologies enabled.  From there it reaches out to a number of brokered and managed APIs that integrate into the various microservices which have been built in Java, NodeJS, PHP, and Python."
        },
        {
          id: 3,
          question: "Where can I find the source code?",
          answer: "The source code can be found online for a number of the components.<ul class=\"mt-3\"><li><strong>Front-end SPA</strong><br />https://github.com/kenmoini/SaltSmarts</li></ul>"
        },
        {
          id: 4,
          question: "What is required to use Salt Smarts?",
          answer: "All you need to use Salt Smarts is an internet-connected web browser.  From there you can compute single fertilizers, bulk fertilizers, and more.  To access more advanced features such as fertilizer salt inventory management, saving of generated reports, and persistent profiles you will need to create an account and log in to access these more advanced features."
        },
        {
          id: 5,
          question: "How much does Salt Smarts cost?",
          answer: "Salt Smarts is completely free to use for Individuals and supports all the major functions.  For Groups of users we have Team and Enterprise plans with better collaboration and management within your domain."
        },
      ]
    }
  },
}
</script>

<template>
  <Layout>

    <PageHeader :title="title" :items="items" />

    <div class="row">
      <div class="col-sm-12">
        <div class="card">
          <div class="card-body">

            <div role="tablist" class="custom-accordion ml-4">
                
              <b-card no-body v-for="question in questions" class="mb-1">
                <b-card-header header-tag="header" role="tab">
                  <a href="javascript: void(0);" class="text-black">
                    <h5 v-b-toggle="'custom-' + question.id" class="m-0 font-size-14">
                      <i
                        class="uil uil-question-circle h3 text-primary icon"
                      ></i>
                      {{ question.question }}
                    </h5>
                  </a>
                </b-card-header>
                <b-collapse :id="'custom-' + question.id" visible accordion="accordion" role="tabpanel">
                  <b-card-body>
                    <b-card-text v-html="question.answer"></b-card-text>
                  </b-card-body>
                </b-collapse>
              </b-card>

            </div>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>

<style scoped></style>
