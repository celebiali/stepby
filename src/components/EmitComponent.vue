<template>
        <h1>Emit component</h1>
        <EmitChild :userList="userList"/>
        <AddSection @new-item="$emit('new-item',$event)"/>

</template>

<script>
import EmitChild from './EmitChild.vue';
import AddSection from './AddSection.vue';

export default {
   props: ["userList"],
    emits: ["new-item"],
    components: { EmitChild,AddSection }
};

</script>

