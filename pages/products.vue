<template>
    <div class="products">
        <div v-for='(product,index) in products' :key='index' class="product">
            <div class="img-product">
                <img v-bind:src="product['photo']">
            </div>
            <div>{{ product['name'] }}</div>
        </div>
    </div>
</template>

<script>
import { mapActions } from 'vuex'

export default{

    data: function(){
        return{
            products: [
                {name: "Lipton Ice Tea", photo: "/img/lipton_icetea.jpg"},
                {name: "Coca cola", photo: "/img/lipton_icetea.jpg"},
                {name: "Fanta citron", photo: "/img/lipton_icetea.jpg"},
                {name: "Jus de pomme", photo: "/img/lipton_icetea.jpg"}
            ]
        }
    },
    
    mounted(){
    },

    methods: {
        
    }
}
</script>

<style>
.products{
    display:flex;
    flex-direction:column;
}
.product{
    display:flex;
    padding:15px;
    border-bottom: 1px solid grey;
    width:90%;
    align-self:center;
}
.img-product{
    width:30%;
}

.img-product img{
    width:100%;
}
</style>