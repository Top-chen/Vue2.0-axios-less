<template>
  <span class="icon"  :class="[classMap[stype],'icon'+iconType]"></span>
</template>

<script>

export default {
  props: {
    stype: {
      type: Number
    },
    iconType: {
      type: Number
    }
  },
  created() {
    this.classMap = ['decrease','discount','special','invoice','guarantee'];
  }
}
</script>

<style scoped lang="less" rel="stylesheet/less">
@import "../../common/less/mixin.less";
.icon(@W,@H,@MR,@NUM){
    display: inline-block;
    vertical-align: top;
    width: @W;
    height: @H;
    margin-right: @MR;
    background-size: @W @H;
    background-repeat: no-repeat;
    &.decrease{
      .bg-image('icon/decrease_@{NUM}');
    }
    &.discount{
      .bg-image('icon/discount_@{NUM}');
    }
    &.guarantee{
      .bg-image('icon/guarantee_@{NUM}');
    }
    &.invoice{
      .bg-image('icon/invoice_@{NUM}');
    }
    &.special{
      .bg-image('icon/special_@{NUM}');
    }
}
.icon1{
    .icon(12px,12px,4px,1)
}
.icon2{
    .icon(16px,16px,6px,2)
}
.icon3{
    .icon(12px,12px,2px,3)
}
.icon4{
    .icon(16px,16px,6px,4)
}
</style>
