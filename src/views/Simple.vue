<template>
  <transition appear @before-enter="beforeEnter" @enter="enter" :css="false">
    <div class="card"></div>
  </transition>
</template>

<script>
import gsap from 'gsap'

export default {
  name: 'Simple',
  methods: {
    beforeEnter(el) {},
    enter(el, done) {},
  },
}
</script>

<style scoped>
.card {
  width: 6.5em;
  height: 6.5em;
  display: block;
  border-radius: 1%;
  margin: 0 auto 0 auto;
  background-color: #16c0b0;
  box-shadow: 0.08em 0.03em 0.4em #ababab;
}
</style>