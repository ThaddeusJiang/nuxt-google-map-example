<template>
  <div>
    <div class="container">
      <div>
        <h2 class="title">
          teamLab Borderless
        </h2>

        <Map :lat="35.626097" :lon="139.782513" />
      </div>
    </div>
    <div class="container">
      <nuxt-link to="/local"><h2>Get your position</h2></nuxt-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
