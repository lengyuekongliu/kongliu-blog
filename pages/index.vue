<template>
  <div class="container">{{ name }}</div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

interface User {
  name: String
}

@Component({
  asyncData(context): User {
    console.log(111)

    // called every time before loading the component
    return { name: '11111' }
  },
})
export default class YourComponent extends Vue {}
</script>