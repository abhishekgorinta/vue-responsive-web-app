<template>
  <div class="container" id="users">
    <h2>Our users</h2>
    <h4>Fetched From API</h4>
    <div class="card-wrapper">
      <div class="card" v-for="(user, index) in users" :key="index">
        <img :src="user.picture.medium" :alt="user.name.first">
        <h3>{{ user.name.first }} {{ user.name.last }}</h3>
        <p>{{ user.email }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const users = ref([]);

onMounted(async () => {
  const res = await fetch("https://randomuser.me/api/?results=10");
  const data = await res.json();
  users.value = data.results;
});
</script>

<style>
.container {
  padding: 20px;
  background-color: #f9f9f9;
  min-height: 100vh;
}

h2,
h4 {
  text-align: center;
}

.card-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 16px;
}

.card {
  background: #ffffff;
  padding: 16px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
  text-align: center;
  display: grid;
  place-items: center;
}

.card:hover {
  transform: translateY(-5px);
}

.card h3 {
  margin-top: 10px;
  font-size: 18px;
}

.card p {
  margin: 0 0 12px;
  color: #555;
  word-break: break-all;
}

.card img {
  border-radius: 50%;
  align-items: center;
}

img {
  width: 100px;
  height: 100px;
}
</style>
