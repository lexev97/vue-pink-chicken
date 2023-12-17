<template>
  <section class="messenger">
    <header class="messenger__header">
      <div class="messenger__header-wrapper">
        <h2 class="messenger__heading">Личный помошник</h2>
        <div class="messenger__manager">
          <p class="messenger__manager-name">Jim Davidson</p>
          <p class="messenger__manager-email">Jim Davidson@adaurum.ru</p>
        </div>
      </div>
      <ShowProps />
    </header>
    <div class="messenger__messages-area">
      <div class="messenger__dialog">
        <div v-if="!dialogIsShown && !isLoading" class="messenger__no-messages">
          <img
            class="messenger__no-messages-pic"
            src="../../shared/assets/images/PNG/call-manager-pic.png"
            alt="Изображение оператора"
          />
          <p class="messenger__no-messages-text">
            Это чат с администратором. Ты можешь с ним пообщаться по любому
            вопросу о нашем сервисе и узнать о ходе работы
          </p>
        </div>
        <p v-if="isLoading" class="messenger__is-loading">Загрузка...</p>
        <ShowMessages v-if="dialogIsShown && !isLoading" />
      </div>
      <div class="messenger__textarea">
        <OrderDocs className="messenger__order-docs" @handle-show-docs-click="handleShowDocsClick"/>
        <div class="messenger__text-input-area">
          <textarea
            placeholder="Введите сообщение для администратора"
            class="messenger__text-input"
          ></textarea>
          <div class="messenger__add-to-message">
            <AddFileBtn className="messenger__add-file" />
            <AddImgBtn className="messenger__add-img" />
          </div>
        </div>
        <div class="messenger__send-area">
          <SendMessage
            className="messenger__send-button"
            @handle-show-message-click="handleShowMessageClick"
          />
          <p class="messenger__send-text">Enter</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ShowMessages } from '../../features/Messenger/ShowMessages';
import { ShowProps } from '@/features/Messenger/ShowProps';
import { OrderDocs } from '@/features/Messenger/OrderDocs';
import { SendMessage } from '@/features/Messenger/SendMessage';
import { AddFileBtn, AddImgBtn } from '@/shared/ui/buttons';

export default {
  data() {
    return {
      dialogIsShown: false,
      isLoading: false,
    };
  },
  name: 'TheMessenger',
  components: {
    AddFileBtn,
    AddImgBtn,
    SendMessage,
    OrderDocs,
    ShowProps,
    ShowMessages,
  },
  methods: {
    handleShowMessageClick() {
      this.isLoading =true
      setTimeout(()=> {
        this.isLoading =false
        this.dialogIsShown = true
      }, 1000)
    },
    handleShowDocsClick() {
      this.$emit('handle-show-message-click');
    }
  },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
