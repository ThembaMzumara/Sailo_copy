<template>
  <div>
    <header class="header fixed-top">
      <div class="logo">
        <h5><span>envato</span> market</h5>
      </div>
      <button class="buy-now">Buy now</button>
    </header>
  </div>
</template>

<script setup></script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0px 25px;
  background-color: #282727;
  color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  height: 55px;
}

h5 {
  font-size: 19px;
  font-weight: 200;
  padding: 8px;
}

span {
  font-weight: 700;
}

.buy-now {
  padding: 5px 20px;
  background-color: #073f14;
  color: #fff;
  font-weight: 600;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.buy-now:hover {
  cursor: pointer;
}
</style>
