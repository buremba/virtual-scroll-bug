<template>
<div>
fsdfd
<link rel="stylesheet" href="//unpkg.com/vue-virtual-scroller@1.0.0-beta.6/dist/vue-virtual-scroller.css">

  <RecycleScroller
    style="height:100%"
    :items="list"
    :item-height="32">
    <div slot-scope="{ item }" class="user">
      {{ item }}
    </div>
  </RecycleScroller>
  </div>
</template>
<script>
import { RecycleScroller } from 'vue-virtual-scroller'
export default {
  components: {RecycleScroller},
  data () {
    return {
    list: [{test: 1}, {test:3}]
    }
  }
}
</script>