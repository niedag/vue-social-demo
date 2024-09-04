<template>
  <s-twitter
    :window-features="windowFeatures"
    :share-options="shareOptions"
    :use-native-behavior="useNativeBehavior"
    @popup-close="onClose"
    @popup-open="onOpen"
    @popup-block="onBlock"
    @popup-focus="onFocus"
  >
    <!-- your icon component -->
  <a>Click me to send a Twitter post</a>
  </s-twitter>
</template>

<script>
  import { STwitter } from 'vue-socials'

  export default {
    name: 'STwitterSharing',
    
    components: { STwitter },
    
    data() {
      return {
        windowFeatures: {},
        shareOptions: {
          url: 'https://github.com/',
          text: 'Hello world',
          hashtags: ['hash', 'tag'],
          via: 'twitterdev',
        },
        useNativeBehavior: false,
      }
    },
    
    methods: {
      onClose() {},
      onOpen() {},
      onBlock() {},
      onFocus() {},
    }
  };
</script>