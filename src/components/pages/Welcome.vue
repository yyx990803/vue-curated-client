<template>
  <div class="welcome-page page-content">
    <h1>Welcome</h1>
    <h2>Find the best packages for your Vue app!</h2>
    <section class="image preview">
      <img src="~assets/preview.svg" width="500" height="300" />
    </section>
    <section class="info">
      Browse a curated list of high-quality <a href="https://vuejs.org/">Vue.js</a> packages that will help you build awesome apps.
    </section>
    <section class="actions">
      <a href="https://github.com/vuejs/awesome-vue">
        <VueIcon icon="star"/>
        <span>Browse more packages</span>
      </a>
      <a href="https://github.com/vuejs/vue-curated">
        <VueIcon icon="assistant"/>
        <span>Submit a package</span>
      </a>
      <a href="https://github.com/vuejs/vue-curated-client">
        <VueIcon icon="edit"/>
        <span>Contribute to the app</span>
      </a>
    </section>
  </div>
</template>

<script>
export default {
  name: 'welcome-page',
}
</script>


<style lang="stylus" scoped>
@import "~style/imports";

h1,
h2,
section {
  text-align: center;
}

h1 {
  font-size: 3.2em;
  font-weight: 300;
  margin: 42px 0 0 0;
}

h2 {
  font-weight: 300;
  margin: 24px 0;
}

img {
  max-width: 100%;
}

.preview img {
  animation: preview .5s cubic-bezier(0.0, 0.0, 0.2, 1);;
}

@keyframes preview {
  from {
    transform: scale(.7);
    opacity: 0;
  }
  to {
    transform: none;
    opacity: 1;
  }
}

.info {
  color: #999;
  margin: 24px;
}

.actions {
  a {
    margin: 12px;
  }
}

@media ({$small-screen}) {
  .welcome-page {
    display: none;
  }
}
</style>
