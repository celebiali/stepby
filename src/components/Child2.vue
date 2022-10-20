<template>
 <h1>{{childUser.name}}</h1>
 <h1>{{childUser.email}}</h1>
</template>

<script lang="ts">
import {defineComponent} from "vue"

export default defineComponent( {
    name:"Child2",
    props: ["childUser"]
})
</script>

<style>
.child {
    background-color: red;
}
</style>