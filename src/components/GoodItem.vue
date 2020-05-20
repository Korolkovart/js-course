<template>
   <div class="goods-list">
        <!-- <template v-if="filteredGoods.length == 0">
          <h3>Упс, нет такого товара, попробуйте еще раз </h3>
      </template> -->
        <div class="goods-item" >
            <img class="img-goods" src="@/img/icon-cart.svg" alt="photo-goods">
            <div class="inf-goods">
                <h3 class="name-goods">{{good.product_name}}</h3>
                <p class="price-goods">{{good.price.toLocaleString()}} ₽</p>
                <button class="goods-button" type="button"> Добавить в корзину</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        good: {
            type: Object,
            required: true
        }
    }
    
}
</script>

<style>
    .goods-list{
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;

    }
    .goods-item{
        width: 250px;
        height: 300px;
        padding: 0 0 10px 0;
        margin: 0 0 30px 0;
        box-sizing: border-box;
        display: flex;
        align-items: flex-end;
        justify-content: center;
        flex-wrap: wrap;
        border: 1px solid black;
        box-shadow: 4px 12px 2px rgba(0, 0, 0, 0.09);
    }
    .inf-goods{
        width: 100%;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    .name-goods{
        font-size: 30px;
        margin: 0;
        width: 100%;
        text-align: center;
    }

    .price-goods{
        padding: 10px 0 10px 0;
        box-sizing: border-box;
        font-size: 24px;
        margin: 0;
        width: 100%;
        text-align: center;
    }
    .goods-button{
        outline: none;
        background-color: #40905cc7;
        color: #FFFFFF;
        width: 78%;
        height: 35px;
        border: 1px solid #D9D9D9;
        box-sizing: border-box;
        box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.0015);
        border-radius: 12px;
        font-size: 16px;
        line-height: 24px;
        cursor: pointer;
    }
    .goods-button:hover{
        background-color: rgb(210, 136, 2);
    }
    .goods-button:active{
        background-color: #40905cc7;
        color: rgb(59, 25, 11);
    }
</style>