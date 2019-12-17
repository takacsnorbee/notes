<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label>Note</label>
        <textarea class="form-control" rows="3" v-model="note"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <button class="btn btn-primary" @click.prevent="createNew" >Add new note</button>
      </div>
    </form>
  </div>
</template>
 
<script>
  export default {
    data: function() {
      return {
        note: ''
      };
    },
    methods: {
      createNew() {
        this.$emit('noteAdded', this.note);
        this.note = '';
      }
    }
  }
</script>

<style>
  form {
    width: 100%;
    margin: 0 auto;
  }
  .form-group {
    margin: 20px auto;
  }
</style>