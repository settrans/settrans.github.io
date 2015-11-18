---
layout: default
title: About
menu: true
permalink: /about/
---

{::options parse_block_html="true" /}
<script>
   $(document).ready(function($) {
      $('.page-content').closest('div.wrapper').removeClass('wrapper');
      $('.section').wrapInner('<div class="wrapper"></div>');
   });
</script>

<div class="section inbox">
<span class="playfair content-id lang-hide">{{ site.subtitle_id }} {{ site.title }}</span><span class="playfair content-en">{{ site.title }} {{ site.subtitle_en }}</span>

SetTrans adalah sebuah perusahaan kecil Indonesia di bidang jasa 
penerjemahan yang memiliki satu penerjemah utama (purna waktu) dan beberapa 
tambahan penerjemah (paruh waktu) jika diperlukan. Semua penerjemah 
memiliki sertifikat Penerjemah Teks Umum Bahasa Inggris ke Bahasa Indonesia 
dari [LBI FIB UI][lbi-fib-ui] dan telah mengerjakan beberapa 
[proyek penerjemahan][portfolio] secara subkontrak.
{: class="content-id lang-hide normal" style="text-align: justify;"}
SetTrans is a small Indonesian translation service company comprising of one
 main (full-time) translator and several on-demand (part-time) translators. 
All translators have earned certificates for English to Indonesian 
General Text Translator from [Lembaga Bahasa Internasional FIB Universitas 
Indonesia][lbi-fib-ui] and completed a couple of subcontracted 
[translation projects][portfolio]. 
{: class="content-en normal" style="text-align: justify;"}
</div>


[lbi-fib-ui]: http://lbifib.ui.ac.id/ "LBI FIB UI" 
[portfolio]: {{ base_url }}/portfolio/ "Translation Projects"
