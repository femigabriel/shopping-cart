<template>
  <div class="cart">
    <div class="title">
      <h1>Grocery Bud</h1>
    </div>
    <div class="flex">
      <div class="inputs">
        <input type="text" placeholder="e.g Eggs" />
      </div>
      <button>Submit</button>
    </div>
    <div class="cart-list" v-for="cart in carts" :key="cart">
      <h3>{{ cart.name }}</h3>
      <div class="flex">
        <div class="icon">
          <i class="lar la-edit"></i>
        </div>
        <div class="icon-1">
          <i class="lar la-trash-alt"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carts: [
        {
          name: "Bacon",
          price: "",
          remove: "",
        },
        {
          name: "Milk",
          price: "",
          remove: "",
        },
        {
          name: "Eggs",
          price: "",
          remove: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
.cart {
  background: #fff;
  padding-top: 20px;
  padding-bottom: 20px;
  border-radius: 5px;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
  /* font-size: 32px; */
}
.title h1 {
      text-shadow: 2px 2px 5px red;
  align-items: center;
  display: flex;
  justify-content: center;
  padding-top: 20px;
  padding-bottom: 20px;
  font-size: 36px;
}
.flex {
  display: flex;
  align-items: center;
  justify-content: center;
}
.input {
  width: 100%;
}
input {
    width: 600px;
    height: 40px;
    border-radius: 5px;
     text-indent: 10px;
     font-size: 18px;
}
button{
    padding: 15px 15px;
    color: ;
    background: honeydew;
    font-size: 16px;
    font-weight: 600;
    border-radius: 5px;
    border: none;
}

.cart-list {
  display: flex;
  justify-content: space-between;
  padding-left: 40px;
  padding-right: 40px;
  /* padding-top: 40px; */
  font-size: 18px;
  font-weight: 400;
  
}
.lar {
    font-size: 20px;
}
.icon {
color: greenyellow;

}
.icon-1 {
color: red;
}
</style>
