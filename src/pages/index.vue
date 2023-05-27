<script>
export default {

}
</script>

<template>
  <div class="background">
    <div class="decorations">
      <img class="top-left" src="../../public/zelda/pattern.svg">
      <img class="bottom-left" src="../../public/zelda/pattern.svg">
      <img class="bottom-right" src="../../public/zelda/pattern.svg">
      <img class="top-right" src="../../public/zelda/pattern.svg">
    </div>
    <div class="content">
      <div class="title">
        <img class="title-image" src="../../public/zelda/title.png">
      </div>
      <div class="buttons">
        <img class="button" src="../../public/zelda/button1.png" alt="制作实录">
        <img class="button" src="../../public/zelda/button2.png" alt="人物设定">
        <img class="button" src="../../public/zelda/button3.png" alt="历代作品">
        <img class="button" src="../../public/zelda/button4.png" alt="壁纸下载">
      </div>
    </div>
  </div>
</template>

<style>
.background {
  background-image: url(../../public/zelda/index-bg.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.title {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: -300px; /* 调整向上的偏移量，这里设置为-50px */
}
.title-image {
  max-width: 50%; /* 调整缩放比例，这里设置为50% */
  transform: scale(0.9); /* 调整缩放比例，这里设置为0.8 */
}
.decorations {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  z-index: 1;
  transform-style: preserve-3d; /* 添加此属性以保留3D变换效果 */
}

.decorations img {
  width: 120px; /* 调整图片的大小 */
  height: 120px;
  position: absolute;
  transform-origin: center center; /* 设置旋转的基点为中心 */
}

.top-left {
  top: 50px; /* 距离顶部的距离 */
  left: 50px; /* 距离左侧的距离 */
  transform: rotate(0deg); /* 将左上角图片旋转0度 */
}

.bottom-left {
  bottom: 50px; /* 距离底部的距离 */
  left: 50px;
  transform: rotate(-90deg); /* 将左下角图片旋转90度 */
}

.bottom-right {
  bottom: 50px;
  right: 50px; /* 距离右侧的距离 */
  transform: rotate(-180deg); /* 将右下角图片旋转180度 */
}

.top-right {
  top: 50px;
  right: 50px;
  transform: rotate(-270deg); /* 将右上角图片旋转270度 */
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.buttons {
  display: flex;
  justify-content: center;
  margin-top: 20px; /* 调整按钮与标题之间的距离 */
}

.buttons .button {
  margin: 0 10px; /* 调整按钮之间的间距 */
  width: 15%; /* 设置按钮宽度为20% */
  height: auto; /* 根据宽度自适应高度 */
}

.buttons .button:hover {
  background-image: url("../../public/zelda/button1-onclick.png");
}

.buttons .button:nth-child(2):hover {
  background-image: url("../../public/zelda/button2-onclick.png");
}

.buttons .button:nth-child(3):hover {
  background-image: url("../../public/zelda/button3-onclick.png");
}

.buttons .button:nth-child(4):hover {
  background-image: url("../../public/zelda/button4-onclick.png");
}
</style>
