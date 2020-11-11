<template>
  <div class="child">
    <h2>Child sub page: {{$route.path}}</h2>
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  // transition: {
  //   name: 'custom',
  // },
  key(route) {
    return route.fullPath
  },
  async asyncData ({ params, $content }) {
    // console.log(params.id)
    const page = await $content(params.id).fetch()

    return {
      page
    }
  }
}
</script>
