<template>
  <div>
    <button @click="emitLogEvent">Emit from cond</button>
  </div>
</template>

<script>
export default {
  name: 'EventChildCond',
  methods: {
    emitLogEvent () {
      let data = {
        componentName: 'EventChild1',
        string: 'Lorem ipsum',
        complex: {
          string: 'Lorem ipsum',
          object: {
            number: 23,
            boolean: true,
            array: [1,2,3,4,5]
          }
        }
      }
      this.$emit('log', data)
    }
  }
}
</script>
