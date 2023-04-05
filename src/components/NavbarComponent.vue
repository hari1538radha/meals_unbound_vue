<template>
  <div id="nav">
    <div class="block_1">
      <img id="logo-img" :src="Logo" />
      <select class="dropdown">
        <option>Product</option>
        <option>Shops</option>
        <option>location</option>
      </select>
      <input v-model="searchproduct" class="input-search" type="text" placeholder="search" />
      <div @click="handleInput" id="search-image">
        <img src="../components/icons/search.svg" />
      </div>
    </div>
    <div class="block_2">
      <div class="cell_container">
        <img :src="cell_image" />
        <p id="phone-number">+91&nbsp;63837&nbsp;27628</p>
      </div>
      <div class="profile_container">
        <img :src="userimage" />
        <P>username</P>
      </div>
    </div>
  </div>
</template>

<script setup>
import Logo from '../components/icons/Logo.svg'
import userimage from '../components/icons/userimage.svg'
import cell_image from '../components/icons/phonelogo.svg'
</script>
<script>
export default {
  data() {
    return {
      searchproduct: ''
    }
  },
  methods: {
    handleInput() {
      console.log(this.searchproduct)
      this.searchproduct = ''
    }
  }
}
</script>

<style>
#logo-img {
  margin-right: 26px;
  margin-left: 30px;
}
#nav {
  height: 106px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0px 1px 30px rgba(0, 0, 0, 0.06);
}
.dropdown
{
  width: 83px;
  height: 66px;
  border: 1px solid #d3d3d3;
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  border-right: none;
  color:#3E4958;
  padding-left: 5px;
}
.block_1 {
  display: flex;
}
.block_2 {
  display: flex;
}
.profile_container {
  display: flex;
  color: #3e4958;
  margin-right: 50px;
  font-weight: 800;
}
.profile_container p {
  margin-left: 10px;
}
.input-search {
  width: 542px;
  height: 66px;
  
  box-sizing: border-box;
  border: 1px solid #d3d3d3;
  padding-left: 30px;
}
#search-image {
  background-color: #5e81f4;
  height: 66px;
  width: 66px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}
.cell_container {
  display: flex;
  color: #3e4958;
  margin-right: 50px;
}
.cell_container p {
  margin-left: 10px;
}
</style>
