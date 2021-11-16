<template>
  <button v-if="showA2HSBtn" class="action" @click="handleClick">
    Add Jetstream to your phone
  </button>
</template>

<script>
export default {
  name: "A2HSBtn",
  data() {
    return {
      deferredPrompt: null,
    };
  },
  created() {
    window.addEventListener("beforeinstallprompt", (e) => {
        console.log('pwa add')
      e.preventDefault();
      this.deferredPrompt = e;
    });
  },
  computed: {
    showA2HSBtn() {
      return this.deferredPrompt;
    },
  },
  methods: {
    handleClick() {
      console.log("clicked");
    },
  },
};
</script>

<style scoped>
.action {
  padding: 10px;
  background: #42b983;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
