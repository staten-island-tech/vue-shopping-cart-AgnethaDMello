<template>
  <div class="home">
    <div class="cart">
      <h2 class="urcart">Your Cart!</h2>
      <p class="arts"></p>
      <h3 id="totalprice"></h3>
    </div>
    <div class="cards">
      <Card
        class="card"
        v-for="item in items"
        :id="item.id"
        :key="item.name"
        :title="item.name"
        :image="item.img"
        :price="item.price"
        @click="shop"
      >
      </Card>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Card from "@/components/Card.vue";

export default {
  name: "Home",
  components: {
    Card,
  },
  data() {
    return {
      items: [
        {
          name: "Sandcastle Panda Sticker",
          img: "https://i.etsystatic.com/11283935/c/1315/1045/106/84/il/5b037e/3468761399/il_340x270.3468761399_fwm9.jpg",
          price: 3,
          id: 1,
        },
        {
          name: "Pool Panda Sticker",
          img: "https://i.etsystatic.com/11283935/c/1193/948/158/229/il/b09058/3468465571/il_340x270.3468465571_grws.jpg",
          price: 3,
          id: 2,
        },
        {
          name: "Flower Panda Sticker",
          img: "https://i.etsystatic.com/11283935/c/959/763/492/484/il/fa154a/3468747255/il_340x270.3468747255_ko3p.jpg",
          price: 4,
          id: 3,
        },
        {
          name: "Overheating Panda Sticker",
          img: "https://i.etsystatic.com/11283935/c/789/627/310/310/il/b3c776/3468650029/il_340x270.3468650029_r14s.jpg",
          price: 3,
          id: 4,
        },
        {
          name: "Foxes Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/1121/891/220/244/il/1f8434/3592731471/il_340x270.3592731471_7h04.jpg",
          price: 2,
          id: 5,
        },
        {
          name: "Sushi Cat Shirt",
          img: "https://i.etsystatic.com/11283935/c/946/752/655/400/il/2e8b4d/3312612820/il_340x270.3312612820_2nnm.jpg",
          price: 16,
          id: 6,
        },
        {
          name: "Sushi Cat Stickers",
          img: "https://i.etsystatic.com/11283935/c/1032/820/251/185/il/7b4beb/2705313020/il_340x270.2705313020_9zk1.jpg",
          price: 5,
          id: 7,
        },
        {
          name: "Star Kitten Stickers",
          img: "https://i.etsystatic.com/11283935/c/759/603/162/204/il/3d7a3e/2690610308/il_340x270.2690610308_e9vr.jpg",
          price: 5,
          id: 8,
        },
        {
          name: "Prototype E-1 Print",
          img: "https://i.etsystatic.com/11283935/c/1421/1129/60/406/il/d5a0c4/2786652243/il_340x270.2786652243_1u7m.jpg",
          price: 10,
          id: 9,
        },
        {
          name: "Wild Radio Sticker",
          img: "https://i.etsystatic.com/11283935/c/873/694/336/224/il/c0170b/2707804864/il_340x270.2707804864_4m49.jpg",
          price: 4,
          id: 10,
        },
        {
          name: "Woodland Tea Party Sticker",
          img: "https://i.etsystatic.com/11283935/c/916/728/274/203/il/b7958d/2717107854/il_340x270.2717107854_q3rd.jpg",
          price: 4,
          id: 11,
        },
        {
          name: "Cliff Side Drift Print",
          img: "https://i.etsystatic.com/11283935/c/872/693/52/522/il/d98abe/2821571861/il_340x270.2821571861_jzgs.jpg",
          price: 11,
          id: 12,
        },
        {
          name: "A Hard Day's Work Print",
          img: "https://i.etsystatic.com/11283935/c/619/492/368/50/il/d764ab/2749641174/il_340x270.2749641174_kad1.jpg",
          price: 11,
          id: 13,
        },
        {
          name: "Animal Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/2752/2187/164/11/il/cde0f4/2331786627/il_340x270.2331786627_70nz.jpg",
          price: 4,
          id: 14,
        },
        {
          name: "Polygons Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/2129/1693/291/209/il/2851a2/2334360643/il_340x270.2334360643_1ipq.jpg",
          price: 4,
          id: 15,
        },
        {
          name: "TV-Boy Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/2223/1767/180/228/il/d0640b/2284171328/il_340x270.2284171328_j5sb.jpg",
          price: 4,
          id: 16,
        },
        {
          name: "Bean People Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/2216/1761/312/265/il/21e9ca/2334378557/il_340x270.2334378557_p9dq.jpg",
          price: 4,
          id: 17,
        },
        {
          name: "Food Sticker Pack",
          img: "https://i.etsystatic.com/11283935/c/1960/1558/377/326/il/92b23a/2334361851/il_340x270.2334361851_3z15.jpg",
          price: 4,
          id: 18,
        },
        {
          name: "Crumbling Sweets Print",
          img: "https://i.etsystatic.com/11283935/c/749/595/374/262/il/07b184/2767290339/il_340x270.2767290339_sg1y.jpg",
          price: 10,
          id: 19,
        },
        {
          name: "City Streets at Night Print",
          img: "https://i.etsystatic.com/11283935/c/1120/890/478/335/il/ce614b/2769222341/il_340x270.2769222341_tqgc.jpg",
          price: 10,
          id: 20,
        },
        {
          name: "Jump Bros Print",
          img: "https://i.etsystatic.com/11283935/r/il/4a11ce/2030744456/il_340x270.2030744456_jgvd.jpg",
          price: 10,
          id: 21,
        },
        {
          name: "Nitro at Sunset Painting",
          img: "https://i.etsystatic.com/11283935/c/1136/903/63/179/il/263bce/3426591739/il_340x270.3426591739_mwpl.jpg",
          price: 100,
          id: 22,
        },
        {
          name: "Night City Streets Painting",
          img: "https://i.etsystatic.com/11283935/r/il/8bdeb5/3378934488/il_340x270.3378934488_sy1o.jpg",
          price: 70,
          id: 23,
        },
        {
          name: "Megaman vs. Ryu Painting",
          img: "https://i.etsystatic.com/11283935/c/1851/1471/522/276/il/5adc1a/2143201739/il_340x270.2143201739_letb.jpg",
          price: 30,
          id: 24,
        },
        {
          name: "It's A Snow Poff Painting",
          img: "https://i.etsystatic.com/11283935/c/1807/1436/571/633/il/0b262d/2143095231/il_340x270.2143095231_r412.jpg",
          price: 25,
          id: 25,
        },
      ],
    };
  },
  methods: {
    shop: function () {},
  },
};
</script>

<style>
.card {
  margin-top: 2rem;
  width: 21rem;
  height: 23rem;
  background-color: rgb(79, 146, 197);
}
.image {
  width: 12rem;
  height: 12rem;
}
button {
  border-radius: 5rem;
  background-color: rgb(191, 236, 221);
}
button:hover {
  transform: scale(1.05);
  box-shadow: 0 10px 0.5rem rgba(0, 0, 0, 0.2);
}
.cards {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
}
.cart {
  background-color: rgb(255, 255, 255);
}
</style>