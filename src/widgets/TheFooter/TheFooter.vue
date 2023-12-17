<template>
  <footer class="footer">
    <div class="footer__wrapper">
      <div class="footer__logo-area">
        <div class="footer__logo"></div>
        <a href="#" class="footer__priv-policy link"
          >Политика конфиденциальности</a
        >
      </div>
      <div class="footer__menu">
        <div class="footer__mailto-area">
          <MailIcon />
          <p class="footer__mailto-text">pinkchicken@adaurum.ru</p>
        </div>
        <div class="footer__lang-area">
          <GlobeIcon />
          <ul class="footer__lang-list">
            <li
              @click="choseLang('RU')"
              class="footer__lang"
              :class="lang === 'RU' ? 'footer__lang_selected' : ''"
            >
              RU
            </li>
            <li
              @click="choseLang('EN')"
              class="footer__lang"
              :class="lang === 'EN' ? 'footer__lang_selected' : ''"
            >
              EN
            </li>
            <li
              @click="choseLang('TUR')"
              class="footer__lang"
              :class="lang === 'TUR' ? 'footer__lang_selected' : ''"
            >
              TUR
            </li>
          </ul>
        </div>
        <ul class="footer__social-links">
          <li>
            <a
              href="#"
              class="footer__social-link footer__social-link_telegram"
            ></a>
          </li>
          <li>
            <a
              href="#"
              class="footer__social-link footer__social-link_whatsup"
            ></a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import { GlobeIcon, MailIcon } from '@/shared/ui/icons';

export default {
  data() {
    return {
      lang: 'RU',
    };
  },
  name: 'TheFooter',
  components: { MailIcon, GlobeIcon },
  methods: {
    choseLang(lang) {
      this.lang = lang;
    },
  },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
