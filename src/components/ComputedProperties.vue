<template>
    <h1>Computed</h1>
    <h2>Name : {{this.firstName}}</h2>
    <h2>Surname : {{this.lastName}}</h2>
   <div class="flex">
    <div>
        <span>{{this.items[0].name}}:{{this.items[0].price}}</span>
        <button :disabled="this.items[0].price + this.items[1].price + this.items[2].price >= 80000" v-on:click="AddPc()">Ekle</button>
    </div>
    <div>
        <span>{{this.items[1].name}}:{{this.items[1].price}}</span>
        <button :disabled="this.items[0].price + this.items[1].price + this.items[2].price >= 80000" v-on:click="AddKulaklık()">Ekle</button>
    </div>
    <div>
         <span>{{this.items[2].name}}:{{this.items[2].price}}</span>
         <button :disabled="this.items[0].price + this.items[1].price + this.items[2].price >= 80000" v-on:click="AddTablet()">Ekle</button>
    </div>
   </div>
   <p>Toplam tutar: {{this.items[0].price + this.items[1].price + this.items[2].price}}</p>
   <p v-if="this.items[0].price + this.items[1].price + this.items[2].price >= 55000">Paran bitiyor</p>
   <p v-if="this.items[0].price + this.items[1].price + this.items[2].price >= 80000">Paran bitti</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent ({
    name: "ComputedProperties",
    data() {
        return {
            firstName: "Ali",
            lastName: "ÇELEBİ",
            items: [
                {
                    name: "PC",
                    price: 15000
                },
                {
                    name: "Kulaklık",
                    price: 1200
                },
                {
                    name: "Tablet",
                    price:7000
                },
            ]
        }
    },
    computed: {
        fullName() {
        return `${this.firstName} ${this.lastName}`
        },
        total() {
            return `${this.items.name} ${this.items.price}`
        },
    },
    methods: {
        AddPc() {
            this.items[0].price = this.items[0].price + 15000
        },
        AddKulaklık() {
            this.items[1].price = this.items[1].price + 1200
        },
        AddTablet() {
            this.items[2].price = this.items[2].price + 7000
        }
    }
})

</script>


<style>
.flex {
    display: flex;
    align-items: center;
}
</style>