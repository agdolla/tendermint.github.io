<template lang="pug">
page-split
  page-header(title='Community' subtitle='Join and contribute to the vibrant Cosmos & Tendermint community.' type='split' slot='header' theme="tendermint")
  ni-section
    div(slot="title") Discuss & Chat
    card-community(
      dt='Forum'
      dd='Read the latest developer updates and join community discussions.'
      icon='university'
      :anchor='links.cosmos.community.discourse')
    card-community(
      dt='Community Chat (Telegram)'
      dd='Join the `cosmosproject` group to join our community chat.'
      icon='telegram'
      :anchor='links.cosmos.community.telegram')
    card-community(
      dt='Developer Chat (Matrix)'
      dd='Join the #cosmos:matrix.org room to join our developer chat.'
      icon='comments-o'
      :anchor='links.cosmos.community.matrix')
    card-community(
      dt='IRC'
      dd='Join the #cosmos_network channel on the irc.freenode.net server.'
      icon='hashtag'
      :anchor='links.cosmos.community.irc')

  ni-section
    div(slot="title") Social Media
    card-community(
      dt='Twitter'
      dd='Follow @cosmos, our official Twitter account.'
      icon='twatter'
      :anchor='links.cosmos.community.twitter')
    card-community(
      dt='BitcoinTalk'
      dd='Keep up with updates on our thread in the BitcoinTalk forum.'
      icon='bitcoin'
      :anchor='links.cosmos.community.bitcointalk')
    card-community(
      dt='Facebook'
      dd='Like the `cosmosproject` page to get updates in your Facebook feed.'
      icon='footbook'
      :anchor='links.cosmos.community.facebook')
    card-community(
      dt='Reddit'
      dd='Subscribe to /r/cosmosnetwork to get news on your Reddit homepage.'
      icon='raddit'
      :anchor='links.cosmos.community.reddit')
  ni-section
    div(slot="title") Tendermint
    card-community(
      dt='Twitter'
      dd='Follow @tendermint_team, our official Twitter account.'
      icon='twatter'
      :anchor='links.tm.community.twitter')
    card-community(
      dt='Facebook'
      dd='Like the `tendermint` page to get updates in your Facebook feed.'
      icon='footbook'
      :anchor='links.tm.community.facebook')
    card-community(
      dt='LinkedIn'
      dd='View our official company profile on LinkedIn.'
      icon='linkedout'
      :anchor='links.tm.community.linkedin')
</template>

<script>
import {mapGetters} from 'vuex'
import CardCommunity from './CardCommunity'
import NiSection from './NiSection'
import PageHeader from '@nylira/vue-page-header'
import PageSplit from '@nylira/vue-page-split'
export default {
  name: 'page-community',
  components: {
    CardCommunity,
    NiSection,
    PageHeader,
    PageSplit
  },
  computed: {
    ...mapGetters(['links'])
  },
  mounted () {
    document.title = 'Community - Tendermint'
  }
}
</script>
