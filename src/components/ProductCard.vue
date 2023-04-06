<script>

</script>
<template>
  <div class="product_container">
    <div>
      <img src="../components/icons/product1.svg" />
    </div>
    <div class="discription_Contaianer">
      <h2 class="product_title">Fully Furnished Smart Studio Apartment</h2>
      <div class="rating_container">
        <div>
          <img src="../components/icons/Star.svg" />
          <p>4.5</p>
        </div>
        <div>
       content
        </div>
      </div>
      <div class="rating_container">
        <div class="detail_image--bg">
          <img src="../components/icons/store.svg" />

        </div>
        <div>
       content
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.product_container {
  display: flex;
  align-items: center;
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.15);
  border-radius: 20px;
  width: 561px;
  height: 215px;
}
.product_container img {
  margin-left: 10px;
}
.product_title {
  font-size: 18px;
  font-weight: 800px;
  margin-left: 10px;
}
.detail_image--bg
{
    background-color:#5E81F4;
}

.discription_Contaianer {
  display: flex;
  flex-direction: column;
}
.discription_Contaianer h2 {
  flex-wrap: wrap;
  width: 256px;
  margin-left: 10px;
}
.rating_container div {
  display: flex;
}
.rating_container {
  display: flex;
  align-items: center;
  column-gap: 20px;
}
</style>
