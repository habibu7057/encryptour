<script setup>
import { ref } from 'vue'

const membersKey = ref([
  {
    name: "Kasumi Toyama",
    role: "Vocalist",
    id: "21120124140121",
    img: "https://i.bandori.party/u/c/art/4326Kasumi-Toyama-Cool-Hospital-Director-Toyama-AZ7QQX.png"
  },
  {
    name: "Saaya Yamabuki",
    role: "Drummer",
    id: "21120124140121",
    img: "https://i.bandori.party/u/c/art/4236Saaya-Yamabuki-Happy-A-Bag-Full-of-Enjoyment-13GKnX.png"
  },
])
</script>

<template>
  <h1>
    members page maybe
  </h1>
  <div class="members">
    <Card v-for="member in membersKey" type="card-big" :name="member.name" :role="member.role" :id="member.id"
      :image="member.img" />
  </div>
  <div class="members">
    <Card type="card-small" />
    <Card type="card-small" />
  </div>
</template>

<style scoped>
.members {
  max-width: 100vw;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 1rem;
}
</style>
