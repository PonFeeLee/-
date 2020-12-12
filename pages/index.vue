<template>
  <div class="container">
    <el-carousel :interval="5000" arrow="always">
      <el-carousel-item v-for="(item, index) in banners" :key="index">
        <div
          class="banner-image"
          :style="
            `
                background:url(${item.url}) center center no-repeat;
                background-size:contain contain;
                `
          "
        ></div>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      banners: [
        {
          url:
            "http://img0.imgtn.bdimg.com/it/u=255540472,3722890280&fm=26&gp=0.jpg"
        },
        {
          url:
            "http://attach.bbs.miui.com/forum/201407/12/191515sskuppax42aarano.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.container {
  min-width: 1000px;
  margin: 0 auto;
  position: relative;

  /deep/ .el-carousel__container {
    height: 700px;
  }

  .banner-image {
    width: 100%;
    height: 100%;
  }
}
</style>
