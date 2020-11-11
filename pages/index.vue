<template>
  <div class="container">
    <div>
      <h1 class="title">
        Nuxt-child-transition-test
      </h1>
      <h3>Issue with transitins in nested routes</h3>
      <p>This site has both a page <strong>child.vue</strong> and dynamic routes for sub pages <strong>child/_id.vue</strong>, and it seems to break transitions for the children. Navigating between <strong>child/_id.vue</strong>.</p>
      <p><strong>child.vue</strong> has a <strong><nuxt-child /></strong> component for the dynamic routes.</p>
      <p>Removing the <strong>child.vue</strong>, and moving the <strong><nuxt-child /></strong> to index.vue fixes the issue with the transitions, but then there is no 'root' page for the children.</p>
    </div>
  </div>
</template>

<script>
export default {}
</script>
