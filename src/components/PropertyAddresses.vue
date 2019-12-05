<!--passing the data:       <property-addresses :houses="houses />-->
<!--this is the same thing: <property-addresses v-bind:houses="houses />-->
<!--pass this inside the template- <property-addresses :houses="houses" />-->

<template>
    <div id="property-addresses">
        <table>
            <thead>
            <tr>
                <th>Property Address</th>
                <th>Property Dimensions</th>
            </tr>
            </thead>
            <tbody>
            <!--new code added here using "v-for attribute"-->
            <!--v-for= "houses in houses" :key="houses.id"-->
            <tr v-for= "houses in houses" :key="houses.id">
                <td>{{houses.name}}</td>
                <td>{{houses.dimensions}}</td>
                <!--<td>125 Burbank dr Nw</td>-->
                <!--<td>1,100 Sq. ft 3/1.5</td>-->
            </tr>
            <tr >
                <td>{{houses.name}}</td>
                <td>{{houses.dimensions}}</td>
                <!--<td>661 Brookline St SW</td>-->
               <!--<td>1,600 sq. ft duplex</td>&ndash;&gt;-->
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        name: "property-addresses",
        props: {
            houses: Array,
        },
    }
</script>
<style scoped></style>
