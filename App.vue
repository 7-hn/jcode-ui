<template>
  <div>
    <j-button type="red" size="big" icon="shop">按钮</j-button>

    <!--  显示  -->
    <j-button animated="fade">
      <div slot="hidden">$20000</div>
      <div slot="visible"><i class="shop icon"></i>不要错过哈</div>
    </j-button>


    <j-headline :level="1" icon="tag" size="mini">
      标题
      <div slot="sub">
        子标题
      </div>
    </j-headline>
  </div>
</template>
<script>
import JButton from './packages/j-test-button'
import JHeadline from './packages/j-test-headline'
export default {
  name: 'app',
  components: {
    JButton,
    JHeadline
  },
  data () {
    return {}
  }
}
</script>
