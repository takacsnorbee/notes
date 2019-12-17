<template>
  <div class="row">
    <div class="col-sm-12">
      <h3 class="text-center">Note added</h3>
      <div class="progress">
        <div class="progress-bar" role="progressbar" 
              aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"
              :style="{width:( noteCount / maxNote ) * 100 + '%'}">
              {{ noteCount }} / {{ maxNote }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['noteCount', 'maxNote']
}
</script>

<style>
  .progress-bar, .progress {
    height: 2rem;
  }
</style>