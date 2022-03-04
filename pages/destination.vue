<template>
  <h1>Destination</h1>
</template>

<script>
export default {
  data(){
    return{
      destinations: [],
    }
  },
  methods: {
    async loadData() {
      const response = await fetch(
        'https://space.wp.seiwald.hak-stjo.schulwebspace.at/wp-json/wp/v2/destination'
      )
      this.destination = await response.json()
  },
  },
  mounted() {
    this.loadData()
    document.body.style.backgroundImage = "url('background-destination-mobile.jpg')"
  },
}
</script>