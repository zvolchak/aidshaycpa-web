<template lang="pug">
  #InfoBlock
    article.media.columns(
    )
      //- :style="{'background-image': 'url(' + require(`@/assets/${img_name}`) + ')', backgroundSize: 'cover',}"
      .media-content.column.is-6
        .content
          slot
      figure.media-right.column.is-6.is-hidden-mobile
        .image
          img(:src="require(`@/assets/${img_name}`)")
   
</template>

<script>
export default {
  name: 'InfoBlock',
  props: {
    img_name: {
      default: 'business.jpg',
      type: String,
    }
  }
}//default
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

  figure {
    // background: black;
    height: 100%;
    width: 100%;
    padding: 0rem;
  }

  .image {
    height: 100% !important;
    width: 100% !important;
    
  }

  img {
    height: 100% !important;
    width: 100% !important;
  }

  article, .media {
    height: 25rem !important;
    // background: green;
  }

  @media (min-width:320px)  { 
    figure {
      // position: absolute;
      // display: none;
      z-index: 0;
    }

    .media-content {
      z-index: 1;
      
    }

    .content {
      padding: 0.6rem;
    }

    article {
      // background: black;
    }

    .media {
      height: 28rem !important;
      
    }
  }
</style>
