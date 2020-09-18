<template>
  <div>
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'
export default {
  components: { AppHeader }
}
</script>

<style>
body, html {
  margin: 0;
  padding: 0;
  font-family: "Open Sans",-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
  font-size: 16px;
  color: rgba(99, 99, 99, 1);
  overflow: hidden;
}

*, :after, :before {
  box-sizing: border-box;
  border: 0 solid #d9d9d9;
}

</style>
