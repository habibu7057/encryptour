<script setup>

const props = defineProps(['type', 'name', 'role', 'id', 'image'])

const cardBig = props.type === 'big'
const cardSmall = props.type === 'small'

</script>

<template>
  <main>
    <div class="card" :class="props.type">
      <div class="img">
        <img :src="props.image" alt="profile pic">
      </div>
      <div class="info">
        <div class="main">
          <h1>
            {{ props.name }}
          </h1>
          <h2>
            {{ props.role }}
          </h2>
        </div>
        <div class="more">
          <div class="elem">
            <div class="key">ID</div>
            <div class="value">{{ props.id }}</div>
          </div>
          <div class="elem">
            <div class="key">Key</div>
            <div class="value">Value we value we definitely value</div>
          </div>
        </div>
        <div class="socials">
          <button>IG</button>
          <button>TW</button>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  margin: 0.5rem;
}

.card {
  max-width: 100vw;
}

.socials>button {
  width: 2rem;
  height: 2rem;
}

.img {
  overflow: hidden;
  display: flex;
  justify-content: center;
}

.img>img {
  height: 100%;
}

.card-big {
  width: 32rem;
  height: 20rem;
  background: red;
  display: flex;
}

.card-big>.img {
  background: magenta;
  height: 100%;
  max-width: 40%;
}

.card-big>.info {
  padding: 0.5rem;
  padding-left: 1rem;
  display: flex;
  flex-direction: column;
}

.card-big>.info>.main>h1,
h2 {
  text-align: left;
  margin: 0;
}

.info>.more>.elem {
  display: flex;
}

.info>.more>.elem>* {
  text-align: left;
}


.elem>.key {
  width: 10ch;
}

.elem>.value {
  width: 100%
}

.card-big>.info>.socials {
  height: 2rem;
  margin-bottom: 0.5rem;
  display: flex;
  gap: 0.25rem;
}

.card-big>.info>.more {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.card-small {
  width: 30rem;
  height: 10rem;
  background: blue;
  display: flex;
}

.card-small>.img {
  width: 10rem;
  height: 10rem;
  background: magenta
}

.card-small>.info {
  margin-left: 0.5rem;
  position: relative;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: start;
  padding: 0.5rem;
}

.card-small>.info>.main>h1 {
  font-size: 1.5rem;
}

.card-small>.info>.main>h2 {
  /* font-size: 1.25rem; */
  display: none;
}

.card-small>.info>.more>.key {
  display: inline-block;
  width: 12ch
}

.card-small>.info>.socials {
  display: flex;
  gap: 0.25rem;
  flex-direction: column;
  position: absolute;
  right: 1rem;
  bottom: 1rem;
}
</style>
