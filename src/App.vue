<template>
  <div class="container">
    <p>
      <b style="font-size: 20px; color: red"> BY Berkaycan Sakar </b>
      <br /><br />
      <a href="mailto:berkaycansakar@gmail.com"
        ><i class="fa-solid fa-envelope"></i
      ></a>
      <a href="https://www.instagram.com/berkaylxl/"
        ><i class="fa-brands fa-instagram"></i
      ></a>
      <a href="https://www.linkedin.com/in/berkaycan-sakar"
        ><i class="fa-brands fa-linkedin"></i
      ></a>
      <br />
      <br />
      Ar-ge:<b style="color: gold">Ferhan Apaydın </b><br /><br />
      <a href="https://www.instagram.com/ferhan_pdn/"
        ><i class="fa-brands fa-instagram"></i
      ></a>
      <a href="https://www.linkedin.com/in/ferhan-apayd%C4%B1n-30501219b/"
        ><i class="fa-brands fa-linkedin"></i
      ></a>
    </p>

    <h2 >Cevapların Kitabı <i  @click="info" class="blink">?</i></h2>
    <div @mouseleave="test" class="book">
      <div class="cover"></div>
      <div class="page"></div>
      <div class="page"></div>
      <div class="page"></div>
      <div class="page"></div>
      <div class="page"></div>
      <div class="last-page">
        <div>
          <h4>{{ answer }}</h4>
        </div>
      </div>
      <div class="backcover"></div>
    </div>

    <div></div>
  </div>
</template>
<script>
import Swal from "sweetalert";

export default {
  data() {
    return {
      answer: "",
      answers: [
        { id: 0, answer: "Olmaz" },
        { id: 1, answer: "Evet" },
        { id: 2, answer: "Hayır" },
        { id: 3, answer: "Asla" },
        { id: 4, answer: "Belki" },
        { id: 5, answer: "Evet" },
        { id: 6, answer: "Olabilir" },
        { id: 7, answer: "Kesinlikle" },
        { id: 8, answer: "Malesef" },
        { id: 9, answer: "Olumsuz" },
        { id: 10, answer: "Olur" },
        { id: 11, answer: "İmkansız" },
        { id: 12, answer: "Bi ihtimal" },
        { id: 13, answer: "Soruya bak ahaha Hayır" },
        { id: 14, answer: "Tabi ki de" },
        { id: 15, answer: "Kesinlikle" },
        { id: 16, answer: "Evet" },
        { id: 17, answer: "Neden olmasın" },
        { id: 18, answer: "olmaması mümkün değil" },
        { id: 19, answer: "Gerçekleş -memesi için bir sebep yok" },
        { id: 20, answer: "Gerekeni yapmalısın" },
        { id: 21, answer: "Olabilir" },
        { id: 22, answer: "Çabalamalısın" },
        { id: 23, answer: "Yapabileceğini biliyosun" },
        { id: 24, answer: "Olur be" },
        { id: 25, answer: "Umudunu kaybetme" },
        { id: 26, answer: "Çalışmayı bırakmazsan evet" },
        { id: 27, answer: "Hedefin için çalış" },
        { id: 28, answer: "Oldu bil" },
        { id: 29, answer: "Niye olmasın ki" },
        { id: 30, answer: "Yapabileceğini biliyorsun" },
        { id: 31, answer: "Tek başına olmaz" },
        { id: 32, answer: "Destek almalısın" },
        { id: 33, answer: "Keyfini çıkart" },
        { id: 34, answer: "Her şey senin elinde" },
        { id: 35, answer: "Destek almalısın" },
        { id: 36, answer: "Keyfini çıkart" },
        { id: 37, answer: "Endişelenme" },
        { id: 38, answer: "Bu işi daha sonra düşün" },
        { id: 39, answer: "Başarmak için tüm gücünle uğraş" },
        { id: 40, answer: "Hiç denenmemiş bir çözüm düşün" },
        { id: 41, answer: "Olmasını istiyorsan çabalamalısın" },
        { id: 42, answer: "İlk aldığın karara güven" },
        { id: 43, answer: "Şükretmesini bil" },
        { id: 44, answer: "Fikrini değiştirme" },
        { id: 45, answer: "Hedefinden şaşma" },
        { id: 46, answer: "Kafanı dağıtmalısın" },
        { id: 47, answer: "Mutlaka destek göreceksin" },
        { id: 48, answer: "Etrafında -kilere bak" },
        { id: 49, answer: "Önce durumu değerlendir sonra keyfini" },
        { id: 50, answer: "Önce durumu değerlendir sonra keyfini çıkart" },
        { id: 51, answer: "Endişelenme" },
        { id: 52, answer: "Yaptığın için mutlu olacaksın ,çalış" },
        { id: 53, answer: "İyi niyetle çabalarını sürdür" },
        { id: 54, answer: "Bekle" },
        { id: 55, answer: "Mutlaka başarılı olacaksın" },
        { id: 56, answer: "Başarıcaksın" },
        { id: 57, answer: "Sana söyleneni yap" },
        { id: 58, answer: "Sorumluluk -larını yerine getir" },
        { id: 59, answer: "Bu konuda yeteri kadar deneyimin var" },
        { id: 60, answer: "Karar vermek için kendine zaman ayır" },
        { id: 61, answer: "Israrlı ol" },
        { id: 62, answer: "Cesurca davran" },
        { id: 63, answer: "Hayır" },
        { id: 64, answer: "İmkansız" },
        { id: 65, answer: "Oması mümkün değil" },
        { id: 66, answer: "Gerçekleşecek bir şey değil" },
        { id: 67, answer: "Ne kadar çabalarsan çabala :(" },
        { id: 68, answer: "Olmayabilir" },
        { id: 69, answer: "Umutlanma" },
        { id: 70, answer: "Olmayacağını biliyorsun" },
        { id: 71, answer: "Olamaz" },
        { id: 72, answer: "Maalesef" },
        { id: 73, answer: "cık" },
        { id: 74, answer: "Yok" },
        { id: 75, answer: "Herkesin gördüğünü görmezlikten gelme" },
        { id: 76, answer: "Şuan daha fazlasını isteme" },
        { id: 77, answer: "Bu başka bir konuya bağlı" },
        { id: 78, answer: "Bu pek tavsiye edilmez" },
        { id: 79, answer: "Adımlarını dikkatli at" },
        { id: 80, answer: "Boşuna zamanını harcama" },
        { id: 81, answer: "Hedefini değiştir" },
        { id: 82, answer: "Bu iş senin elinde değil" },
        { id: 83, answer: "Fikrini değiştirmelisin" },
        { id: 84, answer: "Önce başka şeyleri bitir" },
        { id: 85, answer: "Bu kesin değil" },
        { id: 86, answer: "Önceliklerini değiştirmelisin" },
        { id: 87, answer: "10a kadar say ve tekrar sor" },
        { id: 88, answer: "Başka konulara odaklan" },
        { id: 89, answer: "Sana pahalıya patlayacak" },
        { id: 90, answer: "Alışman gerekecek" },
        { id: 91, answer: "Beklenmedik şeylerle karşılaşa- bilirsin" },
        { id: 92, answer: "Bazı durumlara hazırlıklı ol" },
        { id: 93, answer: "Hayır ve zorlama" },
        { id: 94, answer: "Tekrar deneyiniz" },
        { id: 95, answer: "Olsun mu?" },
        { id: 96, answer: "Maalesef , hayırlısı böyleymiş" },
        { id: 97, answer: "Annene sor" },
        { id: 98, answer: "Çok mu istiyon" },
        { id: 99, answer: "Olsun be seni mi kırıcam" },
        { id: 100, answer: "Oldu paşam" },
        { id: 101, answer: "Bunu bilmiyorum başka soru sor" },
        { id: 102, answer: "Hee olur olur" },
        { id: 103, answer: "Evet(!)" },
        { id: 104, answer: "Bu soruyu sormak istediğine emin misin" },
        { id: 105, answer: "Bunu orjinal kitaba sorsan daha iyi olur" },
        { id: 106, answer: "Kapağı yavaşça kapat ve defol burdan" },
        { id: 107, answer: "Yoo" },
        { id: 108, answer: "Başka hayaller kur" },
        { id: 109, answer: "Bunu yazan tosun ..." },
      ],
    };
  },
  methods: {
    test() {
      setTimeout(() => {
        const number = Math.floor(Math.random() * 109);
        const answer = this.answers.filter((a) => a.id == number);
        this.answer = answer[0].answer;
      }, 1900);
    },
    info() {
      Swal('Aklından bir soru tut.Cevabını almak için kitaba tıkla','(Ör: Uzaylılar var mı ?)')
    },
  },
  mounted() {
    const number = Math.floor(Math.random() * 109);
    const answer = this.answers.filter((a) => a.id == number);
    this.answer = answer[0].answer;
    console.log(number, answer);
  },
};
</script>


<style >
.container {
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  gap: 7rem;
}
* {
  margin: 0px;
  padding: 0px;
  font-family: "Courier New", Courier, monospace;
}
body {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #e0e4ee;
}
p {
  text-align: center;
}
a {
  text-decoration: none;
  margin-right: 4px;
}
 .blink{
   text-shadow: 5px 5px 18px ;
   cursor: pointer;
      animation: blinker 0.9s linear infinite;
      color: #1c87c9;
      font-size: 30px;
      font-weight: bold;
      font-family: sans-serif;
      }
      @keyframes blinker {  
      50% { opacity: 0; }
      }
.book {
  perspective: 1000px;
  display: flex;
  align-items: center;
  cursor: pointer;
}
.book:hover .cover {
  transform: rotateX(10deg) rotateY(-180deg);
}
.book:hover .page {
  transform: rotateX(10deg) rotateY(-180deg);
  z-index: 2;
}
.cover {
  z-index: 1;
  transition: all 3s;
}
.backcover {
  z-index: -2;
}
.cover,
.backcover {
  height: 200px;
  width: 160px;
  background: #353755;
  border-radius: 2px 20px 20px 2px;
  position: absolute;
  box-shadow: 1px 1px 10px gray;
  transform: rotatex(10deg);
  transform-origin: center left;
}
.page,
.last-page {
  height: 180px;
  width: 150px;
  background: white;
  position: absolute;
  border-radius: 2px 10px 10px 2px;
  transform: rotatex(10deg);
  transform-origin: center left;
  z-index: -1;
}
.page:nth-child(2) {
  transition-duration: 3s;
}
.page:nth-child(3) {
  transition-duration: 2.6s;
}
.page:nth-child(4) {
  transition-duration: 2.2s;
}
.page:nth-child(5) {
  transition-duration: 1.8s;
}
.page:nth-child(6) {
  transition-duration: 1.4s;
}
.book:hover .page:nth-child(2) {
  transition-duration: 6s;
}
.book:hover .page:nth-child(3) {
  transition-duration: 5.6s;
}
.book:hover .page:nth-child(4) {
  transition-duration: 5.2s;
}
.book:hover .page:nth-child(5) {
  transition-duration: 4.8s;
}
.book:hover .page:nth-child(6) {
  transition-duration: 4.4s;
}
.last-page div h4 {
  width: 100px;
  display: block;
  margin: 45% auto;
  text-align: center;
  position: relative;
  z-index: -1;
}
</style>