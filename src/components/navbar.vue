<template>
  <div class="nav" id="home">
    <div class="nav-l">
      <div class="logo">
        <a href="#home">
          <img src="../assets/logo.png" alt="logo">
        </a>
      </div>
    </div>

    <div class="nav-r">
      <ul>
        <li><a href="#carousel">Home</a></li>
        <li><a href="#carousel">About</a></li>
        <li><a href="#users">Users</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="ham" @click="toggleMenu" :aria-expanded="isOpen" aria-label="Toggle menu">
        <i class="fa-solid fa-bars"></i>
      </button>
    </div>

    <div class="mobile-menu" v-show="isOpen">
      <ul>
        <li><a href="#carousel" @click="closeMenu">Home</a></li>
        <li><a href="#carousel" @click="closeMenu">About</a></li>
        <li><a href="#users" @click="closeMenu">Users</a></li>
        <li><a href="#contact" @click="closeMenu">Contact</a></li>
      </ul>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}

const closeMenu = () => {
  isOpen.value = false
}
</script>



<style>
.ham {
  display: none;
  background: transparent;
  border: none;
  font-size: 24px;
  cursor: pointer;
  color: #282C3F;
  padding: 8px;
  transition: color 0.3s ease;
}

.ham:hover {
  color: #E4272C;
}

.mobile-menu {
  display: none;
  position: fixed;
  top: 70px;
  right: 0;
  width: 100%;
  background-color: #ffffff;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  animation: slideDown 0.3s ease;
}

.mobile-menu ul {
  list-style: none;
  padding: 16px 20px;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 0;
}

.mobile-menu li {
  padding: 12px 0;
  border-bottom: 1px solid #f0f0f0;
}

.mobile-menu li:last-child {
  border-bottom: none;
}

.mobile-menu a {
  text-decoration: none;
  font-size: 16px;
  font-weight: 500;
  color: #282C3F;
  display: block;
  transition: color 0.3s ease;
}

.mobile-menu a:hover {
  color: #E4272C;
}

@keyframes slideDown {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

 .nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 70px;
    z-index: 1000;
    display: flex;
    justify-content: space-between;
    align-items: center; 
    padding: 0 40px;
    background-color: #ffffff;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
}

.nav-l {
    display: flex;
    align-items: center;
}

.logo img {
    width: 42px;
    height: 42px;
    
}

.nav-r {
    display: flex;
    align-items: center;
}

.nav-r ul {
    list-style: none;
    display: flex;
    align-items: center; 
    gap: 28px;
    margin: 0;
    padding: 0;
}

.nav-r li {
    display: flex;
    align-items: center;
}

.nav-r a {
    text-decoration: none;
    font-size: 16px;
    font-weight: 500;
    color: #282C3F;
    padding: 8px 4px;
    transition: color 0.3s ease;
}

.nav-r a:hover {
    color: #E4272C;
}
@media (max-width: 768px) {
  .nav-r ul {
    display: none;
  }
  .ham {
    display: block;
  }
  .mobile-menu {
    display: block;
  }
  .nav {
    padding: 0 16px;
  }
}

</style>