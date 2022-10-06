<template>
  <form id="test-form">
    <div id="header">
        <h1>Level 1</h1>
        <h2>Section 1</h2>
    </div>
    <div class="learner-section">
        <div class="HeaderbannerLabel">USERNAME</div>
        <input type="username" required v-model="username" placeholder="Enter your username">
    </div> <br>
    
    <div class="instructions">
        <div class="HeaderbannerLabel">INSTRUCTIONS</div>
        <p>Please complete this test in 5 minutes. <br>Ask your coach for any questions you may have.</p>
    </div>
    <div class="questions">
        <div class="HeaderbannerLabel">QUESTIONS</div>
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
        <div class="HeaderbannerLabel">COACH SECTION</div> <br>
        <input type="coach_id" required v-model="coach_id" placeholder="COACH ID"> <br>
        <label>GRADE</label> <br> <br>
        <select v-model="grade" required> <br>
            <option value="grade_4">4</option>
            <option value="grade_5">5</option>
            <option value="grade_6">6</option>
            <option value="grade_7">7</option>
        </select>
        <input type="password" required v-model="password" placeholder="ZM.MM003">
        
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
    margin: 15px auto;
    background: white;
    text-align: left;
    padding: 120px;
    border-radius: 10px;
}
.username {
    border: 0px;
    border-bottom: 1px solid #c0c0c0;
    width: 40%;
    flex-shrink: 1;
    background-color: transparent;
    display: block;
    font: 400 16px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
    height: 24px;
    line-height: 24px;
    margin: 0;
    min-width: 0%;
    outline: none;
    padding: 0;
    z-index: 0;
}
.HeaderbannerLabel {
    background-color: rgb(21, 187, 43);
    color: rgba(255, 255, 255, 1);
    font-size: 20px;
    font-weight: 500;
    font: 400 16px/24px Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
    padding: 8px 8px 8px 34px;
    margin-top: 30px;
    margin-bottom: 25px;
    width: 45%;
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