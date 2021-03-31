<template>
  <transition-group
    appear
    @before-enter="beforeEnter"
    @enter="enter"
    :css="false"
  >
    <div class="card" v-for="card in cards" :key="card.id">
      <p>{{ card.title }}</p>
    </div>
  </transition-group>
</template>

<script>
import Velocity from 'velocity-animate'

export default {
  name: 'Cards',
  data() {
    return {
      cards: [
        { title: 'Could contain anything', id: 123 },
        { title: 'Endless possibilities', id: 456 },
      ],
    }
  },
}
</script>

<style>
</style>