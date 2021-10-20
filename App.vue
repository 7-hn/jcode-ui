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


    <j-slider style="width: 250px; height: 350px;"
               :auto="2000"
               :cur-idx="curIdx"
               :list="list"
               @click="myClick"
               @slider="mySlider"
    ></j-slider>
  </div>
</template>
<script>
import JButton from './packages/j-test-button'
import JHeadline from './packages/j-test-headline'
import JSlider from './packages/j-test-slider'
export default {
  name: 'app',
  components: {
    JButton,
    JHeadline,
    JSlider
  },
  data () {
    return {
      curIdx: 0,
      list: [
        {
          url: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201807%2F14%2F20180714222556_mqijh.jpeg&refer=http%3A%2F%2Fc-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1637308330&t=50b799ccb86d517df1496502ad6a8983',
          alt: '草帽团'
        },
        {
          url: 'https://fuss10.elemecdn.com/3/63/4e7f3a15429bfda99bce42a18cdd1jpeg.jpeg?imageMogr2/thumbnail/360x360/format/webp/quality/100',
          alt: 'food'
        },
        {
          url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg',
          alt: '🐦'
        }
      ]
    }
  },
  methods: {
    myClick (i) {
      console.log('当前照片索引', i)
    },
    mySlider (i) {
      console.log('watch', i)
    }
  }
}
</script>
