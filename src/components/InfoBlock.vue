<template lang="pug">
  #InfoBlock
    article.media.columns(
      :style="{'background-image': useBlurImg(img_name), backgroundSize: 'cover',}"
    )
      //- :style="{'background-image': 'url(' + require(`@/assets/${useBlurImg(img_name)}`) + ')', backgroundSize: 'cover',}"
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
  },//props


  methods: {
    useBlurImg(imgName) {
      var split = imgName.split('.')
      if (split.length !== 2) //expecting img_name.jpg format
        return ''

      split[0] = split[0] + '_blur'
      var newImgName = split.join('.')
      if (screen.width > 768)
        return ''

      return 'url(' + require(`@/assets/${newImgName}`) + ')'
    }
  },//methods
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
      z-index: 0;
    }

    .media-content {
      z-index: 1;

    }

    .media {
      height: 28rem !important;

    }
  }
</style>
