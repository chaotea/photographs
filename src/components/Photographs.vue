<template>
  <div class="photographs">
    <div class="left">
      <div class="info">
        <span class="name">{{ name }}</span>
        <span class="photographer">{{ photographer }}</span>
        <span class="date">{{ date }}</span>
        <span class="context">{{ context }}</span>
        <button v-on:click="next">NEXT</button>
      </div>
    </div>
    <div class="right" v-bind:style="{ 'background-image': 'url(' + url + ')' }"></div>
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
      return require(`../assets/${this.photos[this.index]["url"]}`)
    }
  },
  methods: {
    next() {
      this.index = (this.index < 14) ? (this.index + 1) : this.index
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
  width: 30%;
  background-color: #050505;
}

.info {
  width: 80%;
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
  background-color: #050505;
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}
</style>
