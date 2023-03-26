<template>
  <v-card class="">
    <v-card-title class="ma-3 screen-back-color" width="100%">Language</v-card-title>
    <v-card-text>
      <v-row >
        <v-col class="pa-2  mt-5 mb-3 "  v-for="(lang, index) in languages" :key="index" cols="12" md="6" lg="4">
          <v-radio
            v-model="selectedLanguage"
            :value="lang.code"
            :label="lang.name"
          ></v-radio>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      languages: [
        { name: 'English', code: 'en' },
        { name: 'Français', code: 'fr' },
        { name: 'Español', code: 'es' },
        { name: 'Deutsch', code: 'de' },
        { name: 'Português', code: 'pt' },
        { name: 'Italiano', code: 'it' },
        { name: 'Русский', code: 'ru' },
        { name: '日本語', code: 'ja' },
        { name: '中文', code: 'zh' },
        { name: '한국어', code: 'ko' },
        { name: 'العربية', code: 'ar' },
        { name: 'Bahasa Indonesia', code: 'id' },
        { name: 'Nederlands', code: 'nl' },
        { name: 'Türkçe', code: 'tr' },

        { name: 'Slovenčina', code: 'sk' },
        { name: 'Română', code: 'ro' },
        { name: 'български', code: 'bg' },
        { name: 'Hrvatski', code: 'hr' },
        { name: 'Српски', code: 'sr' },
        { name: 'Українська', code: 'uk' },
      ],
      selectedLanguage: 'en',
    };
  },
};
</script>
