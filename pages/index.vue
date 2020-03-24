<template>
  <div class="container">
    <div>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <logo />
      <h1 class="title">
        OG
      </h1>
      <h2 class="subtitle">
        Test social-sharing and OG content
      </h2>
      <div>
        <social-sharing
          :title="title"
          url="https://desolate-fjord-33890.herokuapp.com/"
          description="social-sharing description"
          inline-template
        >
          <div>
            <network network="facebook">
              <a class="button--green" style="margin-bottom: 15px;">
                Facebook
              </a>
            </network>
            <network network="line">
              <a class="button--green" style="margin-bottom: 15px;">
                Line
              </a>
            </network>
            <network network="twitter">
              <a class="button--green" style="margin-bottom: 15px;">
                Twitter
              </a>
            </network>
          </div>
        </social-sharing>
      </div>
      <hr style="margin-bottom: 30px;">
      <h1 class="title">
        PASS LIFF Login
      </h1>
      <h2 class="subtitle">
        Test pass user LIFF to storefront and new login flow (Alpha)
      </h2>
      <div style="display: flex; flex-direction: column; max-width: 200px; margin: 0 auto;">
        <a
          href="https://shop-alpha.line-beta.me/@096zenyh"
          class="button--grey"
          style="margin: 0 0 10px 0"
        >
          Go to ShopEnd
        </a>
        <a
          href="https://shop-alpha.line-beta.me/@096zenyh/product/100845842"
          class="button--grey"
          style="margin: 0 0 10px 0"
        >
          Go to ProductEnd
        </a>
        <a
          href="https://shop-alpha.line-beta.me/my"
          class="button--grey"
          style="margin: 0 0 10px 0"
        >
          Go to Profile
        </a>
      </div>
      <div style="display: flex; justify-content: center; align-items: center;">
        Logged in User : {{ $store.state.profile.displayName }}
        <img :src="$store.state.profile.pictureUrl" style="border-radius: 100%; width: 40px; margin-left: 10px;">
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
  margin: 30px auto;
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
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 22px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
