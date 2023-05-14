<template>
  <footer id="content-info" role="contentinfo">
    <hr class="dashed">
    <!-- P3.no footer -->
    <div class="p3-footer-container">
  <v-row class="footer__row container footer-cs">
      <v-col  md="4" sm="6">
        <h4>Kontakt</h4>
        <p> Direkte til P3: <a href="mailto:p3@nrk.no">p3@nrk.no</a><br>
          Musikktips: <a href="mailto:musikkprodusenterP3@nrk.no">musikkprodusenterP3@nrk.no</a><br>
          Kontakt NRK: 23 04 70 00</p>
      </v-col>
        <v-col  md="4" sm="6" xs="12">
          <h4>Besøk</h4>
          <p>Oslo: Bjørnstjerne Bjørnsons Plass 1, Marienlyst (<a href="https://bit.ly/kartNRKp3Oslo">kart</a>)<br>
            Trondheim: Otto Nielsens veg 2, Tyholt (<a href="https://bit.ly/kartNRKp3Trondheim">kart</a>)</p>
        </v-col>
        <v-col  md="4" sm="6" xs="12">
          <h4>Følg oss</h4>
            <a href="https://instagram.com/nrkp3" title="Følg oss på Instagram" >
            <v-img class="sosiale__medier__icon" src="https://www.citypng.com/public/uploads/preview/-115981405804zwku1bp9s.png"></v-img></a>
            <a href="https://www.snapchat.com/add/p3snap" title="Følg oss på Snapchat" >
            <v-img class="sosiale__medier__icon" src="https://www.citypng.com/public/uploads/preview/-11600705775qbd0gmt15z.png"></v-img></a>
        </v-col>
    </v-row>
    </div>
    <!-- // P3.no footer -->
  
    <!-- NRK.no-footer-->
  <div class="black__background__color">
  <v-row class="black-footer-pedding">
    <v-col cols="6" class="nrk__om">
    <ul>
      <li>
      <a title="Opphavsrett NRK © 2023" href="https://www.nrk.no/etikk/opphavsrett-pa-nrk.no-1.2843522">Opphavsrett NRK © 2023</a>
      </li>
      <li>Redaktør P3: <a title="Camilla Bjørn" href="mailto:Camilla.Bjorn@nrk.no">Camilla Bjørn</a></li>
      <li>Ansvarlig redaktør: <a title="Thor Gjermund Eriksen" href="//www.nrk.no/informasjon/1.2843526">Vibeke Fürst Haugen</a></li>
      <li>Sjefen: <a title="Homan Mousavi" href="https://homanism.github.io/Homan-portfolio/">Homan Mousavi</a></li>
    </ul>
    </v-col>
    <v-col cols="6" class="nrk__hjelp">
    <ul>
      <li>
      <a title="Kontakt NRK" href="//www.nrk.no/kontakt/">Kontakt NRK</a>
      </li>
      <li>
      <a title="Om NRK" href="//www.nrk.no/informasjon">Om NRK</a></li>
      <li>
      <a title="Personvern" href="//www.nrk.no/retningslinjer/personvern-i-nrk-1.7765898">Personvern</a>
      </li>
      <li>
      <a title="Informasjonskapsler (cookies)" href="//www.nrk.no/retningslinjer/informasjonskapsler-_cookies_-1.11109868">Informasjonskapsler (cookies)</a>
      </li>
    </ul>
    </v-col>
  </v-row>
  </div>
  <!-- //NRK.no-footer-->
    </footer>
  </template>
  
  <script setup>
  //
  </script>
  
  <style>
  .black__background__color {
    background-color: black;
    align-items: center;
    text-align: left;
    position: relative;
    padding-top: 20px;
    padding-bottom: 20px;
  }
  a {
    color: #ffffff;
  }
  
  .nrk__om{
    padding-left: 350px;
    color: #ffffff;
  
  }
  .nrk__hjelp{
    padding-left: 120px;
    color: #ffffff;
  }
  
  /* Dashed border */
  hr.dashed {
    border-top: 3px dotted #32a4eb;
    border-radius: 5px;
  }
  .footer__row{
    margin: 5px 250px 5px 300px;
  }
  .v-row.footer__row{
    justify-content: start;
  
  }
  @media screen and (max-width: 992.5px) {
    .footer__row{
      margin: 5px 50px 5px 50px;
    }
  
  }
  @media screen and (max-width: 892.5px) {
    .footer__row{
      margin: 5px 40px 5px 40px;
    }
  
  }
  @media screen and (max-width: 600px) {
    .v-row.footer__row{
    justify-content: start;
    flex-direction: column;
  
  }
  .footer-cs.v-row.footer__row .v-col{
    width: 100%;
  
  }
  
  }
  
  
  
  p a {
    color: rgb(0, 0, 0);
  }
  .sosiale__medier__icon{
    width:2em;
    height:2em
  }
  .black-footer-pedding{
    padding: 0 50px;
  }
  </style>
  