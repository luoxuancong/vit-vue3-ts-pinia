 <template>
       
    <div>{{ userStore.name }}</div>
     
</template>

 <script lang="ts" setup>
import { useUserStore } from '@/store/user';

const userStore = useUserStore();
setTimeout(()=>{
  userStore.name = 'lxc'
},2000)
</script>