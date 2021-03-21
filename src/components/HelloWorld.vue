<template>
  <div class="group-zone">
    <Draggable v-model="numArr" group="group" @change="log">
      <div
        class="box"
        :class="num.group"
        v-for="(num, idx) in numArr"
        :key="`num-${idx}`"
      >
        {{ num.name }}
      </div>
    </Draggable>
    <Draggable v-model="engArr" group="group" @change="log">
      <div
        class="box"
        :class="eng.group"
        v-for="(eng, idx) in engArr"
        :key="`eng-${idx}`"
      >
        {{ eng.name }}
      </div>
    </Draggable>
  </div>
</template>

<script>
import Draggable from "vuedraggable";
export default {
  name: "HelloWorld",
  data() {
    return {
      numArr: [
        { name: 1, group: "num" },
        { name: 2, group: "num" },
        { name: 3, group: "num" },
        { name: 4, group: "num" },
        { name: 5, group: "num" },
      ],
      engArr: [
        { name: "a", group: "eng" },
        { name: "b", group: "eng" },
        { name: "c", group: "eng" },
        { name: "d", group: "eng" },
        { name: "e", group: "eng" },
      ],
    };
  },
  components: {
    Draggable,
  },
  props: {
    msg: String,
  },
  methods: {
    add() {
      console.log(111);
    },
    log(event) {
      console.log(Object.keys(event));
      if (Object.keys(event)[0] === "added") {
        console.log(event.added);
      } else {
        console.log(event.removed);
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.group-zone {
  width: 1024px;
  display: flex;
  justify-content: space-between;
  font-size: 50px;
}
.box {
  width: 200px;
  height: 200px;
  border: 3px solid #ffffff;
  display: grid;
  align-items: center;
  font-family: ;
  font-size: 140px;
}
.num {
  background: #63cdda;
}
.eng {
  background: #f8a5c2;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
