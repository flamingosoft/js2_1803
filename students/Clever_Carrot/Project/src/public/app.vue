<template>
    <div>
        <header>
            <div class="logo">E-shop</div>
            <div class="cart" id="cart">
                <form action="#" class="search-form">
                    <input type="text" class="search-field">
                    <button class="btn-search">
                        <i class="fas fa-search"></i>
                    </button>
                </form>
                <!-- button class="btn-cart" @click="showcart = !showcart">Cart</button>
                <div class="cart-block" v-show="showcart" -->
                <button class="btn-cart">Cart</button>
                    <cart ref="cartRef" />
            </div>
        </header>

        <main>
            <catalog ref="catalogRef" />
        </main>

    </div>
</template>

<script>
    import catalog from './containers/Catalog.vue'
    import cart from './containers/Cart.vue'
    export default {
        components: {
            catalog,
            cart
        },
        methods: {
            getData(url) {
                return fetch(url)
                .then(dataReceived => dataReceived.json())
            }
        }
    }
</script>

<style>

</style>