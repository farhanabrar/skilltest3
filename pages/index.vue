<template>
  <div>
    <atoms-card>
      <template v-slot:left>
        <ul>
          <li v-for="(left, i) in leftList" :key="i">{{ left }}</li>
        </ul>
      </template>
      <template v-slot:middle>
        <FormInput name="nama" :val="names" @value="(val) => (names = val)" />
        <button class="btn btn-primary" @click="addleftList">ke kiri</button>
        <button class="btn btn-primary" @click="addrightList">ke kanan</button>
      </template>

      <template v-slot:right>
        <ul>
          <li v-for="(right, i) in rightList" :key="i">{{ right }}</li>
        </ul>
      </template>
    </atoms-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      names: "",
      rightList: ["si merah"],
      leftList: ["si biru"],
    };
  },

  computed: {},

  methods: {
    addrightList() {
      this.rightList = [...this.rightList, this.names];
    },
    addleftList() {
      this.leftList = [...this.leftList, this.names];
    },
  },
};
</script>