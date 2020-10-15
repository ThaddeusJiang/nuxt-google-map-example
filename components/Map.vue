<template>
  <div class="google-map" id="map"></div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        {
          src: "https://polyfill.io/v3/polyfill.min.js?features=default"
        },
        {
          src:
            "https://maps.googleapis.com/maps/api/js?key=AIzaSyB8Ovkw9LSpoP2-HOYCdd9ZKVhz6oEo7Vg",
          defer: true
        }
      ]
    };
  },
  props: {
    lat: Number,
    lon: Number
  },
  data() {
    return {};
  },
  mounted() {
    this.initMap();
  },
  methods: {
    initMap() {
      const location = { lat: this.$props.lat, lng: this.$props.lon };
      const map = new google.maps.Map(document.getElementById("map"), {
        center: location,
        zoom: 15
      });
      var marker = new google.maps.Marker({
        position: location,
        animation: google.maps.Animation.DROP
      });
      marker.setMap(map);
    }
  }
};
</script>

<style scoped>
.google-map {
  width: 100%;
  height: 400px;
}
</style>
