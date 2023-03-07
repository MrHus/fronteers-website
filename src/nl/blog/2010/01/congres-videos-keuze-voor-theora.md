---
title: "Congres video's, en de keuze voor Theora"
date: 2010-01-28
author: Sander van Lambalgen
categories: 
  - Congres
  - Website
---
Na een iets langere periode wachten dan waar we met z'n allen op gehoopt hadden, zijn we dinsdag begonnen met de eerste video's van Fronteers 2009 online te zetten. Op dit moment zijn beschikbaar: [A Web of Confusion](/congres/2009/sessions/a-web-of-confusion) door Douglas Crockford, [Roll Your Own Effects Framework](/congres/2009/sessions/roll-your-own-effects-framework) door Thomas Fuchs, [The future state of layout](/congres/2009/sessions/the-future-state-of-layout) door Stephen Hay, [The Type We Want](/congres/2009/sessions/the-type-we-want-using-fonts-on-the-web) door Jonathan Snook, en [Even Faster Web Sites](/congres/2009/sessions/even-faster-web-sites) door Steve Souders. Alle video's die we de komende dagen en weken (maanden?) online gaan zetten zullen worden gelinkt vanaf de [sessions pagina](/congres/2009/sessions) van het congres. Om de video's te tonen maken we gebruik van het [`<video>`](http://www.w3.org/TR/html5/video.html#video) element, en de [Theora](http://en.wikipedia.org/wiki/Theora) codec. Dit is niet zonder enige discussie gepaard gegaan...

Op dit moment gebruikt ongeveer 65% van de bezoekers van de Fronteers website een browser die het `<video>` element in combinatie met de Theora codec ondersteunt. Dit zijn specifiek Firefox 3.5/3.6 (en andere Gecko 1.9.1+ browsers zoals SeaMonkey 2), Chrome 3/4, en (pre-)alpha builds van Opera 10.50. De (toch nog) 20% IE gebruikers zullen geen video in hun browser zien, maar kunnen de video's wel downloaden, en met hun mediaspeler naar keuze afspelen. (In het onwaarschijnlijke geval dat deze geen Theora ondersteunt is [VLC](http://www.videolan.org/vlc/) een goed en open-source alternatief.) En dan zijn er ongeveer 10% aan Safari gebruikers, die op de plaats van het video element wel de posterframe zullen zien, maar door het gebrek aan ondersteuning van de Theora codec in Safari, niet de video zullen kunnen afspelen. Deze bezoekers zullen net als de IE gebruikers de video moeten downloaden om hem te kunnen bekijken, en er is fiks gediscussieerd op het Fronteers IRC kanaal of dit de juiste keuze was, of dat we ook een versie van de video's zouden moeten aanbieden die gebruik maakt van de [H.264](http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC) codec. (Deze codec wordt naast Safari ook ondersteund door Chrome, maar niet door de open-source Chromium.) Opvallend genoeg heeft het na het online zetten van de eerste video nog twee dagen geduurd voordat iemand zelfs maar opperde de video's d.m.v. Flash ook aan IE gebruikers in de browser te tonen.

De kernvraag is: Wat is belangrijker, het op dit moment geven van een zo goed mogelijke ervaring aan zoveel mogelijk bezoekers, of het in de strijd gooien van ons collectief gewicht om toe te werken naar een situatie waarin iedere internetgebruiker zonder enige hindernissen video's kan bekijken en creëren. Wij als Fronteers hebben een voorbeeldfunctie, en willen (zoals op het oprichtingscongres is [besloten](/vereniging/bestuur/notulen/18-09-07), en op de afgelopen ALV nog eens is [bevestigd](/vereniging/bestuur/notulen/27-11-2009)), "standaardenorganisaties en implementerende partijen ertoe [..] bewegen het welzijn van front-end ontwikkelaars te verbeteren middels betere standaarden, technieken, documentatie en implementaties." Aan de andere kant, kunnen we als front-end ontwikkelaars wel serieus genomen worden als we niet de op dit moment voor zoveel mogelijk mensen best werkende oplossing kiezen?

Voor de mensen die niet op de hoogte zijn van de problematiek rondom video codecs, een korte samenvatting. HTML5 specificeert het `<video>` element. Oorspronkelijk ging dit gepaard met het specificeren van de te gebruiken codec, namelijk Theora. Apple, als een van de vijf grote browser makers, had hier echter zwaarwegende bezwaren tegen aangezien ze bevreesd waren voor "submarine" patenten op deze video codec. Dit risico bestaat natuurlijk altijd, maar met andere codecs hadden ze het risico al genomen (bijvoorbeeld via iTunes), en nog een volgend risico nemen was klaarblijkelijk onacceptabel. H.264 als de te specificeren video codec is niet acceptabel voor open source browser makers (specifiek Mozilla, maar ook relevant voor webkit-gebaseerde browsers zoals Chromium, Konqueror, e.a.), aangezien er veel software patenten op H.264 rusten. Hoewel een organisatie als Mozilla theoretisch de kosten van een licentie zou kunnen opbrengen (voor dit jaar 5 miljoen dollar, ongeveer 6% van de jaarlijkse omzet van Mozilla, met verdere jaarlijkse prijsstijgingen bijna zeker), zouden gebruikers van de Mozilla source code niet gerechtigd zijn H.264 te gebruiken. Dit gaat tegen het principe van open source software in, en is [onacceptabel voor Mozilla](http://shaver.off.net/diary/2010/01/23/html5-video-and-codecs/). (Gebruik maken van op het OS geinstalleerde codecs is voor Mozilla ook [geen oplossing](http://weblogs.mozillazine.org/roc/archives/2010/01/video_freedom_a.html); dit brengt grote beveiligingsproblemen met zich mee, en gaat tegen Mozilla's missie voor een open web in.) Tevens vindt Opera H.264 onacceptabel, voornamelijk (?) omwille van de zeer hoge licentie kosten. Gezien deze impasse, en om de realiteit beter te reflecteren, is de specificatie van een te gebruiken codec uit HTML5 verwijderd. De zoektocht naar een voor iedereen acceptabele codec blijft wel doorgaan.

Met een gebrek aan een van hogerhand opgegeven mandaat voor de codec die algemeen gebruikt gaat worden op het web, heeft de strijd zich verplaatst naar implementaties en gebruikers. H.264 wordt ondersteund door de grote media bedrijven, en de hieraan gelieerde partijen. H.264 heeft een voorsprong in gebruik, en ondersteuning in hardware. Daartegenover staat Theora met ondersteuning van de open source software wereld, en alle kleine partijen die zelf video op het web willen kunnen zetten. H.264 is op dit moment gratis te gebruiken voor het produceren van video's op kleine schaal, maar door de jaarlijks veranderende licentie structuur bestaat er totaal geen zekerheid dat dit altijd zo zal blijven. [De geschiedenis leert ons](http://www.0xdeadbeef.com/weblog/2010/01/html5-video-and-h-264-what-history-tells-us-and-why-were-standing-with-the-web/), en alle tekenen wijzen er inderdaad op, dat dit, mocht H.264 _de_ meestgebruikte videocodec worden, over een aantal jaren zal veranderen.

De situatie op dit moment is sterk in flux; alles is mogelijk, en kleine acties kunnen een groot effect hebben. Theora heeft, dankzij Firefox en Chrome, op dit moment veruit het grootste percentage aan directe ondersteuning in een browser. Mozilla werkt er tevens hard aan om de kwaliteit van de codec nog verder te verbeteren. (Er bestaan veel mythes over technische inferioriteit van de Theora codec, voornamelijk door oude tests uit de tijd dat de bitstream codec net was vastgelegd, maar er nog weinig tijd was besteed aan het implementeren van encoders en decoders; [recente](http://people.xiph.org/~greg/video/ytcompare/comparison.html) [tests](http://people.xiph.org/~maikmerten/youtube/) laten zien dat verschillen in kwaliteit minimaal zijn.) Daar tegen over staat dat YouTube en Vimeo in eerste experimenten met `<video>` [gebruik maken van H.264](http://youtube-global.blogspot.com/2010/01/introducing-youtube-html5-supported.html). (Voornamelijk omdat hun video's al in dit formaat gecodeerd waren?) Er zijn [tekenen](http://lists.xiph.org/pipermail/theora/2009-July/002415.html) dat Apple Theora wil heroverwegen, en met de aankoop van On2 heeft Google de oorsprong van de Theora codec in handen, wat mogelijkerwijs meer zekerheid kan gaan geven op het gebied van submarine patenten.

Het komende jaar gaat waarschijnlijk beslissend zijn. Komen we uit op een situatie waar H.264 _de_ video standaard voor het web wordt, en moet iedereen die iets met video doet hier geld voor gaan betalen aan de MPEG-LA? Of weet Theora genoeg momentum te behalen om Apple en grote video sites over te halen gebruik van deze codec te gaan maken, waarmee we in een wereld terecht komen waar video op het web een vrij en open formaat wordt, waar iedereen optimaal gebruik van kan maken?

Ik weet welke situatie mijn voorkeur heeft, en ik weet welke situatie beter is voor ons als web ontwikkelaars. Wij web ontwikkelaars spelen tevens zelf een rol in deze strijd, en onze keuzes kunnen van belang zijn. Hoe meer video van hoge kwaliteit op het web gepubliceerd wordt in Theora (en _niet_ in H.264), des te hoger wordt de kans dat Apple besluit dat het het risico waard is om ook Theora te ondersteunen in Safari. Fronteers is dan wel geen Wikipedia (welke site al hun video's in Theora zal hosten), maar we beginnen ondertussen toch enige omvang en naam te hebben, en kunnen deze hier nuttig gebruiken om te helpen streven naar een open web.

Wat is jullie mening? Doen we hier goed aan, of moeten we niet zo zeuren en lekker praktisch H.264 video via een Flash interface aanbieden? Is het belangrijker om nu 100% van onze bezoekers tevreden te stellen, of mogen we juist wel wat idealisme tonen en zeggen, "Wij weten wat op lange termijn het beste is!"?