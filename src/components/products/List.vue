<template>
    <div class="products">
        <h1>Products</h1>
        <div class="list">
            <div class="item" v-for="product in products" :key="product.slug">
                <h3 @click="select(product)">{{ product.name }}</h3>
                <img :src="product.thumbnail" :alt="product.name" @click="select(product)" />
                <p @click="select(product)">{{ product.shortDescription }}</p>
                <p @click="select(product)">{{ product.price }}</p>
                <hr />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "product-list",
    data() {
        return {
            products: [
                {
                    name: "Samsung Galaxy S8",
                    slug: "samsung-galaxy-s8",
                    thumbnail: "http://placehold.it/200x300",
                    shortDescription: "Samsung Galaxy S8 Android smartphone with true edge to edge display.",
                    price: 499.99,
                    description: "The Infinity Display has an incredible end-to-end screen that spills over the phone’s sides, forming a completely smooth, continuous surface with no bumps or angles. It’s pure, pristine, uninterrupted glass. And it takes up the entire front of the phone, flowing seamlessly into the aluminum shell. The result is a beautifully curved, perfectly symmetrical, singular object."
                }
            ],
            selectedProduct: null
        };
    },
    methods: {
        select(product) {
            this.selectedProduct = product;
        }
    }
}
</script>

<style>

</style>
