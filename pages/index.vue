<template>
  <section class="container">
    <link rel="stylesheet" href="//unpkg.com/vue-virtual-scroller@1.0.0-beta.6/dist/vue-virtual-scroller.css">

    <div style="width:700px;height:700px;border:1px solid #ddd;margin:50px auto">
      <RecycleScroller
        style="height:100%"
        :items="list"
        :item-height="32">
        <div slot-scope="{ item }" style="background:red;color:#fff">
          {{ item }}
        </div>
      </RecycleScroller>
    </div>
  </section>
</template>

<script>
  import { RecycleScroller } from 'vue-virtual-scroller'

  export default {
    components: {RecycleScroller},
    data () {
      return {
        list: Array.from({length: 50}, (v, i) => { return {a: i}})
      }
    }
  }
</script>
