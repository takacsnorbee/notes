<template>
  <div class="row">
    <app-note v-for="(note, index) in notes" :key="note" @click.native="deleteNote(index)">{{ note }}</app-note>
  </div>
</template>

<script>
  import Note from './Note.vue';

  export default {
    props: ['notes'],
    components: {
      appNote: Note
    },
    methods: {
      deleteNote(index) {
        this.$emit('noteDeleted', index);
      }
    }
  }
</script>

<style>
.row {
  margin: 20px;
}
</style>