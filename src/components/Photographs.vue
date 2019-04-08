<template>
  <div class="photographs">
    <div class="left">
      <div class="info">
        <span class="name">{{ name }}</span>
        <span class="photographer">{{ photographer }}</span>
        <span class="date">{{ date }}</span>
        <span class="context">{{ context }}</span>
      </div>
    </div>
    <div class="right" v-bind:style="imageStyle"></div>
  </div>
</template>

<script>
export default {
  name: "Photographs",
  props: {
    photos: Array
  },
  data() {
    return {
      index: 0,
    }
  },
  computed: {
    name() {
      return this.photos[this.index]["name"]
    },
    photographer() {
      return this.photos[this.index]["photographer"]
    },
    context() {
      return this.photos[this.index]["context"]
    },
    date() {
      return this.photos[this.index]["date"]
    },
    url() {
      return this.photos[this.index]["url"]
    },
    imageStyle() {
      let url = "url('../assets/" + this.url + "')"
      return {
        backgroundImage: url
      }
    }
  },
  methods: {
    next() {
      this.index = this.index + 1
    }
  }
}
</script>

<style>
.photographs {
  display: flex;
  align-items: stretch;
  height: 100%;
}

.left {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20%;
  background-color: #050505;
}

.info {
}

.info span {
  color: #ffffff;
  font-weight: 400;
}

.right {
  width: 80%;
  /* background-image: url("../assets/bloody_saturday.jpg"); */
  /* background-color: #050505; */
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}
</style>
