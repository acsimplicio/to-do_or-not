<template>
  <div class="page-wrapper">
    <header class="main-header">
      <div class="header-logo">
        <img 
          src="/logo/logo.png" 
          alt="Logo To-Do or not To-Do?">
      </div>
      <nav class="header-menu">
        <router-link 
          :to="{ name: 'about' }"
          class="link">
          Sobre esta aplicação
        </router-link>
        <router-link 
          :to="{ name: 'index' }"
          class="link">
          To-Do or not To-Do?
        </router-link>
      </nav>
    </header>
    <nuxt/>
  </div>
</template>

<style>

  /* reset.css*/
  /* http://meyerweb.com/eric/tools/css/reset/ 
    v2.0 | 20110126
    License: none (public domain)
  */

  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed, 
  figure, figcaption, footer, header, hgroup, 
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure, 
  footer, header, hgroup, menu, nav, section {
    display: block;
  }
  body {
    line-height: 1;
  }
  ol, ul {
    list-style: none;
  }
  blockquote, q {
    quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
    content: '';
    content: none;
  }
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }
  /* reset.css end */

  @font-face {
    font-display: fallback;
    font-family: 'Roboto Condensed';
    font-weight: 300;
    font-style: normal;
    src: url('../assets/RobotoCondensed-Regular.ttf') format("truetype");
  }

  html {
    height: 100%;
    font-family: 'Roboto Condensed', sans-serif;
  }

  body {
    margin: 0;
  }

  .page-wrapper {
    height: 100vh;
  }

  .main-header {
    background-color: #e65a2f;
    height: 60px;
    padding: 10px 25px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .header-menu {
    margin-right: 50px;
  }

  .header-menu .link {
    color: white;
    text-decoration: none;
    position: relative;
    margin-left: 20px;
    font-size: 16px;
  }

  .header-menu .link::after{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
    width: 0%;
    content: ".";
    color: transparent;
    transition: .5s;
    background-color: white;
    height: 1px;
  }

  .header-menu .link:hover::after {
    width: 100%;
  }

  .header-logo, .header-logo img {
    height: 100%;
  }

</style>
