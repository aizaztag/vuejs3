<template>
  <!-- <Article id="1-d" :title="title" :kabab-case="kababCase" :likes="likes" :status="status"></Article> -->
   
  <!-- <button @click="showPopUP = true">Show Popup</button> -->
  <!-- <PopUp v-show="showPopUP" @close="showPopUP = false"></PopUp> -->
  
  <!-- <Slots>
    <template v-slot:header>
            <h1>Header</h1>
    </template>
    <template v-slot:default>
            <h1>content</h1>
    </template>
    <template v-slot:footer>
            <h1>footer</h1>
    </template>
  </Slots> -->
<!-- <SlotsProps>
  <template v-slot:main="SlotsProps">
        {{  SlotsProps.firstName }} {{  SlotsProps.lastName }}
  </template>
</SlotsProps>

<SlotsProps>
  <template v-slot:main="SlotsProps">
       {{  SlotsProps.lastName }}   {{  SlotsProps.firstName }}
  </template>
</SlotsProps> -->

<!-- <CustomComponent v-model="name"></CustomComponent> -->

<!-- tabs nav -->
<!-- <TabBar :activeTab="activeTab" @activeTab="tabToActive"></TabBar> -->

<!-- teleport -->
 <div class="container">
    <div class="content">
      <h1>My App</h1>
      <p>
        This is an example of how you might use Vue Teleport. I think it is a
        pretty neat API that is yet another awesome escape hatch that Vue
        provides for practical reasons. Sometimes you just need to render
        something completely outside the Vue component tree.
      </p>
      <button @click="showModal = true">Show Modal</button>
      <teleport to="#modal-root">
        <TeleportModal v-show="showModal" @close="showModal = false">
          This is the secret modal message!
        </TeleportModal>
      </teleport>
    </div>
  </div>
</template>

<script>
import Rendering from "./components/Rendering.vue";
import RBasic from "./components/RBasic.vue";
import ListRendering from "./components/ListRendering.vue";
import Methods from "./components/Methods.vue";
import FormHandling from "./components/FormHandling.vue";
import Computed from "./components/Computed.vue";
import watch from "./components/watch.vue";
import Greet from "./components/comp/Greet.vue";
import Article from "./components/comp/Article.vue";
import ComponentC from "./components/comp/ComponentC.vue";
import PopUp from "./components/comp/PopUp.vue";
import Slots from "./components/comp/Slots.vue";
import SlotsProps from "./components/comp/SlotsProps.vue";
import CustomComponent from "./components/comp/CustomComponent.vue";
import TabBar from "./components/comp/DynamicComponent/TabBar.vue";
import TeleportModal from "./components/comp/TeleportModal.vue";

export default {
  components: { TeleportModal },
  name: "App",
  data() {
    return {
      title: "Article",
      name: "Aizaz",
      title: "Article",
      likes: 2,
      status: false,
      kababCase: "camelCase",
      showPopUP: false,
      activeTab : 'TabA',
       showModal: false,
    };
  },
  methods:{
    tabToActive(tab){
        this.activeTab = tab
    }
  },
  provide() {
    return {
      username: this.name,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
