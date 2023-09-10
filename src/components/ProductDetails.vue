<template>
    <div>
        <h3>{{ product.name }}</h3>
        <h2>{{ formattedPrice }}</h2>
        <p class="available" v-if="product.available">Available</p>
        <p class="out" v-else>Out of stock</p>
    </div>
</template>

<script>
export default {
    name: 'ProductDetails',

    data() {
        return {
            product: {
                name: 'Валирийский меч',
                price: 199.99,
                available: true,
            }
        };
    },

    computed: {
        formattedPrice() {
            return `${this.product.price.toFixed(2)} руб.`
        }
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>
    .available {
        color: green;
    }

    .out {
        color: red;
    }
</style>