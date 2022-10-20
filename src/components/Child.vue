<template>
    <div class="child">
        <h1>{{user.name}}</h1>
        <h1>{{user.email}}</h1>
    </div>
<div class="green">
    <Child2 :childUser="user"/>
</div>
</template>

<script lang="ts">
import {defineComponent} from "vue"
import Child2 from "./Child2.vue"

export default defineComponent( {
    name:"Child",
    props: {
        user: Object,
        email: String
    },
    components: {
        Child2,
    }
})
</script>

<style>
.child2 {
    background-color: green;
}
</style>