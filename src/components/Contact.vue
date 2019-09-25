<template lang="pug">
  #Contact
    article.media
      .media-content
        .content.columns.is-multiline.is-centered.has-text-centered
          .column.is-1.profile-picture-container.is-desktop
            figure.image.profile-picture
              img(src='@/assets/aida.jpg')
          .column
            .column.is-12.headline.margin-top-3
              p CONTACTS
            .column.is-12.margin-top-2
              a(href='https://apps.colorado.gov/dora/licensing/Lookup/PrintLicenseDetails.aspx?cred=1262357&contact=1364775') Aida's Colorado CPA license
            .column.is-12.margin-top-2
              p 1199 S Waco St Unit B
              p Aurora, Co 80017
              p USA
            .column.is-12.margin-top-1
              p shaymardanova.aida@gmail.com
            .column.is-12.margin-top-1
              a(href="tel:970-470-991") 970-470-991   
            .column.is-12.margin-top-2
          .column.is-1.profile-picture-container.is-mobile
            figure.image.profile-picture
              img(src='@/assets/aida.jpg')
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

  .profile-picture {
    background: black;
    height: 100%;
    width: 100%;
    padding: 0rem;
    height: 16rem;
    width: 14rem;
  }

  .profile-picture > img {
    height: 100% !important;
    width: 100% !important;
  }

  .profile-picture-container {
    padding-top: 10%; 
  }

  article, .media {
    // height: 25rem !important;
    background: #e0ebeb;
  }

  .headline {
    letter-spacing: 4px;
    font-size: 1.3em;
  }

  .is-mobile {
    display: none;
  }

  @media (max-device-width: 768px)  { 
    .profile-picture {
      // margin-left: 10%; 
    }

    .profile-picture-container {
      padding-left: 15%;
    }

    .is-desktop {
      display: none !important;
    }

    .is-mobile {
      display: block;
    }
  }
</style>
