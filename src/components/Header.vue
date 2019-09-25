<template lang="pug">
  #Header.header.columns.is-multiline(
    :style="{'background-image': 'url(' + require('@/assets/header_blur.png') + ')'}"
  )
    .column.is-12
      .columns.is-centered.is-multiline
        .column.is-5
          p.header-text.has-text-left
            | FOR ALL OF YOUR
            br
            | ACCOUNTING NEEDS
      .columns.is-centered.is-multiline
        .column.is-5
          p.subtext.has-text-justified {{subtext}}
</template>

<script>
import { headline_subtext } from '@/constants/text.js';

export default {
  name: 'Header',
  props: {
  },

  computed: {
    subtext() {
      return headline_subtext
    }
  }
}//default
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .header {
    // display: flex;
    align-items: center;
    min-height: 30rem;
    padding: 0rem;
  }

  .header-text {
    width: 100%;
    font-size: 3.4em;
    color: white;
    text-shadow: 0px 1px 5px rgba(0, 0, 0, 1);
    letter-spacing: 2px;
    word-spacing: 2px;
    padding-left: 0.5rem;
    padding-right: 1rem;
  }

  .subtext {
    width: 100%;
    text-shadow: 0px 1px 2px white;
    font-size: 1.2em;
    font-weight: bold;
    padding-left: 1rem;
    padding-right: 1rem;
  }

  @media (max-width: 1280px)  {
    .header-text {
      font-size: 2.3em;
    }
  }

  @media (max-width: 768px)  {
    .header {
      padding: 0.5rem;
    }

    .header-text {
      padding-top: 2rem;
      font-size: 1.7em;
      font-weight: bold;
    // text-shadow: 0px 0px 5px black;
    }

    .subtext {
      color: white !important;
      font-weight: normal !important;
      text-shadow: 0px 1px 3px black;
    }
  }
</style>
