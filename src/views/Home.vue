<template>
  <div class="home">
    <hello-world v-bind:name="name"
      :age="age"
      :livingArea="livingArea"
      @change-address="childToParent"
    >
    </hello-world>
    <div><button v-on:click="parentToChild">부모에서 자식으로 주소변경</button></div>
    <div><button @click="setInitData">원래 주소로 변경</button></div>
    <div>{{computedName}}</div>
  </div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue';

export default {
  components: {
    'hello-world': HelloWorld,
  },
  data() {
    return {
      name: '초기 데이터',
      age: 999,
      livingArea: '초기 주소',
    };
  },
  computed: {
    computedName() {
      return this.name.substring(1, 3);
    },
  },
  created() {
    this.setInitData();
  },
  methods: {
    setInitData() {
      this.name = '조현영';
      this.age = 29;
      this.livingArea = '서울시 송파구';
    },
    parentToChild() {
      this.livingArea = '인천광역시 부평구';
    },
    childToParent(val) {
      this.livingArea = val;
    },
  },
};

</script>
