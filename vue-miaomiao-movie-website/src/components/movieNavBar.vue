<template>
  <div id="content">
    <div class="movie_menu">
      <router-link tag="div" to="/movie/city" class="city_name">
        <span>{{ $store.state.name }}</span
        ><i class="iconfont icon-lower-triangle"></i>
      </router-link>
      <div class="hot_swtich">
        <router-link tag="div" to="/movie/now" class="hot_item"
          >正在热映</router-link
        >
        <router-link tag="div" to="/movie/comming" class="hot_item"
          >即将上映</router-link
        >
      </div>
      <router-link tag="div" to="/movie/search" class="search_entry">
        <i class="iconfont icon-sousuo"></i>
      </router-link>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "movieNavBar",
  data() {
    return {
      name: "",
    };
  },
  computed: {},
  components: {},
  created() {},
  mounted() {},
  methods: {},
};
</script>
<style lang="scss" scoped>
#content {
  .movie_menu {
    width: 100%;
    height: 45px;
    border-bottom: 1px solid #e6e6e6;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: white;
    z-index: 10;
  }
}
.movie_menu {
  .city_name {
    margin-left: 20px;
    height: 100%;
    line-height: 45px;
  }
  .city_name {
    &.active {
      color: #ef4238;
      border-bottom: 2px #ef4238 solid;
    }
  }
  .hot_swtich {
    display: flex;
    height: 100%;
    line-height: 45px;
  }
  .hot_item {
    font-size: 15px;
    color: #666;
    width: 80px;
    text-align: center;
    margin: 0 12px;
    font-weight: 700;
  }
  .hot_item {
    &.active {
      color: #ef4238;
      border-bottom: 2px #ef4238 solid;
    }
  }
  .search_entry {
    margin-right: 20px;
    height: 100%;
    line-height: 45px;
    &.active {
      color: #ef4238;
      border-bottom: 2px #ef4238 solid;
    }
    i {
      font-size: 24px;
      color: red;
    }
  }
}
</style>
