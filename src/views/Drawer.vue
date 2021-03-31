<template>
  <div>
    <button @click="isOpen = !isOpen">My Profile</button>
    <div v-if="isOpen" class="drawer">
      <img src="../assets/avatar.png" alt="avater" />
      <div></div>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Drawer',
  data() {
    return {
      isOpen: false,
    }
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