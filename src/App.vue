<template>
<div>
<active-user :userName="user.name" :userAge="user.age"></active-user>
<user-data @set-data="setData"></user-data>
</div>
</template>
<script>
export default
{
    data(){
        return{
            user:{ name:"chinar" ,age :35}

        };


    },
    methods:
    {
    setData(name,age)
    {
        this.user={
                name:name,
                age:+age
            };
    }
    }

};
</script>
<style>
html {
  font-family: sans-serif;
}

section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem;
}
</style>