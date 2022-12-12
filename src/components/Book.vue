<template>
  <div id="app">
    <label for="book-item"><strong>{{book.title}}</strong></label> by
    {{book.author}}</p>
    <p>written in {{book.date}}</p>
    <p>{{book.pages}} pages</p>
    
    <span v-if="book.liked">
      <button v-on:click="book.liked = false; $emit('minus')">Like</button>
    </span>
    <span v-else>
      <button v-on:click="book.liked = true;$emit('plus')">Liked</button>

    </span>
  </div>
</template>

<script>
export default {
  name: 'Book',
  props: {
    book: {
      type: Object,
      required: true,
    }
  },
  data: function() {
    return {
      liked: book.liked,
    }
  }
}

</script>