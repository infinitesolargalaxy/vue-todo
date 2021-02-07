<template>
  <div class="footer-wrapper">
    <div class="copyright-wrapper">
        <div class="copyright" :href="copyrightUrl" @click="goToLink(copyrightUrl)">
            {{ copyRightMessage }}
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoFooter',
  data() {
      return {
          copyRightMessage: "Copyright (c) 2021 Michael Ly",
          copyrightUrl: "https://github.com/infinitesolargalaxy/vue-todo/blob/main/LICENSE",
      }
  },
  methods: {
    goToLink(url) {
      // https://stackoverflow.com/questions/5141910/javascript-location-href-to-open-in-new-window-tab
      window.open(
        url,
        '_blank' // <- This is what makes it open in a new window.
      );
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: darkgrey;

    width: 100%;
    height: 40px;
    position: fixed;
    bottom: 0;
}
.copyright-wrapper {
    display: flex;
    justify-content: center;
}

.copyright {
  font-weight: bold;
  text-transform: capitalize;
  cursor: pointer;
}
</style>
