<!--<property-addresses :houses="houses" />-->

<template>
  <div id="app">
    <h1>Properties</h1>
    <!--this has to be done correctly or the entries in the <tr> as props will not transfer over-->
    <property-addresses v-bind:houses="houses"/>
    <house-form @add:houses="houses"/>

  </div>
</template>

<script>
  import PropertyAddresses from "./components/PropertyAddresses"
  import HouseForm from "./components/HouseForm";
  //
  // export default {
  //   name: 'app',
  //   components: {PropertyAddresses,},
  // }
  export default {
    name: 'app',
    components: {
      HouseForm,
      PropertyAddresses,
    },
    data() {
      return {
              houses: [
          {id: 1, name: 'Burbank', dimensions: 'testing dimensions'},
          {id: 2, name: 'Brookline', dimensions: 'testing dimensions'}
        ],
      }
    },
  }

</script>

<style>
  button {
    background: #009435;
    border: 1px solid #009435;
  }

</style>
