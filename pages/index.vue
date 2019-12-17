<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        og-test
      </h1>
      <h2 class="subtitle">
        My marvelous Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data () {
    return {
      title: 'OG TEST!'
    }
  },
  head () {
    return {
      title: this.title,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' },
        { hid: 'og:title', property: 'og:title', content: this.title },
        { hid: 'og:description', property: 'og:description', content: 'My custom description' },
        { hid: 'og:image', property: 'og:image', content: 'https://d.line-scdn.net/lcp-prod-photo/20191120_23/1574192323336LfMD3_JPEG/G9RBG9IAQ5WOMNBT1LSF7VCS4CKC8N.jpeg' },
        { hid: 'og:type', property: 'og:type', content: 'object' },
        { hid: 'twitter:card', name: 'twitter:card', content: 'summary' },
        { hid: 'twitter:title', name: 'twitter:title', content: this.title },
        { hid: 'twitter:image', name: 'twitter:image', content: 'https://d.line-scdn.net/lcp-prod-photo/20191120_23/1574192323336LfMD3_JPEG/G9RBG9IAQ5WOMNBT1LSF7VCS4CKC8N.jpeg' },
        { hid: 'twitter:description', name: 'twitter:description', content: 'My custom description' }
      ]
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
