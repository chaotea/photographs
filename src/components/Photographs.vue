<template>
  <div class="photographs">
    <div class="left">
      <div class="info" v-for="photo in photos" v-bind:key="photo.name">
        <span class="name">{{ photo.name }}</span>
        <span class="photographer">{{ photo.photographer }}</span>
        <span class="date">{{ photo.date }}</span>
        <span class="context">{{ photo.context }}</span>
      </div>
    </div>
    <div class="right">
      <img class="photo" v-for="photo in photos" v-bind:key="photo.name" v-bind:src="toUrl(photo.url)">
    </div>
  </div>
</template>

<script>
export default {
  name: "Photographs",
  props: {
    photos: Array
  },
  methods: {
    toUrl(url) {
      return require(`../assets/${url}`)
    }
  }
}
</script>

<style>
.photographs {
  display: flex;
  align-items: stretch;
  background-color: #050505;
}

.left {
  width: 30%;
}

.info {
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  height: 100vh;
  width: 100%;
  color: #ffffff;
  font-size: 16px;
  font-weight: 400;
  font-style: normal;
  text-align: center;
}

.info span {
  margin: 0.5rem;
}

.info .name {
  display: block;
  font-size: 1.25rem;
  font-weight: 700;
}

.info .photographer {
  display: block;
}

.info .date {
  display: block;
   font-style: italic;
}

.info .context {
  display: block;
  margin: 2rem;
}

.right {
  width: 70%;
}

.photo {
  display: block;
  height: 100vh;
  max-width: 100%;
  margin: auto;
}
</style>
