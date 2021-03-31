<template>
  <div>
    <button @click="isOpen = !isOpen">My Profile</button>
    <transition
      @before-enter="beforeEnter"
      @enter="enter"
      @leave="leave"
      :css="false"
    >
      <div v-if="isOpen" class="drawer">
        <img src="../assets/avatar.png" alt="avater" />
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
    </transition>
  </div>
</template>

<script>
import Velocity from 'velocity-animate'

export default {
  name: 'Drawer',
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    beforeEnter(el) {
      el.style.opacity = 0
      el.style.width = '0em'
    },
    enter(el, done) {
      Velocity(
        el,
        {
          opacity: 1,
          width: '12em',
        },
        {
          duration: 1000,
          easing: [60, 10],
          complete: done,
        }
      )
    },
    leave(el, done) {
      Velocity(
        el,
        {
          opacity: 0,
          width: '0em',
        },
        {
          duration: 500,
          easing: 'easeInCubic',
          complete: done,
        }
      )
    },
  },
}
</script>

<style scoped>
img {
  width: 2.5em;
  height: 2.5em;
  border-radius: 50%;
}

.drawer {
  width: 12em;
  height: 20em;
  display: flex;
  border-radius: 1%;
  padding-top: 0.7em;
  align-items: center;
  flex-direction: column;
  background-color: #e0e0e0;
  box-shadow: 0.08em 0.03em 0.4em #ababab;
}

.drawer div {
  width: 95%;
  height: 3.5rem;
  border-radius: 1%;
  margin-top: 0.6rem;
  background-color: #f0f0f0;
  border: 0.02em solid #ababab;
}
</style>