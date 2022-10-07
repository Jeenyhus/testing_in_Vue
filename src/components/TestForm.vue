<template>
  <form id="test-form" @submit.prevent="handleSubmit">
    <div id="header">
        <img src="/images/edulution_logo.png" alt="edulution logo"> <br> <br> <br>
        <h1>Sample Test 1</h1>
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
            <input type="radio" id="q1_a" name="q1" ng-model="testResponse" value="0">
            <label for="q1_a">0</label>
        </p>
        <p>
            <input type="radio" id="q1_b" name="q1" ng-model="testResponse" value="00">
            <label for="q1_b">2</label>
        </p>
        <p>
            <input type="radio" id="q1_c" name="q1" ng-model="testResponse" value="000">
            <label for="q1_c">8</label>
        </p>
        <p>
            <input type="radio" id="q1_d" name="q1" ng-model="testResponse" value="1">
            <label for="q1_d">3</label>
        </p>
        <h4>(2) 2 &times; 4 &equals;</h4>
        <p>
            <input type="radio" id="q2_a" name="q2" ng-model="testResponse" value="1">
            <label for="q2_a">8</label>
        </p>
        <p>
            <input type="radio" id="q2_b" name="q2" ng-model="testResponse" value="00">
            <label for="q2_b">9</label>
        </p>
        <p>
            <input type="radio" id="q2_c" name="q2" ng-model="testResponse" value="000">
            <label for="q2_c">16</label>
        </p>
        <p>
            <input type="radio" id="q2_d" name="q2" ng-model="testResponse" value="0000">
            <label for="q2_d">24</label>
        </p>
        <h4>(3) 2 &plus; 18 &equals;</h4>
        <p>
            <input type="radio" id="q3_a" name="q3" ng-model="testResponse" value="0">
            <label for="q3_a">34</label>
        </p>
        <p>
            <input type="radio" id="q3_b" name="q3" ng-model="testResponse" value="00">
            <label for="q3_b">19</label>
        </p>
        <p>
            <input type="radio" id="q3_c" name="q3" ng-model="testResponse" value="1">
            <label for="q3_c">20</label>
        </p>
        <p>
            <input type="radio" id="q3_d" name="q3" ng-model="testResponse" value="0000">
            <label for="q3_d">36</label>
        </p>
        <h4>(4) 30 &minus; 10 &equals;</h4>
        <p>
            <input type="radio" id="q4_a" name="q4" ng-model="testResponse" value="0">
            <label for="q4_a">34</label>
        </p>
        <p>
            <input type="radio" id="q4_b" name="q4" ng-model="testResponse" value="00">
            <label for="q4_b">19</label>
        </p>
        <p>
            <input type="radio" id="q4_c" name="q4" ng-model="testResponse" value="1">
            <label for="q4_c">20</label>
        </p>
        <p>
            <input type="radio" id="q4_d" name="q4" ng-model="testResponse" value="0000">
            <label for="q4_d">36</label>
        </p>
        <h4>(5) 10 &times 10 &equals;</h4>
        <p>
            <input type="radio" id="q5_a" name="q5" ng-model="testResponse" value="0">
            <label for="q5_a">10</label>
        </p>
        <p>
            <input type="radio" id="q5_b" name="q5" ng-model="testResponse" value="1">
            <label for="q5_b">100</label>
        </p>
        <p>
            <input type="radio" id="q5_c" name="q5" ng-model="testResponse" value="000">
            <label for="q5_c">50</label>
        </p>
        <p>
            <input type="radio" id="q5_d" name="q5" ng-model="testResponse" value="0000">
            <label for="q5_d">1000</label>
        </p>
    </div>
    <div class="coach-sections">
        <div class="HeaderbannerLabel">COACH SECTION</div> <br>
        <input type="coach_id" required v-model="coach_id" placeholder="ZM.MM003"> <br>
        <label>GRADE</label> <br> <br>
        <select v-model="grade" required> <br>
            <option value="grade_4">4</option>
            <option value="grade_5">5</option>
            <option value="grade_6">6</option>
            <option value="grade_7">7</option>
        </select>
        <input type="password" required v-model="password" placeholder="Password">
        
    </div>
    <div class="submit"> <br>
        <button>SUBMIT</button>
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
            testResponse: null,
            passwordError: ''
        }
    },
    methods: {
        handleSubmit() {
            //portal password validation
            
        }
    }
}
</script>

<style>
    
body {
    background-color: rgb(179, 255, 179);
    font-family: Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
}
h1 {
    font-family: Roboto, RobotoDraft, Helvetica, Arial, sans-serif;
    color: #151515;
}
h3 {
    font-size: 20px;
    font-weight: normal;
    color: #151515;
}
form {
    max-width: 720px;
    margin: 15px auto;
    background: white;
    text-align: left;
    padding: 120px;
    border-radius: 10px;

}
img {
    width: 60%;
    padding-left: 20%;
    margin-top: ;
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
[type="radio"]:checked,
[type="radio"]:not(:checked) {
    position: absolute;
    left: -9999px;
}

[type="radio"]:checked+label,
[type="radio"]:not(:checked)+label {
    color: #444;
    cursor: pointer;
    display: inline-block;
    font-size: 15px;
    font-weight: 400;
    line-height: 20px;
    padding-left: 28px;
    position: relative;

}

[type="radio"]:checked+label:before,
[type="radio"]:not(:checked)+label:before {
    content: '';
    position: absolute;
    left: 1px;
    top: 1px;
    width: 15px;
    height: 15px;
    border: 1px solid #151515;
    border-radius: 100%;
    background: #fff;
}

[type="radio"]:checked+label:after,
[type="radio"]:not(:checked)+label:after {
    content: '';
    width: 11px;
    height: 11px;
    background: #0caf0c;
    border: 1px solid #0caf0c;
    position: absolute;
    top: 3px;
    left: 3px;
    border-radius: 100%;
    -webkit-transition: all 0.2s ease;
    transition: all 0.2s ease;
}

[type="radio"]:not(:checked)+label:after {
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
}

[type="radio"]:checked+label:after {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
}
button {
    background: #4586e7;
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
}
.submit {
    text-align: left;
}
</style>