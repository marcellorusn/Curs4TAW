<script setup lang="ts">
import FullName from '@/components/computed/FullName.vue';
import PriceCalculator from '@/components/computed/PriceCalculator.vue';
import SupplierList from '@/components/computed/SupplierList.vue';
import { ref } from 'vue';


const fullName = ref("");
const totalPrice = ref("");

</script>



<template>
    <h2 class="text-xl font-bold ">Computed in Vue</h2>

    <FullName @update:fullName="fN => fullName = fN" />
    <p>Parent Component Full Name: {{ fullName }}</p>
    <hr class="my-4" />

    <PriceCalculator @update:totalPrice="tp => totalPrice = tp" />

    <hr class="my-4" />

    <SupplierList :fullName="fullName" :totalPrice="totalPrice" />


</template>




<style>
@import "bootstrap-icons";
@import "tailwindcss";
</style>