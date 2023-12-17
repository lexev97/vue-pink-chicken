<template>
  <div class="file-manager__docs show-docs">
    <h3 class="show-docs__heading">{{ heading + 'ы' }}</h3>
    <ul class="show-docs__docs-list">
      <li>
        <div class="show-docs__list-item">
          <div class="show-docs__doc-name">
            <DocIcon />
            <p>Companyname 11/23</p>
          </div>
          <button
            type="button"
            class="show-docs__doc-btn"
            :style="{ backgroundColor: isLoading ? '#949494' : '#F4D4ED' }"
          >
            <DownloadIcon v-if="!isLoading" />
            <LoadingIcon v-if="isLoading" />
          </button>
        </div>
        <span v-if="!isLoading"
          ><DoneIcon /> {{ heading }} от 1.06.22 готов</span
        >
        <span v-if="isLoading"
          ><AttentionIcon /> {{ heading }} в процессе составления</span
        >
      </li>
      <li>
        <div class="show-docs__list-item">
          <div class="show-docs__doc-name">
            <DocIcon />
            <p>Companyname 10/23</p>
          </div>
          <button
            type="button"
            class="show-docs__doc-btn"
            :style="{ backgroundColor: '#F4D4ED' }"
          >
            <DownloadIcon />
          </button>
        </div>
      </li>
      <li>
        <div class="show-docs__list-item">
          <div class="show-docs__doc-name">
            <DocIcon />
            <p>Companyname 9/23</p>
          </div>
          <button
            type="button"
            class="show-docs__doc-btn"
            :style="{ backgroundColor: '#F4D4ED' }"
          >
            <DownloadIcon />
          </button>
        </div>
      </li>
      <li v-if="heading === 'Медиаплан'">
        <div class="show-docs__list-item">
          <div class="show-docs__doc-name">
            <DocIcon />
            <p>Companyname 8/23</p>
          </div>
          <button
            type="button"
            class="show-docs__doc-btn"
            :style="{ backgroundColor: '#F4D4ED' }"
          >
            <DownloadIcon />
          </button>
        </div>
      </li>
    </ul>
    <button type="button" class="show-docs__more">Показать еще</button>
  </div>
</template>

<script>
import {
  DocIcon,
  DownloadIcon,
  LoadingIcon,
  DoneIcon,
  AttentionIcon,
} from '@/shared/ui/icons';

export default {
  name: 'ShowDocs',
  props: {
    heading: String,
    isLoading: Boolean,
  },
  components: { DocIcon, DownloadIcon, LoadingIcon, DoneIcon, AttentionIcon },
};
</script>

<Style lang="scss">
@import './styles.scss';
</Style>
