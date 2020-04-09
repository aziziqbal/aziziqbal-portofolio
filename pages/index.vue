<template>
  <div>
    <about />
    <services />
  </div>
</template>

<script>
import About from '~/components/about.vue'
import Services from '~/components/services.vue'

export default {
  components: {
    About,
    Services
  }
}
</script>
