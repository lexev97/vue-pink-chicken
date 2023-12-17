<template>
  <header class="header">
    <div class="header__wrapper">
      <div class="header__logo"></div>
      <div class="header__menu">
        <div class="header__user-wrapper">
          <div class="header__revenue-area">
            <span class="header__revenue-icon">
              <RevenueIcon />
            </span>
            <p class="header__revenue-text">5%<span> выручки</span></p>
          </div>
          <div class="header__user-area">
            <span class="header__user-icon">
              <UserIcon />
            </span>
            <h1 class="header__user-text">Username@adaurum.ru</h1>
          </div>
        </div>
        <div class="header__settings-wrapper">
          <SettingsBtn className="header__settings-btn"/>
          <LogoutBtn className="header__logout-btn"/>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { LogoutBtn, SettingsBtn } from '@/shared/ui/buttons';
import { RevenueIcon, UserIcon } from '@/shared/ui/icons';

export default {
  name: 'TheHeader',
  components: { RevenueIcon, UserIcon, LogoutBtn, SettingsBtn, },
};
</script>

<style lang="scss">
@import './styles.scss';
</style>
