<template>
  <div>
    <h1>Welcome {{title2}}</h1>
    <input type="text" v-model="input1"/>
    <button type = "button" @click="getDate">get</button>
    <button type = "button" @click="setDate">set</button>
  </div>
</template>

<script>
export default {
    data(){
        return{
            title:"개발자의 품격",
            title2:"seoul",
            input1:"abcd",

        };
    },

    watch:{
        input1(){
            console.log(this.input1);
        }

    },
    methods:{
        getDate(){
            alert(this.input1);
        },
        setDate(){
            this.input1="12345";
        },
    },
    beforeCreate (){
        console.log("beforeCreate")
    },
    created(){
        console.log("created")
    },
    beforeMount(){
        console.log("beforeMount")
    },
    mounted(){
        console.log("mounted")
    },

    // 데이터가 체인지될때 재랜더링이 일어남 - beforeUpdate, updated 일어남
    beforeUpdate(){
        console.log("beforeUpdate")
    },
    updated(){
        console.log("updated")
    },
    beforeDestroy(){
        console.log("beforeDestroy")
    },
    destroyed(){
        console.log("destroyed")
    }

};
</script>
