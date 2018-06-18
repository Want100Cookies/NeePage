<template>
    <div class="translate">
        {{translateRandom()}}
    </div>
</template>

<script>
import { translate, langs } from 'google-translate-api';

export default {
  name: 'Translate',
  props: {
    text: {
      type: String,
      required: true,
    },
    lang: {
      type: String,
      required: true,
    },
  },
  methods: {
    translateRandom() {
      return translate(this.text, { to: this.lang }).then(res => res.text, err => err);
    },
  },
  langs,
};
</script>

