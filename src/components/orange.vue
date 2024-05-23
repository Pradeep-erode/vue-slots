<template>
<!-- for slot props -->
  <div>
    <h5 v-for="fruit in fruits" :key="fruit.fruitname">

        <!-- normal slot usage  -->
    <!-- {{fruit.fruitname}} {{fruit.color}} -->

<!-- for conditional based slot assignment we can send data using v-bind directive like this-->
    <slot :fruitName="fruit.fruitname" :fruitColor="fruit.color"/>
    </h5>
    
  </div>
</template>

<script>
export default {
    name:'orange-fruit',
    data(){
        return{
            fruits:[{
                fruitname:'banana',
                color:'yellow'
            },
            {
                fruitname:'grapes',
                color:'blue'
            },
            {
                fruitname:'jackfruit',
                color:'yellow'
            }
            ]
        }
    }

}
</script>

<style>
div{
    color: orange;
}
</style>