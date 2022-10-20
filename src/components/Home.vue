<template>
<div>
    <h1>Home components</h1>
    <Child :user="parentuser"/>
</div>
</template>

<script lang="ts">
import {defineComponent} from "vue"
import Child from "./Child.vue"

export default defineComponent({
    name:"Home",
    components: {
        Child
    },
    data() {
        return {
            parentuser: { name:"AliCelebi",email:"ali@hotmail.com"},
        }  
    },
 
   
})
</script>