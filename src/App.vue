<template>
  <div id="app">
    <div>数据量: {{ this.list.length }}</div>
    <div v-for="(d, i) in list" @click="click(i)">
      <span>
        <span> 
          <span>
            <span>
              Hello {{name}} {{i}} {{d}}!
            </span>
          </span>
        </span>
      </span>
    </div>
  </div>
</template>

<script>


export default {
  name: 'app',
  data() {
    return {
      name: 'vue',
      list: new Array(500)
    }
  },
  methods: {
    click(index){
      this.list.splice(index, 1, 'test')
    }
  },
}
</script>


