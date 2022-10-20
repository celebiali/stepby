<template>
      <ul>
            <li v-for="user in userList" :key="user">{{user}}</li>
        </ul>
</template>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
  //   inject: ["userList"],
     props: ["userList"]

})

</script>