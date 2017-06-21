<template>
  <div id="app">
   <cart></cart>
    <book-list></book-list>
  </div>
</template>

<script>
import BookList from './components/BookList';
import Cart from './components/Cart';


export default {
  components: {
     BookList,
     Cart

  }
}
</script>

<style>

</style>
