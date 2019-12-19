<template>
    <div>Hey</div>
</template>

<script>
import { mapActions } from 'vuex'

export default{

    mounted(){
        fetchProducts()
    },
    computed: mapState({
        products: state => state.api
    }),
    methods: {
        ...mapActions(['fetchProducts'])
    }
}
</script>

<style>

</style>