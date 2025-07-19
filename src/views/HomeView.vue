<template>
  <div class="index-page">
    <!-- 搜索框 -->
    <a-input-search
      v-model:value="value"
      placeholder="input search text"
      enter-button="Search"
      size="large"
      @search="onSearch"
    />
    <my-divder />
    <!-- tap栏 -->
    <a-tabs v-model:activeKey="activeKey">
      <a-tab-pane key="1" tab="用户">
        <UserList />
      </a-tab-pane>
      <a-tab-pane key="2" tab="文章" force-render>
        <PostList />
      </a-tab-pane>
      <a-tab-pane key="3" tab="图片">
        <PictureList />
      </a-tab-pane>
    </a-tabs>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import UserList from "@/components/UserList.vue";
import PostList from "@/components/PostList.vue";
import PictureList from "@/components/PictureList.vue";
import MyDivder from "@/components/MyDivder.vue";

const value = ref<string>("");
const onSearch = (searchValue: string) => {
  console.log("use value", searchValue);
  console.log("or use this.value", value.value);
};
// tap
const activeKey = ref("1");
</script>
