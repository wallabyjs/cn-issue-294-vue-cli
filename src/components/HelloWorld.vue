<template>
  <div class="chrome-browser active">
      <div v-if="chromeTab" class="chrome-tabs">
          <div class="chrome-tab">
              <slot name="chrome-tab">
                  <img v-if="chromeTab.image" :src="chromeTab.image" class="chrome-tab-icon">
              </slot>
              <span class="chrome-tab-name">{{ chromeTab.name }}</span>
          </div>
      </div>
      <div class="chrome-header">
        <!-- Irrelevant svg html -->
      </div>
      <div class="chrome-body">
          <div class="chrome-viewport" :class="{ 'clean-viewport': cleanPreview }">
              <slot name="chrome-content"></slot>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'ChromePreview',
  props: {
      chromeTab: Object, // { image: String, name: String}
      cleanPreview: {
          type: Boolean,
          default: false,
      },
  },
  data() {
      return {
          url: ""
      };
  },
  mounted() {
    console.log("mounted");  
    fetch("https://google.com").then(() => console.log(":)")); // ADDING THIS LINE CAUSES THE ISSUE
  },
}
</script>
