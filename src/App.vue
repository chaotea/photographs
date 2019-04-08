<template>
  <div id="app">
    <Photographs v-bind:photos="photos"></Photographs>
  </div>
</template>

<script>
import Photographs from "./components/Photographs.vue"

var photos = [
  {
    name: "Bloody Saturday",
    photographer: "H. S. Wong",
    context: "Battle of Shanghai, World War 2",
    date: "August 28, 1937",
    url: "bloody_saturday.jpg"
  },
  {
    name: "Burning Monk",
    photographer: "Malcolm Browne",
    context: "Persecution of buddhists in Vietnam by Ngô Đình Diệm",
    date: "June 11, 1963",
    url: "burning_monk.jpg"
  },
  {
    name: "Camelot",
    photographer: "Hy Peskin",
    context: "Cover of LIFE magazine",
    date: "July 20, 1953",
    url: "camelot.jpg"
  },
  {
    name: "Chairman Mao Swims in the Yangtze",
    photographer: null,
    context: null,
    date: "July 16, 1966",
    url: "chairman_mao_swims_in_the_yangtze.jpg"
  },
  {
    name: "Guerrillero Heroico",
    photographer: "Alberto Korda",
    context: null,
    date: "March 5, 1960",
    url: "che_guevara.jpg"
  },
  {
    name: "Earthrise",
    photographer: "William Anders",
    context: "Apollo 8 mission to the Moon",
    date: "December 24, 1968",
    url: "earthrise.jpg"
  },
  {
    name: "Lunch atop a Skycraper",
    photographer: null,
    context: "Construction of the Rockefeller Center",
    date: "September 20, 1932",
    url: "lunch_atop_a_skyscraper.jpg"
  },
  {
    name: "Mushroom Cloud Over Nagasaki",
    photographer: "Charles Levy",
    context: "Atomic bombing of Nagasaki, World War 2",
    date: "August 9, 1945",
    url: "mushroom_cloud_over_nagasaki.jpg"
  },
  {
    name: "Raising a Flag on Iwo Jima",
    photographer: "Joe Rosenthal",
    context: "Battle of Iwo Jima, World War 2",
    date: "February 23, 1945",
    url: "raising_a_flag_on_iwo_jima.jpg"
  },
  {
    name: "Raising a Flag over the Reichstag",
    photographer: "Yevgeny Khaldei",
    context: "Battle of Berlin, World War 2",
    date: "May 2, 1945",
    url: "raising_a_flag_over_the_reichstag.jpg"
  },
  {
    name: "Tank Man",
    photographer: "Jeff Widener",
    context: "Tiananmen Square protests",
    date: "June 5, 1989",
    url: "tank_man.jpg"
  },
  {
    name: "The Terror of War",
    photographer: "Nick Ut",
    context: "Vietnam War",
    date: "June 8, 1972",
    url: "the_terror_of_war.jpg"
  },
  {
    name: "V-J Day in Times Square",
    photographer: "Alfred Eisenstaedt",
    context: "Surrender of Japan",
    date: "August 14, 1945",
    url: "vj_day_in_times_square.jpg"
  },
  {
    name: "Winston Churchill",
    photographer: "Yousuf Karsh",
    context: null,
    date: "December 30, 1941",
    url: "winston_churchill.jpg"
  }
]

export default {
  name: "app",
  components: {
    Photographs
  },
  data: function() {
    return {
      photos: photos
    }
  }
}
</script>

<style>
html, body, #app {
  height: 100%;
  width: 100%;
  margin: 0px;
  padding: 0px;
}
</style>
