<template>
  <div>
    <Header />
    <Breadcrumb />
    <Nuxt />
  </div>
</template>

<script>
import Header from "../components/header";
import Breadcrumb from "../components/breadcrumb";

export default {
  components: {
    Header,
    Breadcrumb
  }
}
</script>
<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: #fafafa;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.content {
    max-width: 1080px;
    margin: 0 auto;
}
</style>
