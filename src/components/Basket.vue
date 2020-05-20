<template>
    <div class="basket" >
        <div class="basket-item" >
          <h2 class="title-basket-item">{{goods.product_name}}</h2>
          <span class="price-basket-item">{{goods.price.toLocaleString()}} ₽</span>
          <span class="quantity-basket-item"></span>
          <button class="cart-button" type="button" >Удалить</button>
          </div>
      </div>
</template>

<script>
export default {
    
}
</script>

<style>
    .basket{
        max-width: 800px;
        height: 300px;
        background-color: rgb(237, 235, 235);
        border: 1px solid black;
        position: relative;
        z-index: 99;
        top: 350px;
        margin: 0 auto;
    }
    .basket-item{
        width: 94%;
        margin: 10px auto;
        display: flex;
        align-items: center;
        justify-content: space-around;
        border: 1px solid black;
    }
    .cart-button{
        outline: none;
        background-color: #1890FF;
        color: #FFFFFF;
        width: 97px;
        height: 35px;
        border: 1px solid #D9D9D9;
        box-sizing: border-box;
        box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.0015);
        border-radius: 2px;
        font-size: 16px;
        line-height: 24px;
        cursor: pointer;

    }
    .cart-button:hover{
        background-color: rgb(80, 151, 124);
        color: #fff;
    }
    .cart-button:active{
        background-color: #1890FF;
        color: rgb(59, 25, 11);
    }
</style>