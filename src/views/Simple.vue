<template>
  <transition appear @before-enter="beforeEnter" @enter="enter" :css="false">
    <div class="card"></div>
  </transition>
</template>

<script>
export default {
  name: 'Simple',
}
</script>

<style>
</style>