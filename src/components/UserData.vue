<template>
<section>
<form @submit.prevent="addData">
<input type="text" placeholder="Enter Name" v-model="enteredName"/>
<input type="text" placeholder="Enter Age" v-model="enteredAge"/>
<button>Set user Data</button>
</form>
</section>
</template>

<script>
export default
{
    emits:['set-data'],
    data(){
        return{
            enteredName:"",
            enteredAge:""
        };
    },
    methods:
    {
        addData()
        {
        this.$emit('set-data',this.enteredName,this.enteredAge);
        }
    }
}
</script>
