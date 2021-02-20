<template>
  <div class="product-slider">
    <div class="heading">
      <h2 class="topic">Daily Deals</h2>
      <h4 class="viewall">View all</h4>
    </div>

    <div class="container" style="overflow: scroll">
      <table class="tab">
        <td class="tab1" v-for="todo in todos" :key="todo.id">
          <img :src="todo.src" class="imageitems" />
          <div class="product-item__info">
            <div class="product-item-title">LOCK & LOCK</div>

            <div class="product-item-desc">
              LOC1263Ih Lock & Lock Plesio Frying Pan W/IH 26cm
            </div>
            <div class="product-item-price">27,820 Ks</div>
          </div>
        </td>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductSlider",
  props: ["todos"],
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
table,
td {
  border: 1px solid #e1e3e4;
  background-color: #ffffff;
}
table {
  /* width: 100%; */
  border-collapse: collapse;
  cursor: pointer;
  background-color: #ffffff;
}
.product-slider {
  background-color: #f4f6f7;
  margin: 0px;

  padding: 0px;
}
.container {
  width: 100vw;
  margin: 30px;
  padding: 10px;
  margin-top: 0px;
  height: 100%;
  margin-bottom: 0px;
}
.topic {
  padding: 10px;
  padding-bottom: 0;
  padding-top: 20px;
  font-family: Roboto, sans-serif;
  color: #0597cc;
  background-color: #f4f6f7;
  margin: 30px;
  margin-bottom: 0;
}
.viewall {
  padding: 10px;
  padding-bottom: 0;
  padding-top: 20px;
  font-family: Roboto, sans-serif;
  color: #0597cc;
  background-color: #f4f6f7;
  margin: 30px;
  margin-right: 8px;
  margin-bottom: 0;
}
.tab {
}
.imageitems {
  object-fit: contain;
  width: 193px;
  height: 193px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  padding: 5px;
}

.product-item-title {
  color: #677269;
  font-family: Roboto, sans-serif;
  background-color: #ffffff;

  font-size: 14px;
  margin: 20px;
  margin-top: 20px;
}

.product-item-desc {
  font-family: Roboto, sans-serif;
  margin: 20px;
  background-color: #ffffff;

  color: #0597cc;
  font-size: 16px;
}
.product-item-price {
  font-family: Roboto, sans-serif;
  background-color: #ffffff;

  color: #0597cc;
  font-size: 22px;
  margin: 20px;
}
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
