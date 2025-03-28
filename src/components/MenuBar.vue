<script setup>
import Time from './Time.vue'
</script>

<template>
  <div class="menubar">
    <!-- Linkerkant -->
    <div class="menubar__left">
      <!-- Logo -->
      <div class="menubar__item">
        <router-link to="/">
          <img src="../assets/menubar/apple.svg" class="menubar_apple" />
        </router-link>
      </div>
      <!-- About -->
      <div class="menubar__item">
        <router-link to="/about">About</router-link>
      </div>
      <!-- ... -->
      <div class="menubar__item">
        <router-link to="/dock">Dock</router-link>
      </div>
    </div>

    <!-- Rechterkant -->
    <div class="menubar__right">
      <!-- Spotlight -->
      <div class="menubar__item">
        <router-link to="/">
          <img src="../assets/menubar/magnifyingglass.svg" class="menubar_spotlight" />
        </router-link>
      </div>
      <!-- Control Center -->
      <div class="menubar__item">
        <router-link to="/">
          <img src="../assets/menubar/switch.svg" class="menubar_controlcenter" />
        </router-link>
      </div>
      <!-- Timestamp -->
      <div class="menubar__item">
        <Time />
      </div>
    </div>
  </div>
</template>

<style scoped>
.menubar {
  display: flex;
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 30px;
  background: rgba(255, 255, 255, 0.5);
}

.menubar__left {
  display: flex;
  align-items: center;
  margin-left: 10px;
}

.menubar__item {
  margin-right: 5px;
  font-size: 14px;
  padding: 4px 10px;
  display: flex;
  align-items: center;
  filter: drop-shadow(0 4px 4px rgb(0, 0, 0, 0.25));
}

.menubar__item a {
  color: black;
  text-decoration: none;
  font-size: 14px;
}

.menubar__right {
  display: flex;
  align-items: center;
  margin-left: auto;
  margin-right: 10px;
}

.menubar__item:hover {
  background-color: #E6E6E6;
  border-radius: 4px;
}
</style>

