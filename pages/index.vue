<template>
  <div class="container">
    <div class="content">
      <div class="problems-section">
        <div class="problems">
          <div :key="problem.id" v-for="problem of problems" class="problem-item">
            <h2>{{ problem.problem_type.name }}</h2>
            <h3>Hoy | 02:00 PM</h3>
            <h3>{{ problem.location.name }} | {{ problem.location_space.name }}</h3>
            <div class="problem-state">
              <img src="" alt="">
              <h3>{{ problem.problem_state.name }}</h3>
              <h3>{{ problem.comments }}</h3>
            </div>
          </div>
      </div>
      <div class="problems-detail">

      </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      problems: []
    }
  },
  async created() {
    const uri = 'https://api-test.comunal.co/problem'
    const config = {
      headers: {
        'Access-Control-Allow-Origin': '*',
        'Content-Type': 'application/json',
        'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiZGVmYXVsdCIsImlzX2NvbXVuYWwiOmZhbHNlLCJpc3MiOiJ0ZXN0LmNvbXVuYWxjb3dvcmtpbmcuY29tIiwiaGFzX3BlbmRpbmdfaW52aXRhdGlvbiI6ZmFsc2UsImxvY2F0aW9uX2lkIjoibG9faWk0NTRpQUo1RjdEUTBwdCIsImhhc19mdWxsX3Byb2ZpbGUiOnRydWUsImJ1c2luZXNzX3R5cGUiOiJjb3dvcmtpbmciLCJleHAiOjE2MzM1NDAxODYsInVzZXIiOiJ1c19FejRURHJUQzRxRGxxaGliIiwiYnVzaW5lc3NfaWQiOiJjb211bmFsX2Nvd29ya2luZyIsImlhdCI6MTYwMjAwNDE4Niwib3V0bG9va19zeW5jZWQiOmZhbHNlLCJqdGkiOiJzZV9FOFVXenBLTjZVMnhmV2htIn0.gAFuHVvqRnETTfMX6WWW5uzegzkB5A84jc52NqzJ8zQ'
      }
    }
    try {
      const res = await axios.get(uri, config);
      
      console.log(res.data.data);
      this.problems = res.data.data;
    } catch (error) {
      console.log(error);
    }
  }
}
</script>
<style>
  .problems-section {
    display: flex;
    flex-wrap: wrap;
  }

    .problems {
      flex-grow: 1;
      background-color: #ffffff;
      box-shadow: 0 26px 40px -24px rgba(128, 152, 213, 0.15);
      border-radius: 20px;
    }

    .problem-item {
      padding: 20px 30px;
    }

    .problems-detail {
      flex-grow: 6;
    }

    .problem-state {
      display: flex;
      justify-content: space-between;
    }
</style>