<template>
  <div>
    <Map v-if="lat" :lat="lat" :lon="lon" />
    <button @click="getCurrentPosition">Get current Position</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lat: null,
      lon: null
    };
  },
  methods: {
    getCurrentPosition() {
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(position => {
          const lat = position.coords.latitude;
          const lon = position.coords.longitude;
          this.$data.lat = lat;
          this.$data.lon = lon;
        });
      } else {
        console.warn("Geolocation is not supported for this Browser/OS.");
      }
    }
  }
};
</script>
