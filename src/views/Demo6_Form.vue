<template>
  <div id="demo6">
    <form v-on:submit.prevent="submit">

    <!-- First name -->
      <div>
        <label for="first_name">Firstname</label>
        <input type="text" name="first_name" v-model.trim="applicant.first_name" >
      </div>

    <!-- Last name -->
      <div>
        <label for="last_name">LastName</label>
        <input type="text" name="last_name" v-model.trim="applicant.last_name" />
      </div>

    <!-- Sex -->
      <div>
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />
        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>

      <!-- Age -->
      <div>
        <label for="age">Age</label>
        <input type="number" v-model.number="applicant.age" focus/>
      </div>

    <!-- course -->
      <div>
        <select name="courses" v-model="applicant.course">
            <option value="react">React</option>
            <option value="angular">Angular</option>
            <option value="vuejs">VueJs</option>
        </select>
      </div>

      <button type="button" @click="clear">Clear</button>
      <button type="submit">Submit</button>
    </form>

    <div :style="styObj">#Spy {{ JSON.stringify(applicant) }}</div>
  </div>
</template>

<script>
export default {
  name: "Demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "vuejs",
      },
      styObj: {
        marginTop: "16px",
        color: "red",
      },
    };
  },
  methods:{
      submit(/*event*/){
        //event.preventDefault(); // ใส่เพื่อไม่ให้ค่าใน input หายไป
        alert(JSON.stringify(this.applicant))  
      },
      clear(){
          this.applicant = {
              first_name:"",
              last_name:"",
              sex:"male",
              course: "vuejs",
              age : 0
          }
      },
      userDefault(){
        this.applicant = {
          first_name: "UNKNOWN",
          last_name: "UNKNOWN",
          sex: "male",
          course: "react",
          age: 10
        }
      }
  }
};
</script>

<style></style>
