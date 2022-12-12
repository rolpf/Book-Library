<template>
  <div id="shelf">

    Number of liked books : {{count}}
    
    <span v-for="book in books">
      <Book :book="book" @minus="count--" @plus="count++"/>
    </span>
  </div>
</template>


<script>
import Book from './Book';

export default {
  name: 'Shelf',
  components: {
    Book
  },


  data: function() {
    return {
      books: [
      {title: 'The Jungle Book', author: 'Rudyard Kipling', pages: 300, date: '1894', liked: false},
      {title: 'The Lord of the Rings', author: 'J.R.R. Tolkien', pages: 500, date: '1954', liked: false},
      {title: '1984', author: 'George Orwell', pages: 200, date: '1949', liked: false},
      {title: 'The Hobbit', author: 'J.R.R. Tolkien', pages: 300, date: '1937', liked: false}
    ],
    count: 0,
    }
  }
}

</script>
