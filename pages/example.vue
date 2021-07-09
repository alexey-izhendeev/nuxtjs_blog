<template>
    <div>
       <ExampleComponent @sendTopage="data_from_component = $event" />
       <h1> This is parent page </h1>
       <p> This is data from component <b> {{data_from_component}}</b></p>
    </div>  
</template>

<script>
import ExampleComponent from "@/components/ExampleComponent";

export default {
   components: {
       ExampleComponent,
   },
   data() {
       return {
           data_from_component: ""
       }
   }
}
</script>

<style scoped>

</style>