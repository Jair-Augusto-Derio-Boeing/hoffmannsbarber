<script>
import router from './router';

export default {
  mounted () {
    router.push('/home');
  },
}
</script>

<template>
  <RouterView></RouterView>
</template>

<style></style>
