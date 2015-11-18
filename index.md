---
layout: default
---

{::options parse_block_html="true" /}
<script>
   $(document).ready(function(){
      function checkWidth() {
         if ($(window).width < 600) {
            $('.section > .wrapper').removeClass('wrapper');
         }
      }
      $('.page-content').closest('div.wrapper').removeClass('wrapper');
      $('.section').wrapInner('<div class="wrapper"></div>');
      checkWidth(); // to run onLoad
      $('.page-content').fullpage();
      $(window).resize(checkWidth);
   });
</script>

<div class="section shadow-night">
<div class="main">

Layanan Penerjemahan Bahasa Indonesia-Inggris
{: class="content-id lang-hide home-title" style="text-align: center;"}
English-Indonesian Translation Services
{: class="content-en home-title" style="text-align: center;"}

Ingin menerjemahkan   
`dokumen`, `situs`, `aplikasi web`, `aplikasi ponsel`, `iklan`,  
atau media Anda lainnya dari Bahasa Inggris ke Indonesia atau sebaliknya?  
Kami dapat memberikan Anda pelayanan penerjemahan untuk teks Anda dengan  
kualitas baik dan cepat serta dengan [harga yang terjangkau][price]. 
{: class="content-id lang-hide home-text"}
Looking to translate your  
`documents`, `websites`, `web apps`, `smartphone apps`, `ads`,  
or other media from English to Indonesian or vice versa?   
We can give you rapid translations with great quality  
for your texts for an [affordable price][price].  
{: class="content-en home-text"}

</div>
</div>

<div class="section mirage">
<span class="playfair content-id lang-hide">Penerjemah Kami</span><span class="playfair content-en">Our Translators</span>

![Our Translators][our-translators]  
{: class="limage"}  

Semua penerjemah bersertifikat dan dapat menyelesaikan `1.500-2.500 kata` 
per hari. Kami menyediakan layanan penerjemahan untuk bidang teknis, 
pemasaran, akademik, bisnis, keuangan, atau lainnya, dan penerjemahan dapat 
dilakukan oleh beberapa penerjemah profesional kami sekaligus apabila 
diperlukan.  
{: class="rtext content-id lang-hide home" style="padding-top: 2%;"}  
Each of our translators is certified and is able to get through 
`1,500-2,500 words` per day. We provide technical, marketing, academic, 
business, financial, or other translation services and our translation 
process can be performed by more than one of our professional translators 
when the job requires them.   
{: class="rtext content-en home" style="padding-top: 2%;"}  

</div>

<div class="section virgin-america">
<span class="playfair content-id lang-hide">Dapatkan Penawaran Kami</span><span class="playfair content-en">Get A Free Quote</span>

![Free Quote][free-quote]  
{: class="rimage"}  

[Kirimkan][contact-us] berkas Anda dengan format `.docx`, `.pdf`, `.rtf`, 
`.txt`, `.indd`, `.psd`, berkas `strings.xml`, format yang digunakan 
program [CAT][cat-wiki], atau berkas lainnya yang berisi teks yang Anda 
ingin kami terjemahkan! Kami akan menghubungi Anda dan memberitahukan 
harga diskonnya dan waktu pengerjaannya.
{: class="ltext content-id lang-hide home" style="padding-top: 2%;"}  
[Send us][contact-us] your file with `.docx`, `.pdf`, `.rtf`, `.txt`, 
`.indd`, `.psd` format, `strings.xml` file, [CAT][cat-wiki] tools format, 
or any other file with text you want us to translate! We will get back to 
you soon with our discounted price and duration for the job.  
{: class="ltext content-en home" style="padding-top: 4%;"}  

</div>

<div class="section dirty-fog">
<span class="playfair content-id lang-hide">Layanan Lainnya</span><span class="playfair content-en">Other Services</span>

![Other Services][other-services]  
{: class="limage"}  
  
Selain menerjemahkan, kami juga melayani `penyuntingan` dan `pengoreksian` 
hasil terjemahan Anda. Pekerjaan ini bisa dibebankan per jam atau per kata, 
tergantung kesepakatan awal. 
{: class="rtext content-id lang-hide home" style="padding-top: 6%;"}  
In addition to translating, we also do `editing` and `proofreading` for 
your translation texts. These works can be charged by the hour or by word 
count depending on the initial agreement.  
{: class="rtext content-en home" style="padding-top: 7%;"}  

</div>

<div class="section ash">
<span class="playfair content-id lang-hide">Penjurubahasaan</span><span class="playfair content-en">Interpreting</span>

![Interpreting][interpreting]  
{: class="rimage"}  
  
Kami tidak melayani penjurubahasaan untuk saat ini, tetapi kami berharap 
bisa melakukan pelayanan tersebut dalam waktu dekat. Pastikan Anda mengecek 
kembali situs ini jika Anda membutuhkan layanan tersebut nanti.  
{: class="ltext content-id lang-hide home" style="padding-top: 6%;"}  
We don't do interpreting at the moment, but we expect to change the 
situation in not so distant future. Be sure to check this site back when 
you need the service later. 
{: class="ltext content-en home" style="padding-top: 8%;"}  

</div>  

[contact-us]: mailto:settrans.eits@gmail.com "SetTrans.EITS@gmail.com"
[cat-wiki]: https://en.wikipedia.org/wiki/Computer-assisted_translation 
"Computer-assisted translation"
[price]: {{ site.baseurl }}/pricing/


[our-translators]: {{ site.baseurl }}/images/our-translators.png
[free-quote]: {{ site.baseurl }}/images/free-quote.png
[other-services]: {{ site.baseurl }}/images/other-services.png
[interpreting]: {{ site.baseurl }}/images/interpreting.png
