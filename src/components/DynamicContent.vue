<template>
  <fragment>
    <div v-if="loading">
      <p>loading...</p>
    </div>
    <slot v-else></slot>
  </fragment>
</template>

<script>
  import { Fragment } from "vue-frag";

  export default {
    components: {
      Fragment
    },
    data() {
      return {
        loading: true,
      }
    },
    mounted() {
      this.fakeRequest()
    },
    methods: {
      fakeRequest() {
        new Promise((resolve) => {
          setTimeout(() => {
            this.loading = false
            resolve()
          }, 3000);
        })
      }
    }
  }
</script>