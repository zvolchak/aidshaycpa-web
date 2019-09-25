<template lang="pug">
  #Header.header.columns.is-multiline(
    :style="{'background-image': 'url(' + require('@/assets/header.jpg') + ')'}"
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
    width: 100%;
    min-height: 30rem;
  }

  .header-text {
    width: 100%;
    font-size: 3.4em;
    color: white;
    text-shadow: 0px 0px 2px rgba(0, 0, 0, 1);
    letter-spacing: 2px;
    word-spacing: 2px;
  }

  .subtext {
    width: 100%;
    // color: white;
    text-shadow: 0px 0px 3px rgba(255,255,255, 1);
    font-size: 1.2em;
  }

  @media (min-width:320px)  { 
    .header {
      padding: 0.5rem;
    }

    .header-text {
      font-size: 1.7em;
      font-weight: bold;
    }

    .subtext {
      color: white;
      text-shadow: 0px 0px 1px rgb(134, 134, 134);
    }
  }
</style>
