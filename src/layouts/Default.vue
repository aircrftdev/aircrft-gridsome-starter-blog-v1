<template>
  <div id="app">

    <header class="header">
      <div class="header__left">
        <Logo v-if="showLogo" /> 
      </div>
      
      <div class="header__right">        
        <ToggleTheme />
      </div>
    </header>

    <main class="main">
      <slot/>
    </main>

    <footer class="footer">
      <span class="footer__copyright">Copyright © {{ new Date().getFullYear() }}. </span>
      <span class="footer__links">Empowered by Aircrft | Startup Marketplace 🍀 <a href="//aircrft.com"> </a></span>
      <span class="footer__links">Positive Impact Technology Platform <a href="//aircrft.com"> </a></span>
      <span class="footer__links">Aircrft is a act ❤️ <a href="//aircrft.com"> </a></span>
      <span class="footer__links">Blog <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">TV <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Community <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Content <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Code <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Captains & Crew <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Contribute <a href="//blog.aircrft.com"></a>Join as Curator / Code Captain</span>
      <span class="footer__links">Support <a href="//blog.aircrft.com"></a>Join our weekly Live Global Support Video Call</span>
      <span class="footer__links">Aircrft Impact Filters <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Abundance Algorithm <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Podcast <a href="//blog.aircrft.com"></a></span>
      <span class="footer__links">Moonshot Mindset <a href="//blog.aircrft.com"></a></span>
    </footer>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import ToggleTheme from '~/components/ToggleTheme.vue'

export default {
  props: {
    showLogo: { default: true }
  },
  components: {
    Logo,
    ToggleTheme
  }
}
</script>

<style lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: var(--header-height);
  padding: 0 calc(var(--space) / 2);
  top:0;
  z-index: 10;

  &__left,
  &__right {
    display: flex;
    align-items: center;
  }

  @media screen and (min-width: 1300px) {
    //Make header sticky for large screens
    position: sticky;
    width: 100%;
  }
}

.main {
  margin: 0 auto;
  padding: 1.5vw 15px 0;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: calc(var(--space) / 2);
  text-align: center;
  font-size: .8em;

  > span {
    margin: 0 .35em;
  }

  a {
    color: currentColor;
  }
}
</style>
