<template>
  <div>
    <j-button type="red" size="big" icon="shop">按钮</j-button>

    <!--  显示  -->
    <j-button animated="fade">
      <div slot="hidden">$20000</div>
      <div slot="visible"><i class="shop icon"></i>不要错过哈</div>
    </j-button>
  </div>
</template>
<script>
import JButton from './packages/j-test-button'
export default {
  name: 'app',
  components: {
    JButton
  },
  data () {
    return {}
  }
}
</script>
