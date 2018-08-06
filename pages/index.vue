<template>
  <section class="container">
    <div>
      <span>{{msg}}</span>
      <hr>
      <h1>这是首页信息</h1>

      <hr>
      <nuxt-link to="/user">切换到用户页面</nuxt-link>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  data(){
    return{
      msg:'hello vue-ssr'
    }
  },
  //  head () {
  //   return {}
  //     title: this.title,
  //     meta: [
  //       { hid: 'description', name: 'description', content: 'My custom description' }
  //     ]
  //   }
  // }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
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

