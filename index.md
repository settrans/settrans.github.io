---
layout: default
---

{::options parse_block_html="true" /}
<script src="/scripts/jquery.fullPage.min.js"></script>
<script>
   //background rotator function and variables
   var time = $.now();
   var currentBG = time % 4;
   var BGsLoaded = 1;
   var backgrounds = [];
   backgrounds[0] = '/images/bg1.jpg';
   backgrounds[1] = '/images/bg2.jpg';
   backgrounds[2] = '/images/bg3.jpg';
   backgrounds[3] = '/images/bg4.jpg';

   function changeBG() {
       if(BGsLoaded == 2) {
          $('.site-subtitle-en, \
             .site-subtitle-id, \
             .content-en, \
             .site-nav, \
             #down-arrows, \
             #lang-button').fadeIn(4000);
       }

       if(BGsLoaded < 4){
          currentBG++;
          if(currentBG > 3) currentBG = 0;

          $('.bgLower').css({
             'background-image': "url('"+backgrounds[currentBG]+"')",
             'opacity': '0'
          });
          
          $('.bgLower').animate({
             'opacity': '1'
          }, 2000);
          
          $('.bgUpper').animate({
             'opacity': '0'
          }, 2000);

          $('.bgUpper').css({
             'background-image': "url('"+backgrounds[currentBG]+"')",
             'opacity': '1'
          });

          BGsLoaded++;
          setTimeout(changeBG, 2000);
       } 
   }

   function checkWidth() {
      if ($(window).width < 600) {
         $('.section > .wrapper').removeClass('wrapper');
      }
   }

   $(document).ready(function(){
      $('.page-content').fullpage({
         fixedElements: '#down-arrows',
         easing: 'easeInOutQuad',
         verticalCentered: true,
         onLeave: function(index, nextIndex, direction){
            var leavingSection = $(this);

            if(direction == 'up' || (index == 5 && direction == 'down')){
               $('#down-arrows').hide();
            } else {
               $('#down-arrows').show();
            }
            
            if(index == 1 && direction =='down'){
               $('.site-header').addClass('darkgray', 5000);
            }
            else if(index == 2 && direction == 'up'){
               $('.site-header').removeClass('darkgray', 5000);
            }
         },
         afterLoad: function(anchorLink, index){
            var loadedSection = $(this);

            if(index == 6){
               $('#down-arrows').hide();
            } else if(index == 1){
               $('#down-arrows').show();
            } 
         }
      });

      checkWidth(); // to run onLoad
      $(window).resize(checkWidth);

      //rotating background
      $('.site-subtitle-en, \
         .site-subtitle-id, \
         .content-en, \
         #down-arrows, \
         .site-nav, \
         #lang-button').hide();

       $('.bgUpper').css({
          'background-image': "url('"+backgrounds[currentBG]+"')",
          'opacity': '1'
       });
      setTimeout(changeBG, 2000);        

      $('.site-header').removeClass('darkgray');
   });
</script>

<div class="bgUpper"></div>
<div class="bgLower"></div>
<div class="section">
<div class="crazy-orange">
<div class="wrapper">

Ingin menerjemahkan   
`dokumen`, `situs`,  
`aplikasi web`, `aplikasi ponsel`, `iklan`,  
atau media Anda lainnya dari Bahasa Inggris ke Indonesia   
atau sebaliknya?  
{: class="content-id home-text"}
Looking to translate your  
`documents`, `websites`,  
`web apps`, `smartphone apps`, `ads`,  
or other media from English to Indonesian  
or vice versa?   
{: class="content-en home-text"}

</div>
</div>
</div>

<div class="section passion">
<div class="wrapper">

Kami menyediakan:
{: class="content-id home-text"}
We provide:
{: class="content-en home-text"}

Layanan Penerjemahan Bahasa Indonesia-Inggris.
{: class="content-id home-title"}
English-Indonesian Translation Services.
{: class="content-en home-title"}
  

Kami dapat memberikan Anda pelayanan penerjemahan yang cepat untuk  
teks Anda dengan akurasi tinggi serta [harga yang terjangkau][price]. 
{: class="content-id home-text"}
We can give you rapid translations with great accuracy  
for your texts for an [affordable price][price].  
{: class="content-en home-text"}

</div>
</div>

<div class="section ash">
<div class="wrapper">
<span class="open-sans content-id">Penerjemah</span>
<span class="open-sans content-en">Translators</span>

![Our Translators][our-translators]  
{: class="limage"}  

Kami adalah orang-orang Indonesia Asli dan merupakan penerjemah 
bersertifikat. Masing-masing mampu menyelesaikan `1.000-2.500 kata` per 
hari. Selain itu, proses penerjemahan juga dapat dilakukan oleh beberapa 
penerjemah sekaligus untuk mempercepat pengerjaan.
{: class="rtext content-id home" style="padding-top: 2%;"}  
We are all Native Indonesians and certified translators. Each one of us 
can get through `1,500-2,500 words` per day. In addition, our translation 
process can be performed by more than one translator to accelerate the 
job execution.
{: class="rtext content-en home" style="padding-top: 3%;"}  

</div>  
</div>

<div class="section virgin-america">
<div class="wrapper">
<span class="open-sans content-id">Dapatkan Penawaran Kami</span><span class="open-sans content-en">Get A Quote</span>

![Free Quote][free-quote]  
{: class="rimage"}  

[Kirimkan][contact-us] berkas Anda dengan format `.docx`, `.pdf`, `.rtf`, 
`.txt`, `.indd`, `.psd`, berkas `strings.xml`, format yang digunakan 
program [CAT][cat-wiki], atau berkas lainnya yang berisi teks yang Anda 
ingin kami terjemahkan! Kami akan menghubungi Anda dan memberitahukan 
harga dan waktu pengerjaannya.
{: class="ltext content-id home" style="padding-top: 2%;"}  
[Send us][contact-us] your file with `.docx`, `.pdf`, `.rtf`, `.txt`, 
`.indd`, `.psd` format, `strings.xml` file, [CAT][cat-wiki] tools format, 
or any other file with text you want us to translate! We will get back to 
you soon with our price and duration for the job.  
{: class="ltext content-en home" style="padding-top: 5.5%;"}  

</div>  
</div>

<div class="section dirty-fog">
<div class="wrapper">
<span class="open-sans content-id">Layanan Lainnya</span><span class="open-sans content-en">Other Services</span>

![Other Services][other-services]  
{: class="limage"}  
  
Selain menerjemahkan, kami juga melayani `penyuntingan` dan `pengoreksian` 
hasil terjemahan Anda. Tarif pekerjaan tersebut juga dibebankan per kata.
{: class="rtext content-id home" style="padding-top: 5%;"}  
In addition to translating, we also do `editing` and `proofreading` for 
your translation texts. These jobs also charge by word count.
{: class="rtext content-en home" style="padding-top: 7%;"}  

</div>  
</div>

<div class="section midnight-city">
<div class="wrapper">
<span class="open-sans content-id">Penjurubahasaan</span><span class="open-sans content-en">Interpreting</span>

![Interpreting][interpreting]  
{: class="rimage"}  
  
Kami tidak melayani penjurubahasaan untuk saat ini, tetapi kami berharap 
bisa melakukan pelayanan tersebut dalam waktu dekat. Pastikan Anda mengecek 
kembali situs ini jika Anda membutuhkan layanan tersebut nanti.  
{: class="ltext content-id home" style="padding-top: 6%;"}  
We don't do interpreting at the moment, but we expect to change the 
situation in not so distant future. Be sure to check this site back when 
you need the service later. 
{: class="ltext content-en home" style="padding-top: 8%;"}  

</div>  
</div>  

<div id="down-arrows">
<svg class="down-arrows">
<path class="a1" d="M10 0 L30 16 L50 0"></path>
<path class="a2" d="M5 10 L30 29 L55 10"></path>
<path class="a3" d="M0 20 L30 43 L60 20"></path>
</svg>
</div>


[contact-us]: mailto:settrans.eits@gmail.com "SetTrans.EITS@gmail.com"
[cat-wiki]: https://en.wikipedia.org/wiki/Computer-assisted_translation 
"Computer-assisted translation"
[price]: {{ site.baseurl }}/pricing/


[our-translators]: {{ site.baseurl }}/images/our-translators.png
[free-quote]: {{ site.baseurl }}/images/free-quote.png
[other-services]: {{ site.baseurl }}/images/other-services.png
[interpreting]: {{ site.baseurl }}/images/interpreting.png
