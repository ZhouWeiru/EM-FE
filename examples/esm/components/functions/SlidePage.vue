<template>
  <div>
    <div class="demo">
      <emfe-slide :percent="14" maxPercent="100" slideLeft="小" slideRight="大"></emfe-slide>
    </div>
    <br>
    <pre>
      &lt;emfe-slide percent="50" maxPercent="100" slideLeft="小" slideRight="大"&gt;&lt;/emfe-slide&gt;
    </pre>
    <br>
    <br>
    <emfe-slide :percent="val" maxPercent="100" slideLeft="小" slideRight="大" @change="change"></emfe-slide>
    当前进度: {{ val }}%
    <br>
    <pre>
      &lt;emfe-slide :percent="val" maxPercent="100" slideLeft="小" slideRight="大" @change="change"&gt;&lt;/emfe-slide&gt;
    </pre>
    <pre>
      change(val) {
        this.val = val;
      }
    </pre>
    <br>
    <br>
    <h3>API</h3>
    <table style="width: 100%;text-align: center;">
      <thead>
        <tr>
          <th>属性</th>
          <th>说明</th>
          <th>类型</th>
          <th>默认值</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>className</td>
          <td>需要修改的样式</td>
          <td>String</td>
          <td>-</td>
        </tr>
        <tr>
          <td>percent</td>
          <td>进度条进度的value值</td>
          <td>String</td>
          <td>-</td>
        </tr>
        <tr>
          <td>maxPercent</td>
          <td>进度条最大值</td>
          <td>String</td>
          <td>-</td>
        </tr>
        <tr>
          <td>width</td>
          <td>进度条的宽度</td>
          <td>String</td>
          <td>-</td>
        </tr>
        <tr>
          <td>slideLeft</td>
          <td>进度条的左边描述</td>
          <td>String</td>
          <td>-</td>
        </tr>
        <tr>
          <td>slideRight</td>
          <td>进度条的右边描述</td>
          <td>String</td>
          <td>-</td>
        </tr>
      </tbody>
    </table>
    <h3>注册的方法</h3>
    <table style="width: 100%;text-align: center;">
      <thead>
        <tr>
          <th>事件名</th>
          <th>说明</th>
          <th>返回值</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>change</td>
          <td>拖动滑块触发</td>
          <td>滑动元素和距离左边的距离</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  name: 'editPage',
  data() {
    return {
      val: 14,
    };
  },
  methods: {
    change(val) {
      this.val = val;
    }
  }
}
</script>
<style>
.demo {
  width: 451px;
}
</style>
