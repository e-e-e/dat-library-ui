<template>
  <div>
    <h2 id="sourcecode">Source Code Views</h2>
    <p>Pick a file to view</p>
    <div class="mw6 relative">
      <lib-select v-model='selection'>
        <lib-option v-for="(choice, index) in choices" :key="choice.value" :value="index" :label="choice.label" />
      </lib-select>
    </div>
    <lib-source-code language="html" :code="selectedCode"/>
  </div>
</template>

<script>
  export default {
    name: 'SourceCodeViews',
    created() {},
    data() {
      return {
        selection: 0,
        choices: [{
          value: '1',
          label: 'Ashis Nandy',
          code: `
<?xml version='1.0' encoding='utf-8'?>
<package xmlns="http://www.idpf.org/2007/opf" unique-identifier="uuid_id" version="2.0">
  <metadata xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:opf="http://www.idpf.org/2007/opf">
    <dc:identifier opf:scheme="calibre" id="calibre_id">85</dc:identifier>
    <dc:identifier opf:scheme="uuid" id="uuid_id">685360ab-1456-4600-ba36-c2b7c569bab3</dc:identifier>
    <dc:title>The Intimate Enemy: Loss and Recovery of Self Under Colonialism</dc:title>
    <dc:creator opf:file-as="Nandy, Ashis, , ," opf:role="aut">Ashis Nandy</dc:creator>
    <dc:contributor opf:file-as="calibre" opf:role="bkp">calibre (2.47.0) [http://calibre-ebook.com]</dc:contributor>
    <dc:date>2016-07-03T11:56:35+00:00</dc:date>
    <dc:description>Political, economic, and cultural domination under colonialism has repeatedly been studied during the last hundred years. Breaking with the tradition, Ashis Nandy explores the ways in which colonialism damaged the colonizing societies themselves, and how the likes of Gandhi resisted their rulers in British India by building on the lifestyle, values, and psychology of ordinary Indians and by heeding dissenting voices from the West.</dc:description>
    <dc:identifier opf:scheme="ARG">52176449307888af0a00022d.1</dc:identifier>
    <dc:language>en</dc:language>
    <meta content="{&quot;Ashis Nandy&quot;: &quot;&quot;}" name="calibre:author_link_map"/>
    <meta content="2016-07-03T11:57:12.806224+00:00" name="calibre:timestamp"/>
    <meta content="Intimate Enemy: Loss and Recovery of Self Under Colonialism, The" name="calibre:title_sort"/>
  </metadata>
  <guide>
      <reference href="cover.jpg" title="Cover" type="cover"/>
  </guide>
</package>` }, {
          value: '2',
          label: 'Empty',
          code: `
<?xml version='1.0' encoding='utf-8'?>
<package xmlns="http://www.idpf.org/2007/opf" unique-identifier="uuid_id" version="2.0">
  Nothing to see here
</package>` }],
      };
    },
    computed: {
      selectedCode() {
        const choice = this.choices[this.selection];
        return choice ? choice.code : '';
      },
    },
    methods: {},
  };
</script>
