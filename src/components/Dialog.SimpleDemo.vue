<demo>简易开启Dialog</demo>

<template>
  <Button @click="showDialog">showDialog</Button>
</template>

<script lang="ts">
import Button from "../lib/Button.vue";
import { h } from "vue";
import { openDialog } from "../lib/openDialog";
export default {
  components: { Button },
  setup() {
    const showDialog = () => {
      openDialog({
        title: h("strong", {}, "标题"),
        content: "内容",
        Affirm: () => {},
        Cancel: () => {},
      });
    };
    return { showDialog };
  },
};
</script>