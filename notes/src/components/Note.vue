<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
      <div class="panel panel-default">
          <div class="panel-body note">
              <slot></slot>
          </div>
      </div>
  </div>
</template>

<script>

</script>

<style>
    .panel-body {
        font-family: 'Lakki Reddy', cursive;
        font-size: 1.5rem;
        color: bisque;
        background-color: coral;
    }

    .note {
        cursor: pointer;
        margin: 20px;
        padding: 10px;
    }

    .note:hover {
        background-color: darkgray;
    }

</style>