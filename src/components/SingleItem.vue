<template>
    <div class="card my-3">
        <img :src="product.image" class="card-img-top w-50 mx-auto p-3" alt="">
        <div class="card-body">
            <h5 class="card-title">$ {{ product.price }}</h5>
            <p class="card-text">{{ product.title }}</p>
            <small>Rating: {{product.rating.rate}} </small>
            <div class="d-flex justify-content-evenly">
                <router-link :to="{ name: 'shopdetail', params: { id: product.id } }">
                    <button class="btn btn-warning">View</button>
                </router-link>
                <button class="btn btn-primary">Add To Cart</button>
                <button class="btn btn-danger" v-if="parent=='Shop'">Hello</button>
            </div>
        </div>
    </div>
</template>

<script>

    export default{
        name: 'SingleItem',
        props:{
            product : Object,
            parent: String,
        },
        data(){
            return{

            }
        }
    }
</script>

<style>
/* button{
    width:80px;
    height: 30px;
    font-size: 10px;
} */
</style>