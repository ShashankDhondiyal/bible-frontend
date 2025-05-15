<script setup lang="ts">
import { HomeOutlined } from '@ant-design/icons-vue';
import { Layout } from 'ant-design-vue';
const { Header, Footer } = Layout;
</script>

<template>
  <Layout class="layout">
    <Header class="header">
      <router-link to="/">
        <a-button size="large" shape="round" class="home-button"><HomeOutlined /></a-button>
      </router-link>
    </Header>
    <router-view class="content"></router-view>
    <Footer class="footer"></Footer>
  </Layout>
</template>

<style scoped>
.layout {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
}
.header {
  text-align: center;
  color: var(--color-text);
  height: 64px;
  padding-inline: 50px;
  line-height: 64px;
  background-color: var(--color-background-soft);
}
.content {
  text-align: center;
  flex: 1 1 auto;
  color: var(--color-text);
  background-color: var(--color-background-mute);
  display: flex;
  align-items: center;
  justify-content: center;
}
.footer {
  text-align: center;
  color: var(--color-text);
  background-color: var(--color-background-soft);
}

:global(*) {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:global(body), :global(html) {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  overflow: hidden;
}

:global(#app) {
  margin-left: 0;
  padding-left: 0;
}

:deep(.ant-layout) {
  margin-left: 0;
  padding-left: 0;
}

.home-button {
  color: var(--color-text);
  background-color: var(--color-background-soft);
  border-color: var(--color-border);
}
.home-button:hover {
  color: var(--color-text);
  background-color: var(--color-border-hover);
  border-color: var(--color-border-hover);
}
</style>
