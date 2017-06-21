<template>
        <section class="cart">
            <h1>Cart</h1>
            <!--<hello />-->
            <ul>
                <li v-for="item in items">
                    {{item.title}} (Quantity: {{item.quantity}})
                    <p>TAG: {{item.tag}}</p>
                </li>
            </ul>
            <p>Total: {{total}}</p>
           

        </section>
    </template>

    <script>
    import cartService from '../cart.service';

    export default {
        name: 'cart',

    data() {
        return {
            items: cartService.getCartItems(),
        }
    },
    computed: {
        total() {
           this.items;
           return cartService.getCartTotal(); 
        }               

    },
    methods: {
       
    },
    components: {
      //  hello
    }
}
</script>

<style scoped>

</style>
