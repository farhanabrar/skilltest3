<template>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control"
      placeholder="Recipient's username"
      aria-label="Recipient's username"
      aria-describedby="button-addon2"
    />
    <div class="input-group-append">
      <button
        class="btn btn-outline-secondary"
        type="button"
        id="button-addon2"
      >
        pindah
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checkedNames: [],
    };
  },
  props: {
    name: { type: String, default: "default input text" },
    val: { type: String, default: "" },
  },
  computed: {
    value: {
      get() {
        return this.val;
      },
      set(value) {
        this.$emit("value", value);
      },
    },
  },
};
</script>