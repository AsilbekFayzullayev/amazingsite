<template>
  <div>
    <pages_header
      title="Free Hosting"
      text="FOR FIRST TIME IN UZBEKISTAN AND ONLY AT US"
    />

    <v-row>
      <v-col md="8" offset-md="2" class="text-center">
        <h2 class="my-5">FREE HOSTING IN TAS-IX ZONE</h2>
        <v-row>
          <v-col cols="12" md="6" sm="6">
            <v-card outlined>
              <p style="background-color: darkred;color: aliceblue;border:none" class="py-5">What is included</p>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Storage</span>
                <v-spacer></v-spacer>
                <span>100 MB</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Site</span>
                <v-spacer></v-spacer>
                <span>1</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>MySQL database</span>
                <v-spacer></v-spacer>
                <span>1</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Mailbox</span>
                <v-spacer></v-spacer>
                <span>1</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Ram</span>
                <v-spacer></v-spacer>
                <span>512 GB</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Traffic</span>
                <v-spacer></v-spacer>
                <span>UNLIM</span>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" md="6" sm="6">
            <v-card outlined>
              <p style="background-color: bisque;border:none" class="py-5">FEATURES</p>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>in TAS-IX zone</span>
                <v-spacer></v-spacer>
                <span><v-icon color="#8b0000">mdi-checkbox-multiple-marked-circle-outline </v-icon></span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Control panel</span>
                <v-spacer></v-spacer>
                <span>1</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>PHP version</span>
                <v-spacer></v-spacer>
                <span>7.1</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Auto installer</span>
                <v-spacer></v-spacer>
                <span>Wordpress</span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>File manager</span>
                <v-spacer></v-spacer>
                <span><v-icon color="#8b0000">mdi-checkbox-multiple-marked-circle-outline </v-icon></span>
              </div>
              <hr>
              <div class="d-flex px-10 py-5 font-weight-bold">
                <span>Valid until</span>
                <v-spacer></v-spacer>
                <span> 1 year</span>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-col cols="12" style="background-color: aliceblue" class="py-10 mt-10">
      <v-row>
        <v-col md="8" offset-md="2" class="text-center">
          <h4 class="mb-10">
            HOW CAN I BECOME A PARTICIPANT OF THE PROGRAM?</h4>
          <v-row class="align-center">
            <v-col style="position: relative" class="px-10" cols="12" md="4" sm="4">
              <v-card class="py-10 px-2"
                      style="background-color: darkgoldenrod;border-top-right-radius: 50px;border-bottom-left-radius: 50px;color: aliceblue">
                <span style="">register in my.eskiz.uz</span>
              </v-card>
              <span
                style="position: absolute;left: 30px;top: 5px;background-color: darkred; border-radius: 50%;color:aliceblue"
                class="px-2"
              >1</span>
            </v-col>
            <v-col style="position: relative" class="px-10" cols="12" md="4" sm="4">
              <v-card class="py-10 px-2"
                      style="background-color: crimson;border-top-right-radius: 50px;border-bottom-left-radius: 50px;color: aliceblue">
                <span style="">Upload your student ID</span>
              </v-card>
              <span
                style="position: absolute;left: 30px;top: 5px;background-color: darkred; border-radius: 50%;color:aliceblue"
                class="px-2"
              >2</span>
            </v-col>
            <v-col style="position: relative" class="px-10" cols="12" md="4" sm="4">
              <v-card class="py-10 px-2"
                      style="background-color: cadetblue;border-top-right-radius: 50px;border-bottom-left-radius: 50px;color: aliceblue">
                <span style="color: aliceblue">
                   Use start
                </span>
              </v-card>
              <span
                style="position: absolute;left: 30px;top: 5px;background-color: darkred; border-radius: 50%;color:aliceblue"
                class="px-2"
              >3</span>
            </v-col>
          </v-row>

          <v-btn class="mt-10 button">I want a free hosting</v-btn>
        </v-col>
      </v-row>
    </v-col>

    <v-col md="8" offset-md="2" class="text-center py-10">
      <h4>FAQ</h4>

      <v-row class="my-10">
        <v-col cols="12" md="6" sm="6" v-for="question of questions" :key="question.id">
          <v-card outlined>
            <div class="d-flex">
              <div style="width: 10%;" class="py-5">
                <v-icon style="color: aliceblue" color="red">mdi-help-circle-outline</v-icon>
              </div>
              <div style="width: 90%;" class="py-2">
                <v-card-actions>
                  <span>{{ question.question }}</span>
                  <v-spacer></v-spacer>

                  <v-btn
                    icon
                    @click="question.show = !question.show"
                  >
                    <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                  </v-btn>
                </v-card-actions>
              </div>
            </div>
            <v-expand-transition>
              <div v-show="question.show">
                <v-divider></v-divider>
                <v-row class="align-center">
                  <v-col cols="12" md="1" sm="1" class="text-center">
                    <span>
                      <v-icon style="color: green;font-size: 30px">mdi-checkbox-multiple-marked-circle-outline </v-icon>
                    </span>
                  </v-col>
                  <v-col cols="12" md="11" sm="11">
                    <v-card-text>
                      {{ question.answer }}
                    </v-card-text>
                  </v-col>
                </v-row>

              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>

      <ShareWithFriends/>

    </v-col>
  </div>
</template>

<script>
import Pages_header from "../layouts/pagesHeader";
import ShareWithFriends from "../layouts/shareWithFriends"
export default {
  name: "free_hosting",
  components: {Pages_header,ShareWithFriends},
  data:()=>({
    show: false,
    questions: [
      {
        id: 1,
        question: 'Nima uchun bizga yordamlashyapsiz?',
        show: false,
        answer: 'Chunki biz yosh avlod rivojiga va mamlakatimiz ravnaqiga o‘z hissamizni qo‘shmoqchimiz.'
      },
      {
        id: 2,
        question: '“Talabalarga yordam” dasturidan qancha vaqt foydalansam bo‘ladi?',
        show: false,
        answer: 'Dastur talabaning faqat o‘quv yurtida o‘qiyotgan davri uchungina mo‘ljallangan. O‘quv muddati tugagach, shaxsiy kabinetdagi maqomingiz avtomatik tarzda “Foydalanuvchi” bo‘lib qoladi, hamda bundan keyingi barcha Buyurtmalar chegirmasiz rasmiylashtiriladi.'
      },
      {
        id: 3,
        question: 'Bu qanday ishlaydi?',
        show: false,
        answer: '1. Siz my.eskiz.uz saytida ro‘yxatdan o‘tishingiz, hamda o‘z Pasport va Talabalik guvohnomangiz ma’lumotlarini kiritishingiz lozim. 2. Moderator tomonidan barcha ma’lumotlaringiz tekshirib ko‘rilgach, maqomingiz “Talaba” ga aylanadi. Huddi shu paytdan boshlab, buyurtmalarni rasmiylashtirish mobaynida barcha Buyurtmalar chegirmali qilib aks ettiriladi.'
      },
      {
        id: 4,
        question: 'Xizmatlaringizni do‘stim uchun chegirma bilan harid qilishim mumkinmi?',
        show: false,
        answer: 'Ha, Siz barcha Xosting tariflarini, domen, pochta, hamda VPS xizmatlarini do‘stingiz uchun ham sotib olishingiz mumkin. Biroq, buyurtmalarni faqat o‘z akkuantingiz orqaligina, ya’ni faqat o‘z shaxsiy kabinetingizda rasmiylashtira olasiz, Siz o‘z do‘stingiz uchun alohida akkuant yarata olmaysiz.'
      },
      {
        id: 5,
        question: 'Agar men endigina o‘rgana boshlagan bo‘lsam, xostingizni tushuna olamanmi?',
        show: false,
        answer: 'Xosting cPanel boshqaruv panelida ishlaydi. sPanel serverni boshqarish pullik panellari ichida eng mashhuri bo‘lib, Internet sarhadlarida uni boshqarishga oid ko‘pdan-ko‘p ma’lumotlar mavjud. Undan tashqari, Siz bizning 24/7 texnik ko‘makchilarimizga xam murojaat qilishingiz mumkin.'
      },
      {
        id: 6,
        question: 'Talaba sifatida qancha domenlarni ro‘yxatdan o‘tkazishim mumkin, hamda domenlarni uzaytirish uchun chegirma amal qiladimi?',
        show: false,
        answer: 'Siz xohlagan miqdorda yangi domenlarni ro‘yxatdan o‘tkazishingiz mumkin, bundan tashqari domenlarni o‘zaytirish uchun ham chegirmalar taqdim etiladi.'
      }
    ]
  })
}
</script>

<style scoped>
.button {
  border-radius: 30px;
  color: aliceblue;
  background-color: darkslategray !important;
  letter-spacing: 2px;
}

.button:hover {
  transform: scale(1.1);
}
</style>
