<template>
  <el-scrollbar>
    <main class="main">
      <div class="v-content">
        <div class="content-nav">
          <div class="nav-leval1">
            <span
              :class="item.isActive ? 'nav-list is-active' : 'nav-list'"
              v-for="item in navList"
              >{{ item.nav }}</span
            >
          </div>
          <div class="nav-leval2">
            <div>
              <span class="nav-title" v-for="item in navList2.nav">{{
                item.title
              }}</span>
            </div>
            <div class="nav-tool nav-title">{{ navList2.tool }}</div>
          </div>
          <div class="v-list" v-for="list in contentList">
            <div class="avatar">
              <el-avatar shape="square" :size="45" :src="list.avatar" />
            </div>
            <div class="list-content">
              <div class="title">{{ list.title }}</div>
              <span class="nav">{{ list.nav }}</span>
              <span class="user"> {{ list.user }}</span>
              <span class="last"> {{ list.last }}</span>
            </div>
            <div>
              <el-tag class="list-number" type="info" round>
                {{ list.number }}
              </el-tag>
            </div>
          </div>
        </div>
      </div>
      <div class="v-tools">right</div>
    </main>
  </el-scrollbar>
</template>
<script setup lang="ts">
import { ref } from "vue"

const navList = ref([
  {
    nav: "技术",
    id: "1",
    isActive: true,
    children: { nav: [{ title: "test", id: "1" }], tool: "test1" },
  },
  {
    nav: "创意",
    id: "2",
    isActive: false,
    children: { nav: [{ title: "test", id: "2" }], tool: "test1" },
  },
  {
    nav: "好玩",
    id: "3",
    isActive: false,
    children: { nav: [{ title: "test", id: "3" }], tool: "test1" },
  },
  {
    nav: "Apple",
    id: "4",
    isActive: false,
    children: { nav: [{ title: "test", id: "4" }], tool: "test1" },
  },
  {
    nav: "酷工作",
    id: "5",
    isActive: false,
    children: { nav: [{ title: "test", id: "5" }], tool: "test1" },
  },
  {
    nav: "交易",
    id: "6",
    isActive: false,
    children: { nav: [{ title: "test", id: "6" }], tool: "test1" },
  },
  {
    nav: "城市",
    id: "7",
    isActive: false,
    children: { nav: [{ title: "test", id: "7" }], tool: "test1" },
  },
  {
    nav: "问与答",
    id: "8",
    isActive: false,
    children: { nav: [{ title: "test", id: "8" }], tool: "test1" },
  },
  {
    nav: "最热",
    id: "9",
    isActive: false,
    children: { nav: [{ title: "test", id: "9" }], tool: "test1" },
  },
  {
    nav: "全部",
    id: "10",
    isActive: false,
    children: { nav: [{ title: "test", id: "10" }], tool: "test1" },
  },
  {
    nav: "R2",
    id: "11",
    isActive: false,
    children: { nav: [{ title: "test", id: "11" }], tool: "test1" },
  },
  {
    nav: "VXNA",
    id: "12",
    isActive: false,
    children: { nav: [{ title: "test", id: "12" }], tool: "test1" },
  },
  {
    nav: "节点",
    id: "13",
    isActive: false,
    children: { nav: [{ title: "test", id: "13" }], tool: "test1" },
  },
  {
    nav: "关注",
    id: "14",
    isActive: false,
    children: { nav: [{ title: "test", id: "14" }], tool: "test1" },
  },
])
const navList2 = ref({ nav: [{ title: "test", id: "1" }], tool: "test1" })

const contentList = ref([
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
  {
    avatar: "",
    user: "lpf0309",
    title: "微信通话总是显示信号不好，怎么定位光猫、网线、路由器的问题？",
    nav: "宽带症候群",
    time: "44 分钟前",
    last: "最后回复来自 wolffcat",
    number: "999",
  },
])
</script>

<style lang="scss" scoped>
.main {
  width: 1200px;
  margin: 0 auto;
  margin-top: 20px;
  display: flex;
  padding-bottom: 50px;
  .v-content {
    flex: 1;
    margin-right: 20px;
    .content-nav {
      .nav-leval1 {
        padding: 10px;
        border-top-left-radius: 3px;
        border-top-right-radius: 3px;
        background: #fff;
        .nav-list {
          padding: 4px 8px;
          margin-right: 4px;
          border-radius: 4px;
          line-height: 25px;
          cursor: pointer;
          &:hover {
            background: #f2f2f2;
          }
          &.is-active {
            background: #334;
            color: #fff;
          }
        }
      }
      .nav-leval2 {
        background: #f9f9f9;
        padding: 6px 10px;
        border-bottom: 1px solid #e2e2e2;
        display: flex;
        justify-content: space-between;
        .nav-title {
          padding: 4px 8px;
          line-height: 25px;
          cursor: pointer;
          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
  .v-list {
    display: flex;
    align-items: center;
    background: #fff;
    padding: 10px;
    .list-content {
      flex: 1;
      padding: 0 10px;
      .title {
        &:hover {
          text-decoration: underline;
          cursor: pointer;
        }
      }
      .nav {
        font-size: 12px;
        margin-right: 15px;
        color: #ccc;
        cursor: pointer;
      }
      .user {
        font-size: 12px;
        margin-right: 15px;
        color: #ccc;
        cursor: pointer;
      }
      .last {
        font-size: 12px;
        color: #ccc;
        cursor: pointer;
      }
    }
    .list-number {
      cursor: pointer;
      &:hover {
        background: #eee;
      }
    }
  }
  .v-tools {
    width: 280px;
  }
}
</style>
