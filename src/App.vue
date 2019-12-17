<template>
  <div class="container" >
    <app-header :noteCount="notes.length" :maxNote="maxNotes"></app-header>
    <app-new-note @noteAdded="newNote"></app-new-note>
    <app-all-note :notes="notes" @noteDeleted="delNote"></app-all-note>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">You can delete a note by clicking on it. The number of max notes is 10.</div>
      </div>
    </div>
  </div>
</template>

<script>
  import Header from './components/Header.vue';
  import AllNote from './components/AllNote.vue';
  import NewNote from './components/NewNote.vue';

  export default {
    data: function() {
      return {
        notes: [
          'Ez a jegyzet azért jött létre, hogy legyen itt valami!'
        ],
        maxNotes: 10
      }
    },
    methods: {
      newNote(note) {
        if(this.notes.length >= this.maxNotes) {
          return alert('Please delete notes first!');
        }
        this.notes.push(note);
      },
      delNote(index) {
        this.notes.splice(index, 1);
      }
    },
    components: {
      appHeader: Header,
      appAllNote: AllNote,
      appNewNote: NewNote
    }
  }
</script>

<style>

</style>
