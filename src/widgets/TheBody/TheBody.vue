<template>
  <main class="main">
    <FileManager :docIsLoading="isLoading" :docsIsShow="docsIsShow" />
    <TheMessenger @handle-show-message-click="handleShowDocsClick" />
  </main>
</template>

<script>
import FileManager from '@/widgets/FileManager/FileManager.vue';
import TheMessenger from '@/widgets/TheMessenger/TheMessenger.vue';

export default {
  name: 'TheBody',
  data() {
    return {
      isLoading: false,
      docsIsShow: false,
    };
  },
  components: { FileManager, TheMessenger },
  methods: {
    handleShowDocsClick() {
      this.isLoading = true;
      this.docsIsShow = true;
      setTimeout(() => {
        this.isLoading = false;
      }, 2000);
    },
  },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
