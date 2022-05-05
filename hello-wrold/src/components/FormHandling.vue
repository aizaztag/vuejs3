<template>
  <div class="">
    {{ JSON.stringify(formValues, null, 4) }}


    <form @submit.prevent="formSubmit">
      <div>
        <label>Name</label>
        <input v-model.trim.lazy="formValues.name" />
      </div>
      
       <div>
        <label>Age (number validated)</label>
        <input v-model.number="formValues.age.enter" type="number"/>
      </div>

      <div>
        <label>Country</label>
        <select v-model="formValues.country">
          <option>Pakistan</option>
          <option>China</option>
        </select>
      </div>

      <div>
        <label>Job Location</label>
        <select v-model="formValues.jobLocation" multiple>
          <option>Pakistan</option>
          <option>China</option>
          <option>HDf</option>
        </select>
      </div>

      <div>
        <label>Checkbox</label>
        <input
          type="checkbox"
          v-model="formValues.remoteWork"
          true-value="yes"
          false-value="no"
        />
      </div>

      <div>
        <label>Checkbox Group</label>

        <label>Html</label>
        <input type="checkbox" v-model="formValues.skillSet" value="HTML" />
        <label>CSS</label>
        <input type="checkbox" v-model="formValues.skillSet" value="CSS" />
      </div>
      
      <div>
        <label>Radio button</label>

        <label>Html</label>
        <input type="radio" v-model="formValues.experince" value="1-10" />
        <label>CSS</label>
        <input type="radio" v-model="formValues.experince" value="1-20" />
      </div>
      <button >Submit</button>
    </form>
  </div>
  <!--  -->
</template>

<script>
export default {
  name: "FormHandling",
  data() {
    return {
      formValues: {
        name: "erwr",
        age: "",
        country: "",
        jobLocation: [],
        remoteWork: "no",
        skillSet: [],
        experince: '',
      },
    };
  },
  methods:{
      formSubmit(){
          console.log('dsf' , this.formValues)
      }
  }
};
</script>
