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
      checkedNames:[],
      names: "",
      rightList: ["si merah"],
      leftList: ["si biru"],
    };
  },

  computed: {},

  methods: {
    addrightList() {
      this.rightList = [...this.rightList, this.checkedNames];
    },
    addleftList() {
      this.leftList = [...this.leftList, this.checkedNames];
    },
  },
};
</script>