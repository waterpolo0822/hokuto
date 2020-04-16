<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
    <p>見たい名言をクリック</p>
    <div class=btn>
      <button v-on:click="active01=!active01" v-bind:class="{active:active01}">ラオウ</button>
      <button v-on:click="active02=!active02" v-bind:class="{active:active02}">ケンシロウ</button>
      <button v-on:click="active03=!active03" v-bind:class="{active:active03}">トキ</button>
      <button v-on:click="active04=!active04" v-bind:class="{active:active04}">ジャギ</button>
    </div>
    <ul class="text">
      <li class="serif" v-bind:class="{active:active01}">
        ラオウ「我が生涯に一片の悔いなし！」</li>
      <li class="serif" v-bind:class="{active:active02}">
        ケンシロウ「お前はすでに死んでいる」</li>
      <li class="serif" v-bind:class="{active:active03}">
        ラオウ「我が生涯に一片の悔いなし！」</li>
      <li class="serif" v-bind:class="{active:active04}">
        ジャギ「兄より優れた弟はいないのだ！」</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function() {
    return {
      active01: false,
      active02: false,
      active03: false,
      active04: false,
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
.btn .active {
  color: red;
}
.serif {
  display: none;
}
.text .active {
  display: block;
}
</style>
