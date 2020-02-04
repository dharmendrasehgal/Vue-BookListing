<template>
  <form class="" action="#" method="post" @submit.prevent="bookSubmit(bookTitle,bookAuthor)">
      <input type="text" v-model="bookTitle" name="title" value="" placeholder="Book Title">
      <input type="text" v-model="bookAuthor" name="author" value="" placeholder="Book Author">
      <button type="submit" name="button">Add Book</button>
  </form>
</template>
<script>
  export default {
    name: 'BookForm',
    props: ['books'],
    data() {
      return {
        bookTitle: '',
        bookAuthor: ''
      }
    },
    methods: {
      bookSubmit (bookTitle,bookAuthor) {
        return this.$emit('addBook', bookTitle, bookAuthor);
      }
    }
  }
</script>
<style>
li {
    display: block;
    margin: 0 10px;
  }
</style>
