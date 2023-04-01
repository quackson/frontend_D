<template>
  <div class="logo" style = "margin-top:10%;">
    <n-image
    width="100"
    src="imgUrl"
  	/>
  </div>
  <div class="description" style = "margin-top:5%;">
	  <n-gradient-text :size="24" type="warning" >这是一个GitHub多样化检索平台</n-gradient-text><br>
    <n-gradient-text :size="20" type="danger" >这是一个GitHub多样化检索平台</n-gradient-text><br>
    <n-gradient-text :size="16" type="info" >这是一个GitHub多样化检索平台</n-gradient-text><br>
  </div>
  <div style="width:40%;margin-left:30%;margin-top:20px;">
    <n-input size="large"  style = "margin-top:2%;align:center;" 
    round 
    placeholder="请输入">
      <template #suffix>
        <n-button quaternary @click="search">
          <template #icon>
            <n-icon><search-outline /></n-icon>
          </template>
        </n-button>
      </template>
    </n-input>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue';
import router from '@/router/index.js'
import { SearchOutline} from "@vicons/ionicons5";

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    SearchOutline
  },
  setup() {
    return {
      SearchOutline,
    };
  },
  data() {
    return {
        imgUrl:require("../assets/logo.jpg"),
    };
  },
  methods:{
    search(){
      this.$router.push('/about')
    }    
  }
}
</script>
