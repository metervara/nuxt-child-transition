<template>
  <div class="container">
    <h1 class="title">
      Child Root Page
    </h1>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  key(route) {
    return route.fullPath
  },
}
</script>
