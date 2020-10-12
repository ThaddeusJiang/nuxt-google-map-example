<template>
  <div class="google-map" id="map"></div>
</template>

<script>
export default {
  data() {
    return {};
  },
  mounted() {
    this.initMap();
  },
  methods: {
    initMap() {
      const location = { lat: 35.626097, lng: 139.782513 };
      const map = new google.maps.Map(document.getElementById("map"), {
        center: location,
        zoom: 15
      });
      var marker = new google.maps.Marker({
        position: location,
        label: "T", // teamLab
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
