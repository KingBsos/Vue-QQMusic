<template>
  <div>
    <div class="container">
      <div class="wrap pB-1R">
        <h1>我喜欢</h1>
        <ul class="menu">
          <li class="mR-1R">
            <router-link class="link" to="/index/ilike/song">歌曲{{ 208 }}</router-link>
          </li>
          <li class="mL-1R mR-1R">
            <router-link class="link" to="/index/ilike/songsheet">歌单{{ 0 }}</router-link>
          </li>
          <li class="mL-1R mR-1R">
            <router-link class="link" to="/index/ilike/album">专辑{{ 0 }}</router-link>
          </li>
          <li class="mL-1R mR-1R">
            <router-link class="link" to="/index/ilike/anchorstation">主播电台{{ 0 }}</router-link>
          </li>
          <li class="mL-1R">
            <router-link class="link" to="/index/ilike/video">视频{{ 0 }}</router-link>
          </li>
        </ul>
        <div class="w-100 o-a mt_5rem">
          <button class="custom-btn btn-primary mR-1R VA-M">
            <span class="iconfont icon-play"></span> 播放全部
          </button>
          <button class="custom-btn mR-1R VA-M">
            <span class="iconfont icon-xiazai"></span> 下载
          </button>
          <button class="custom-btn VA-M">
            <span class="iconfont icon-liebiao"></span> 批量操作
          </button>
        </div>
      </div>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  padding-top: 10px;
}
.wrap {
  width: 100%;
  position: sticky;
  top: -50px;
  background-color: #fff;
  z-index: 1;
  white-space: nowrap;
}
.custom-btn {
  padding: 4px 20px;
  border: 0px;
  border-radius: 50px;
  font-size: 16px;
  font-weight: 600;
  .iconfont {
    font-size: 20px;
  }
}
.btn-primary {
  color: #fff;
  background-color: var(--color2);
}
.custom-btn:hover {
  box-shadow: 0 0 0px 500px rgba(0, 0, 0, 0.031) inset;
}
.menu {
  display: flex;
  width: 100%;
  overflow: auto;
}
.link {
  display: inline-block;
  padding: 5px;
  color: #333;
  border: 3px solid transparent;
}
.router-link-active {
  color: var(--color2);
  position: relative;
}
.router-link-active:after {
  content: '';
  position: absolute;
  width: 35%;
  border-bottom: 3px solid var(--color2);
  left: 50%;
  top: 100%;
  transform: translate(-50%, -3px);
}
@media screen and (max-width: 400px) {
  .container {
    padding: 3px;
  }
}
</style>