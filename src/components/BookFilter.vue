
    <template>
        <section class="book-filter">
            <h2>Books Filter</h2>
            <input type="text" v-model="bookFilter.byText" placeholder="Filter By Name" >
        </section>
    </template>

    <script>
    export default {
    name: 'book-filter',

    data() {
        return {
            bookFilter: { byText: '', byMaxPrice: 1000 }
        }
    },
    created() {
        this.$watch('bookFilter.byText', function (newVal, oldVal) {
            this.$emit('set-filter', this.bookFilter);
        })

    },
    methods: {

    }
}
</script>
<style scoped>
.book-filter {

    background: lightgreen;
    padding:10px;
    margin: 10px;
}
input {
    padding: 10px;
}
h2 {
    font-family: sans-serif;
}
</style>
