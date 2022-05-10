<template>
  <v-container>
    <v-row>
      <v-col
        v-for="card of cards"
        :key="card.img"
        cols="12"
        lg="3"
        md="4"
        sm="6"
      >
        <v-card class="mx-auto card pa-2" color="indigo lighten-4">
          <v-img class="img_card" cover :src="card.img"></v-img>

          <v-card-title>{{ card.title }}</v-card-title>

          <v-card-subtitle> {{ card.subtitle }} </v-card-subtitle>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn icon @click="show = !show">
              <v-icon>{{
                show ? "mdi-chevron-up" : "mdi-chevron-down"
              }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>

              <v-card-text>
                {{ card.text }}
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    show: false,

    cards: [
      {
        img: "images/students/Qodirova.jpg",
        title: "Qodirova Dilnoza",
        subtitle: "402-guruh",
        text: "manzil jarqo'rg'on tumani ismoil tepa mahallasi",
      },
      {
        img: "images/students/Mavlon.jpg",
        title: "Mingboboyev Mavlonbek",
        subtitle: "402-guruh",
        text: "manzil Sarosiyo tumani",
      },
      {
        img: "images/students/Yoqubjon.jpg",
        title: "Chorshanbiyev Yoqubjon",
        subtitle: "402-guruh",
        text: "manzil qiziriq tumani",
      },
      {
        img: "images/students/Doniyor.jpg",
        title: "Normueodov Doniyor",
        subtitle: "402-guruh",
        text: "Manzil Jarqo'rg'on tumani",
      },
      {
        img: "images/students/Isomiddin.jpg",
        title: "Isoqov Isomiddin",
        subtitle: "402-guruh",
        text: "manzil angor tumani",
      },
      {
        img: "images/students/Abdurahmonov Jamshid.jpg",
        title: "Abdurahmonov Jamshid",
        subtitle: "402-guruh",
        text: "Manzil jarqo'rg'on tumani",
      },
      {
        img: "images/students/Akbar.jpg",
        title: "Qudratov Akbar",
        subtitle: "402-guruh",
        text: "Manzil Termiz tuman termiz mahalla(40 yillik)",
      },
      {
        img: "images/students/Aliboyev.jpg",
        title: "Aliboyev Jo'rabek",
        subtitle: "403-guruh",
        text: "Manzil sherabot tumani 17 sentir",
      },
      {
        img: "images/students/Aliyev.jpg",
        title: "Aliyev Shoxjaxon",
        subtitle: "402-guruh",
        text: "manzil Oltinsoy tumani",
      },
      {
        img: "images/students/Baxtiyor.jpg",
        title: "Ismoilov Baxtiyor",
        subtitle: "402-guruh",
        text: "manzil Jarqo'rg'on tumani",
      },
      {
        img: "images/students/Bekzod.jpg",
        title: "Temurov Bekzod",
        subtitle: "402-guruh",
        text: "Manzil termiz tumani",
      },
      {
        img: "images/students/Dilnavoz.jpg",
        title: "Boybo'riyeva Dilnavoz",
        subtitle: "402-guruh",
        text: "Manzil termiz tumani",
      },
      {
        img: "images/students/Elbek.jpg",
        title: "Lolayev Elbek",
        subtitle: "402-guruh",
        text: "manzil sho'rchi tumani",
      },
      {
        img: "images/students/Faxriddin.jpg",
        title: "Mannonov Faxriddin",
        subtitle: "402-guruh",
        text: "Manzil Denov tumani",
      },
      {
        img: "images/students/Iskandarov Do'sali.jpg",
        title: "Iskandarov Do'sali",
        subtitle: "402-guruh",
        text: "manzil qiziriq tumani",
      },
      {
        img: "images/students/Islombek.jpg",
        title: "Tadjiyev Islombek",
        subtitle: "403-guruh",
        text: "Manzil Jarqo'rg'on tumani oftobqo'rg'on mahhallasi mustaqillik ko'chasi 30-uy",
      },
      {
        img: "images/students/Isroil.jpg",
        title: "Muhammadiyev Isroil",
        subtitle: "403-guruh",
        text: "manzil Boysun tumani",
      },
      {
        img: "images/students/Jalol.jpg",
        title: "Qurbonov Jaloliddin",
        subtitle: "402-guruh",
        text: "Manzil Jarqo'rg'on tumani",
      },
      {
        img: "images/students/Kabirova.jpg",
        title: "Kabirova Saida",
        subtitle: "403-guruh",
        text: "manzil sho'rchi tumani",
      },
      {
        img: "images/students/Kamol.jpg",
        title: "Ismoilov Kamoliddin",
        subtitle: "402-guruh",
        text: "manzil Denov tumani",
      },
      {
        img: "images/students/Madiyev.jpg",
        title: "Madiyev Nasrulloh",
        subtitle: "402-guruh",
        text: "manzil boysun tumani",
      },
      {
        img: "images/students/Sanjar.jpg",
        title: "Xayitov Sanjar",
        subtitle: "403-guruh",
        text: "Manzil Jarqo'rg'on tumani surxon 5",
      },
      {
        img: "images/students/Sayyora.jpg",
        title: "Qurbonova Sayyora",
        subtitle: "402-guruh",
        text: "manzil farg'ona viloyati qo'qon",
      },
      {
        img: "images/students/Sohib.jpg",
        title: "Eshtimrov Sohibjon",
        subtitle: "402-guruh",
        text: "Manzil Muzrabot tumani",
      },
      {
        img: "images/students/Toshpo'lat.jpg",
        title: "Xidirov Toshpo'lat",
        subtitle: "402-guruh",
        text: "manzil Bandixon tumani",
      },
      {
        img: "images/students/Toshtemirov Safojon.jpg",
        title: "Toshtemirov Safojon",
        subtitle: "402-guruh",
        text: "Manzil Oltinsoy tumani",
      },
      {
        img: "images/students/Ziyodullo.jpg",
        title: "Jo'rayev Ziyodullo",
        subtitle: "402-guruh",
        text: "Manzil Qiziriq tumani",
      },
      {
        img: "images/students/Oqiljon.jpg",
        title: "Narzulloyev Oqiljon",
        subtitle: "402-guruh",
        text: "Manzil Sorosiyo tumani",
      },
    ],
  }),
};
</script>

<style>
@media (max-with: 600px) {
  .card {
    height: 100vh;
  }
}

.img_card {
  border-radius: 15px !important;
}
</style>
