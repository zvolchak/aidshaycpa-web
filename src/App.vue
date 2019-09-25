<template lang="pug">
  #App
    .columns
      .column.is-12
        Header

    .columns.is-centered
      .column.is-5.has-text-centered.margin-top-5
        strong.services SERVICES
        
    .columns.is-centered.margin-top-4
      .column.is-10
        InfoBlock(img_name="handshake.jpg")
          .columns.margin-top-3.is-multiline.is-centered
            .column.is-9.service-headline
              p.has-text-left CORPORATE FORMATION - LLC/S CORP
            .column.is-9.services-body.margin-top-1
              p.has-text-justified.text-bg
                | Consultation on the available 
                | options of business types and identifying one that
                | fits best for you. Forming corporate documents, obtaining
                | Fed Tax ID, Colorado Filing.
              
              p.text-bg $200

    .columns.is-centered.margin-top-3
      .column.is-10
        InfoBlock(img_name="virt_accounting.jpg")
          .columns.margin-top-3.is-multiline.is-centered
            .column.is-9.service-headline
              p.has-text-left VIRTUAL ACCOUNTING/BOOKKEEPING
            .column.is-9.services-body.margin-top-1
              p.has-text-justified
                | Producing monthly financial records and generating
                | statements about financial position and results 
                | of operations of the company in accordance with 
                | General Accepted Accounting Principles (US GAAP).

              p $200 / month


    .columns.is-centered.margin-top-3
      .column.is-10
        InfoBlock(img_name="business.jpg")
          .columns.margin-top-1.is-multiline.is-centered
            .column.is-9.service-headline
              p.has-text-left TAX PLANNING AND ERTURN PREPARATION
            .column.is-9.services-body.margin-top-1
              p.has-text-justified
                | Estimated tax calculation and EFT account set up.
                br
                | Small Business and Individual Tax Preparation.

            .column.is-9.services-body(style="font-size: 1em;")
              p 1040 - $350 (included schedule D, E)
                br
                | Schedule C - $150
                br
                | Schedule 1065 - $250
                br
                | Schedule 1120 - $250
                br
                | Schedule 1120S - $250

    .columns.is-centered.margin-top-3
      .column.is-10
        InfoBlock(img_name="coins.jpg")
          .columns.margin-top-3.is-multiline.is-centered
            .column.is-9.service-headline
              p.has-text-left ACCOUNTING PACKAGE
            .column.is-9.services-body.margin-top-1
              p.has-text-justified
                | Monthly package includes bookkeeping, quarterly 
                | financial statements generation, estimated taxes 
                | calculation, payroll tax calculation, with
                | <b>free tax return at the end of the year.</b>

              p $260 / month

    .margin-top-5
    .columns.is-centered
      .column.is-12-mobile.is-8-desktop
        Contact

    .margin-top-5

</template>

<script>
import InfoBlock from '@/components/InfoBlock'
import Header from '@/components/Header'
import Contact from '@/components/Contact'
import * as TextEntries from '@/constants/text.js'


export default {
  name: 'app',
  components: {
    Header,
    InfoBlock,
    Contact
  },//components

  computed: {
    entries() {
      return [
        TextEntries.service_corp_formation,
        TextEntries.service_virtual_accounting,
        TextEntries.service_taxes,
        TextEntries.service_accounting,
        TextEntries.contacts
      ]
    }
  }
}
</script>

<style lang='scss'>

  @import "bulma";
  @import "@/styles/positionings.scss";

  $headline-color: #00e6e6;

  .services {
    font-size: 1.5em;
    color: $headline-color;
    letter-spacing: 2px;
  }

  .service-headline {
    font-size: 1.4em;
    color: $headline-color;
  }

  .services-body {
    font-size: 1.15em;
    letter-spacing: 1px;
  }

  .text-bg {
    // background: gray;
  }

  @media (min-width:320px)  { 
    .service-headline {
      text-shadow: 0px 0px 1px rgb(0, 0, 0);
    }

    .services-body {
      color: white;
      text-shadow: 0px 0px 10px rgb(0, 0, 0);
    }
  }
</style>
