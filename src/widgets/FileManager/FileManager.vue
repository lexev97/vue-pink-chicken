<template>
  <section class="file-manager">
    <h2 class="file-manager__heading">Файлы</h2>
    <div v-if="!docsIsShow" class="file-manager__nofiles">
      <img
        class="file-manager__nofiles-pic"
        src="../../shared/assets/images/PNG/order-docs-image.png"
        alt="Документов нет"
      />
      <p class="file-manager__nofiles-text">
        Закажи у личного помощника медиаплан. Он появится в этом разделе
      </p>
    </div>
    <div v-if="docsIsShow" class="file-manager__files">
      <ShowDocs heading="Медиаплан" :isLoading="docIsLoading" />
      <ShowDocs heading="Отчет" :isLoading="docIsLoading" />
    </div>
  </section>
  <section class="file-manager-small">
    <span
      class="file-manager-small__media"
      :style="{
        backgroundColor: docsIsShow && '#fff',
        border: docsIsShow && '1px solid #EE26C2',
      }"
      >Медиапланы <DoneIcon v-if="!docIsLoading && docsIsShow" />
      <AttentionIcon v-if="docIsLoading && docsIsShow"
    /></span>
    <span
      class="file-manager-small__reports"
      :style="{
        backgroundColor: docsIsShow && '#fff',
        border: docsIsShow && '1px solid #2676EE',
      }"
      >Отчеты
    </span>
  </section>
</template>

<script>
import { AttentionIcon, DoneIcon } from '@/shared/ui/icons';
import { ShowDocs } from '@/features/FileManager/ShowMediaplans';

export default {
  name: 'FileManager',
  props: {
    docsIsShow: Boolean,
    docIsLoading: Boolean,
  },
  components: { ShowDocs, AttentionIcon, DoneIcon },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
