<template>
<div class="mt-2">
    
    <div class="container text-center">
        <div class="row">
            <div class="col-sm-3">
        <img :src="picture" :width="size" :height="size">
    </div>  


    <div class="col-sm-9">
        <div class="row">
        <p>ข้อมูล :</p>
        <ul>
        <p>ชื่อ-สกุล : {{ getFullname() }}</p>
        <p>ชื่อ :{{ firstname }}</p>
        <p>นามสกุล :{{ lastname }}</p>
        <p>ชื่อเล่น : {{ nickname }}</p>
        <p>อายุ :{{ age }}</p>
        <p>ที่อยู่ :<span v-html="address"></span></p>
        </ul>
        <p v-if ="hobby.length ===0">ไม่มีงานอดิเรก</p>
        <div v-else>
        <p>งานอดิเรก :</p>
        <ul>
            <li v-for="items in hobby">{{ items }}</li>
        </ul>
        </div>

        <p>ข้อมูลเพื่อนฐาน</p>
        <ul>
            <li v-for="(value,key) in general" :key="key">{{ key }} : {{ value }}</li>
        </ul>
        <button @click="showData">คลิกเพื่อดูข้อมูล</button>
        <button @click="increment(10)">เพิ่มค่า</button>
        <button @click="decrement(3)">ลดค่า</button>
    </div>
</div>  
</div>
</div>
</div>
</template>

<script>
export default{
    data(){
        return{
            firstname:"Karan",
            lastname: "Sannog",
            nickname: "Ton",
            age: 19,
            address: "21/10 หมู่4 ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            picture:"http://rms.tatc.ac.th/files/importpicstd/01/66309010002.jpg",
            size:300,
            hobby : ["ทำไร","ทำสวน","ทำนา"],
            general : {เพศ :"ชาย", น้ำหนัก :90, ส่วนสูง :170, โรคประจำตัว:false}
        }
    },
    methods:{
        getFullname(){
            return `${this.firstname} ${this.lastname}`
        },
        showData(){
            alert(this.firstname)
        },
        increment(value){
            this.age += value
        },
        decrement(value){
            this.age -= value
        },
        setNickName(event){
            this.nickname=event.target.value
        },
        submitForm(e){
            e.preventDefault();
            alert('บันทึกข้อมูลเรียยร้อย')
        }

    }
}
</script>