<template property-form @add:houses="addHouses">

    <div id ='house-form'>
        <form>
            <label> House Name</label>
            <input type="text" />
            <label> House Dimensions</label>
            <input type="text" />
            <button> Add House</button>
        </form>
    </div>
</template>

<script>
    // import PropertyAddresses from "./PropertyAddresses";
    export default {
        name: "house-form",
        data() {
            return {
                houses: {
                    name:'',
                    dimensions:'',
                }
            }
        }
    }
</script>

<style scoped>
    form {
        margin-bottom: 2rem;
    }
</style>
