<script>
import { store } from '../data/store'
export default {
    name: 'Select',
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <div class="container">
        <select @click="$emit('selected')" v-model="store.selectArchetype" class="form-select" aria-label="Default select example">
            <option value="" selected>Archetype</option>
            <option
           v-for="(archetype,index) in store.archetypeList"
           :key="index" 
           :value="archetype"
           >
            {{archetype}}
           </option>
        </select>
    </div>
</template>



<style lang="scss" scoped>
select{
    width: 15%;
}


</style>