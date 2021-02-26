<template>
  <div class="home">
    <step class="step" :current_page=1 :step_number=3></step>
  </div>
</template>

<script>
// @ is an alias to /src
import step from "../components/step-indicator"

export default {
  name: 'Home',
  components: {
    step
  }
}
</script>

<style lang="scss">
  .step{
    height: 10em;
  }
</style>