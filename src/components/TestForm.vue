<template>
  <form id="test-form">
    <div id="header">
        <h1>Level 1</h1>
        <h2>Section 1</h2>
    </div>
    <div class="learner-section">
        <label>USERNAME</label>
        <input type="username" required v-model="username" placeholder="Enter your username">
    </div>
    <div class="instructions">
        <label>INSTRUCTIONS</label>
        <p>Please complete this test in 5 minutes. <br>Ask your coach for any questions you may have.</p>
    </div>
    <div class="questions">
        <label>QUESTIONS</label>
        <h4>(1) 1 &plus; 2 &equals;</h4>
        <p>
            <input type="radio" id="q1_a" name="q1" v-model="testResponse.q1" value="0">
            <label id="answers" for="q1_a">4</label>
        </p>
        <p>
            <input type="radio" id="q1_b" name="q1" v-model="testResponse.q1" value="00">
            <label id="answers" for="q1_b">2</label>
        </p>
        <p>
            <input type="radio" id="q1_c" name="q1" v-model="testResponse.q1" value="000">
            <label id="answers" for="q1_c">1</label>
        </p>
        <p>
            <input type="radio" id="q1_d" name="q1" v-model="testResponse.q1" value="1">
            <label id="answers" for="q1_d">3</label>
        </p>
    </div>
    <div class="coach-sections">
        <label>COACH SECTION</label> <br>
        <input type="coach_id" required v-model="coach_id" placeholder="COACH ID">
        <label>GRADE</label> <br>
        <select v-model="grade" required>
            <option value="grade_4">4</option>
            <option value="grade_5">5</option>
            <option value="grade_6">6</option>
            <option value="grade_7">7</option>
        </select>
        <input type="password" required v-model="password" placeholder="Password">
        
    </div>
  </form>
</template>

<script>
export default {
    data() {
        return {
            username: '',
            coach_id: '',
            password: '',
            grade: '',
            testResponse: []
        }
    }
}
</script>

<style>
form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}

</style>