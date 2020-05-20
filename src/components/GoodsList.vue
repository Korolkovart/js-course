<template>
    <div class="goods-list">
        <GoodItem
            v-for="good of goods"
            :good="good"
            :key="good.id"
        />
    </div>

</template>

<script>

import GoodItem from '@/components/GoodItem.vue'

// const API = 'https://raw.githubusercontent.com/GeekBrainsTutorial/online-store-api/master/responses';
export default {
            props: ['goods'],
            components: {
                GoodItem
            }
}
        
    // methods:{
    //     FilterGoods() {
    //         const regexp = new RegExp(this.searchLine, 'i');
    //         this.filteredGoods = this.products.filter(product => {
    //             return regexp.test(product.product_name);
    //         });
    //     },

    // }
    

</script>

<style>

</style>