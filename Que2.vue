<template>
  <div> 
    <b-form-input v-model="lowercase" ></b-form-input
    ><br/><br/>
    <b-form-input v-model="uppercase"></b-form-input>
  </div>
</template>
<script>
export default {
  name: "QuestIon2",
  data() {
    return {
      lowercase: "",
      uppercase: "",
    };
  },
  watch: {
    lowercase() {
      this.uppercase = this.lowercase.toUpperCase();
    },
  },
};
</script>
