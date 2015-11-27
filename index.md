---
layout: default
---

{::options parse_block_html="true" /}
<head>
<link rel="stylesheet" href="{{ "/css/jquery.fullPage.css" | prepend: site.baseurl }}">
<script src="/scripts/jquery.fullPage.min.js"></script>
<script>
   //background rotator function and variables
   function changeBG() {
      $("#bg1")
         .fadeOut(800, function(){
            $('.site-subtitle-en, \
               .site-subtitle-id, \
               .content-en, \
               #down-arrows, \
               .site-nav, \
               #lang-button').velocity("fadeIn", {duration: 6000});
            $("#bg2")
               .delay(1200)
               .fadeOut(800, function(){
                  $("#bg3")
                     .delay(1200)
                     .velocity("fadeOut", {duration: 800});
               });
         });
   }

   function checkWidth() {
      if ($(window).width() < 600) {
			$('.small-screen').show();
         $('.section > .wrapper').removeClass('wrapper');
         $('.site-subtitle-en, .site-subtitle-id').hide();
		} else if ($(window).width() < 800) {
			$('.small-screen').show();

		} else {
			$('.small-screen').hide();
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
						$('.site-footer').show();
					} else if(index == 1){
						$('#down-arrows').show();
					} 
				}
			});

			//rotating background
			$('.site-subtitle-en, \
				.site-subtitle-id, \
				.content-en, \
				#down-arrows, \
				.site-nav, \
				#lang-button').hide();
			setTimeout(changeBG, 1200);        

			$('#down-arrows').on("click", $.fn.fullpage.moveSectionDown);

		}
   }

   $(document).ready(function(){
		$('.no-script').hide();
      checkWidth(); // to run onLoad
      $(window).resize(checkWidth);
		$('.site-header').removeClass('darkgray');
   });
</script>
</head>

<div class="no-script">
I'm ugly with javascript disabled.  
Please enable javascript.
</div>

<div class="small-screen">
I'm ugly on narrow screen.  
Please open in wider screen.
</div>

<div class="main" id="bg0"></div>
<div class="main" id="bg1"></div>
<div class="main" id="bg2"></div>
<div class="main" id="bg3"></div>
<div class="main" id="bg4"></div>
<div class="facade section">
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

<div class="section passion">
<div class="wrapper" style="margin-top: -120px;">

Kami dapat memberikan Anda  
{: class="content-id home-text"}
Layanan Penerjemahan Bahasa Indonesia-Inggris
{: class="content-id home-title"}
yang cepat untuk teks Anda dengan akurasi tinggi dengan [harga yang 
bersaing][price]. 
{: class="content-id home-text"}

We can give you rapid  
{: class="content-en home-text"}
English-Indonesian Translation Services
{: class="content-en home-title"}
with great accuracy for your texts at [competitive prices][price].  
{: class="content-en home-text"}

</div>
</div>

<div class="section ash">
<div class="wrapper">

Penerjemah
{: class="open-sans content-id"}
Translators
{: class="open-sans content-en"}

![Our Translators][our-translators]  
{: class="limage"}  

Kami adalah orang-orang Indonesia Asli dan merupakan penerjemah 
bersertifikat. Masing-masing dari kami mampu menyelesaikan hingga 
`2.500 kata` per hari. Selain itu, kami menggunakan pengingat 
terjemahan dan penerjemahan kolaboratif untuk mempercepat pengerjaan.
{: class="rtext content-id home" style="padding-top: 3%;"}  
We are all Native Indonesians and certified translators. Each one of us 
can get through up to `2,500 words` per day. In addition, we use 
translation memory tools and collaborative translation to accelerate the 
job execution.
{: class="rtext content-en home" style="padding-top: 5%;"}  

</div>  
</div>

<div class="section virgin-america">
<div class="wrapper">

Dapatkan Penawaran Kami
{: class="open-sans content-id"}
Get A Free Quote
{: class="open-sans content-en"}

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

Layanan Lainnya
{: class="open-sans content-id"}
Other Services
{: class="open-sans content-en"}

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
We don't do interpreting at the moment, but we do expect to change the 
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
