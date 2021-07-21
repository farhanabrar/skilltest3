<template>
  <div class="center">
    <button type="button" class="btn btn-primary btn-lg btn-block">
      kiri
    </button>
    <br>
    <button type="button" class="btn btn-secondary btn-lg btn-block">
      kanan
    </button>
  </div>
</template>

<script>
export default {
  props: {
    warna: {
      type: String,
      default: "primary",
    },
  },
};
</script>