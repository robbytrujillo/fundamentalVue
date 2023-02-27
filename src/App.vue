<template>
  <h2>Welcome, {{ nama }}</h2>
  <!-- <button v-on:click="changeName">Change Name</button> -->
  <!-- disingkat -->
  <button @click="changeName">Change Name</button><br />
  <br />
  <input type="text" v-model="panggil" /><br />
  <!-- output agar realtime -->
  {{ panggil }}<br /><br />
  <a :href="url">Go To Laksana web solution</a>
  <br />
  <!-- condition if -->
  <div v-if="products.length">
    <ul>
      <!-- looping -->
      <li v-for="item in products" :key="item.id">{{ item.title }} - {{ item.price }}</li>
    </ul>
  </div>
  <div v-else>
    <p>No Data Found</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      nama: "Robby Ilhamkusuma",
      url: "https://laksanasolution.com",
      panggil: "",

      products: [
        // { id: 1, title: "Product 1", price: 1000 },
        // { id: 2, title: "Product 2", price: 2000 },
        // { id: 3, title: "Product 3", price: 3000 },
        // { id: 4, title: "Product 4", price: 4000 },
        // { id: 5, title: "Product 5", price: 5000 },
      ],
    };
  },
  methods: {
    changeName() {
      this.nama = "Asep";
    },
  },
  // Lifecycle hooks
  // beforeCreate() {
  //   console.log("Before Create");
  // },
  created() {
    //console.log("Created");
    this.products = [{ id: 1, title: "Product 1", price: 1000 },
        { id: 2, title: "Product 2", price: 2000 },
        { id: 3, title: "Product 3", price: 3000 },
        { id: 4, title: "Product 4", price: 4000 },
        { id: 5, title: "Product 5", price: 5000 },
      ],
  // },
  // beforeMount() {
  //   console.log("Before Mount");
  // },
  // mounted() {
  //   console.log("Mounted");
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
