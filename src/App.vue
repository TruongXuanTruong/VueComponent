<template>
  <h1>Hello World !</h1>
  <FirstComponent></FirstComponent>
  <FirstComponent />
  <first-component></first-component>
  <first-component />
  <SecondComponent /> 
  <ProductList />
  <GobalComponent />
  <hr />
  <DemoSlots>
      <!-- <div>
        <h2> Day la doan html truyen xuong cho Demo Slots</h2>
      </div> -->
      <!-- <template v-slot:header>
        <h1>Header</h1>
      </template>
      <template v-slot:footer>
        <h1>Footer</h1>
      </template>
      <template v-slot:default>
        <h1>Defaul</h1>
      </template> -->
      <template #header>
        <h1>Header</h1>
      </template>
      <template #footer>
        <h1>Footer</h1>
      </template>
      <template #default>
        <h1>Defaul</h1>
      </template>
  </DemoSlots>
  <hr />
  <DemoCinemaComponent />
  <br />
  <br />
  <br />
  <br />
  <br />
</template>

<script>
import FirstComponent from "./components/FirstComponent.vue";
import SecondComponent from './components/SecondComponent.vue';
import ProductList from './components/ProductList.vue';
import DemoSlots from './components/DemoSlots.vue';
import DemoCinemaComponent from './components/DemoCinemaComponent.vue';
export default {
  name: 'App',
  components : {
    FirstComponent,
    SecondComponent,
    ProductList,
    DemoSlots,
    DemoCinemaComponent,
  },
  provide(){
    return {
      user: "Truong Xuan Truong",
    };
  },
}
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
