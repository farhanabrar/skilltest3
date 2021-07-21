<template>
  <section>
    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
    <label for="jack">Jack</label>
    <input type="checkbox" id="john" value="John" v-model="checkedNames" />
    <label for="john">John</label>
    <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
    <label for="mike">Mike</label>
    <br />
    <span>Checked names: {{ checkedNames }}</span>
  </section>
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
    checkedNames: {
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