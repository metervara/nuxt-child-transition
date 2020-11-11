<template>
  <div class="child">
    <h1>CHILD: {{$route.path}}</h1>
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  transition: {
    name: 'custom',
  },
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
