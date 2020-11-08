<template>
  <v-container fluid class="py-0 my-0 mt-0">
    <v-row class="py-0 my-0">
      <v-col md="9" sm="6" cols="12" class="py-0 my-0">
        <p
          class="google-font mb-1"
          style="font-size:110%"
        >Our events are open to newbies, developers, managers, and organizations who are interested in Google's technologies or use them as part of their projects.</p>
        <p class="google-font">{{data.shortDescription}}</p>
        <p class="google-font mt-5">Questions? Please contact <a style="color:#1565C0;text-decoration: none;" :href="`mailto:dscpdpu@gmail.com`">dscpdpu@gmail.com</a></p>
        <CommunitySocialInfo :config="config"  class="mb-2"/>
        <span v-for="(item,i) in hashtags" :key="i" >
          <v-chip
            class="mr-1 mb-1"
            :href="'https://twitter.com/hashtag/'+item.name"
            target="_blank"
            label
          >#{{item.name}}</v-chip>
        </span>
      </v-col>
      <v-col md="3" sm="6" cols="12" class="py-0 my-0">
        <img :src="require('@/assets/img/svg/contact.svg')" style="float:right" width="80%" alt />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// import SocialInfo from '@/components/common/SocialInfo'
import { mapState } from 'vuex'

export default {
  components:{
      CommunitySocialInfo : ()=>import('@/components/common/CommunitySocialInfo'),
    },
     data() {
    return {
      selectedProduct: null,
      hashtags: [
        {
          name: 'DSCPDPUchapter',
        },
        {
          name: 'DeveloperStudentClubs',
        },
        {
          name: 'StudentCommunity',
        },
      ],
    };
  },
    computed:{
      ...mapState(['config'])
    },
  props: ["data"],
};
</script>