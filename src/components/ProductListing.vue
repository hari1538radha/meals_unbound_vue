<style scoped>
.main_container {
  display: flex;
  margin-top: 50px;
  margin-left: 50px;
  
}
.productcard
{
  margin-right: 50px;
}
</style>
<script setup>
import ProductCard from '../components/ProductCard.vue'
</script>
<template>
  <div class="main_container">
    <ProductCard class="productcard" />
  <GMapMap :center="center" :zoom="10" map-type-id="terrain" style="width: 900px; height: 593px">
    <GMapMarker
      :key="index"
      v-for="(m, index) in markers"
      :position="m.position"
      :clickable="true"
      :draggable="true"
      @click="openMarker(m.id)"
    >
      <!-- <GMapInfoWindow
          :closeclick="true"
          @closeclick="openMarker(null)"
          :opened="openedMarkerID === m.id"
      >
        <div>I am in info window {{ m.id }} </div>
      </GMapInfoWindow> -->
    </GMapMarker>
  </GMapMap>
  </div>
  
</template>

<script>
export default {
  data() {
    return {
      openedMarkerID: null,
      center: { lat: 10.5855, lng: 77.2513 },
      markers: [
        {
          id: 1,
          position: {
            lat: 10.5855,
            lng: 77.2513
          }
        },
        // {
        //   id: 2,
        //   position: {
        //     lat: 51.198429,
        //     lng: 6.69529
        //   }
        // }
      ]
    }
  },
  methods: {
    openMarker(id) {
      this.openedMarkerID = id
    }
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
