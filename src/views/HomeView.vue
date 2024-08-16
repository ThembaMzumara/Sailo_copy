<template>
  <div class="main">
    <HeaderComp />
    <div class="content">
      <BodyComp />
      <FooterComp />
    </div>
  </div>
</template>

<script setup>
import HeaderComp from '../components/HeaderComponent.vue'
import BodyComp from '../components/BodyComponent.vue'
import FooterComp from '../components/FooterComponent.vue'
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  height: 100vh;
  overflow: hidden;
  margin: 0;
  padding: 0;
}

header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.content {
  flex: 1;
  margin-top: 57px;
  overflow-y: auto;
}
</style>
