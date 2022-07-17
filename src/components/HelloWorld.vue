<template>
  <div class="container">
    <div class="title">
      <h1>YOUR BAGS</h1>
    </div>
    <div class="bag-list" v-for="list in lists" :key="list">
      <div class="lists-items">
        <div class="flex">
          <div class="img">
            <img :src="list.image" alt="" />
          </div>
          <div class="content">
            <div class="list-name">
              <h3>{{ list.name }}</h3>
            </div>
            <div class="price">
              <p>{{ list.price }}</p>
            </div>
            <div class="remove">
              <P>{{ list.remove }}</P>
            </div>
          </div>
        </div>
        <!-- flex ends here -->
      </div>
      <div class="list-count">
        <div class="icon"><i class="las la-angle-up"></i></div>
        <h3>1</h3>
        <div class="icon"><i class="las la-angle-down"></i></div>
      </div>
      <!-- listed items ends here -->
    </div>
    <div class="amount">
      <p>Total</p>
      <p>$1200</p>
    </div>
    <div class="btn">
      <button>CLEAR CART</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      lists: [
        {
          image: [require("../images/phone1.png")],
          name: "Samsung Galaxy S8",
          price: "$399.99",
          remove: "remove",
        },
        {
          image: [require("../images/phone1.png")],
          name: "Samsung Galaxy S8",
          price: "$399.99",
          remove: "remove",
        },
        {
          image: [require("../images/phone1.png")],
          name: "Samsung Galaxy S8",
          price: "$399.99",
          remove: "remove",
        },
        {
          image: [require("../images/phone1.png")],
          name: "Samsung Galaxy S8",
          price: "$399.99",
          remove: "remove",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  border: 3px solid wheat;
  padding-left: 20px;
  padding-right: 20px;
  padding-bottom: 40px;

}
h1 {
  align-items: center;
  display: flex;
  justify-content: center;
  padding-top: 20px;
  padding-bottom: 20px;
  font-size: 32px;
}
.bag-list {
  display: flex;
  justify-content: space-between;
}
.lists-items {
  display: flex;
}
.bag-list {
  padding-bottom: 20px;
}
.list-count {
  /* margin: -10px */
}
.content {
  padding-right: 20px;
}
.content p {
  padding-right: 50px;
}
.list-name {
  /* padding-left: 20px; */
}
.flex {
  display: flex;
}
img {
  width: 80px;
  /* padding-left: 60px; */
}
.price {
  font-size: 16px;
  font-weight: 700;
  margin: -5px 0px;
}
.remove {
  color: blue;
  font-weight: 700;
  font-size: 14px;
  margin: 10px 0px;
}
.amount {
  display: flex;
  justify-content: space-between;
  border-top: 3px solid green;
  padding-left: 20px;
}
.amount p {
  padding-right: 20px;
  font-weight: 900;
  font-size: 16px;
}
.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  align-items: center;
  padding-bottom: 20px;
}
button {
  color: brown;
  background: transparent;
  border: 1px solid brown;
  font-size: 18px;
  border-radius: 5px;
  padding: 10px 30px;
  font-weight: 700;
}
</style>
