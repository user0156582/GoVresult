<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Education Board Result - Demo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #e8f0fe;
      margin: 0;
      padding: 0;
    }
    .container {
      width: 400px;
      margin: 50px auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px #999;
    }
    h2 {
      text-align: center;
      color: #003366;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }
    select, input[type="text"] {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      margin-top: 15px;
      width: 100%;
      padding: 10px;
      background: #003366;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
    }
    .result {
      margin-top: 20px;
      padding: 15px;
      background: #d4edda;
      border: 1px solid #c3e6cb;
      color: #155724;
      border-radius: 5px;
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Education Board Result</h2>
    <label for="exam">Examination</label>
    <select id="exam">
      <option>SSC/Dakhil</option>
      <option>HSC/Alim</option>
      <option>JSC/JDC</option>
    </select>

    <label for="year">Year</label>
    <select id="year">
      <script>
        for (let i = 2025; i >= 2000; i--) {
          document.write(`<option>${i}</option>`);
        }
      </script>
    </select>

    <label for="board">Board</label>
    <select id="board">
      <option value="dhaka">Dhaka</option>
      <option value="rajshahi">Rajshahi</option>
      <option value="comilla">Comilla</option>
      <option value="barisal">Barisal</option>
      <option value="chittagong">Chittagong</option>
      <option value="dinajpur">Dinajpur</option>
      <option value="jessore">Jessore</option>
      <option value="sylhet">Sylhet</option>
      <option value="madrasah">Madrasah</option>
      <option value="tec">Technical</option>
    </select>

    <label for="roll">Roll</label>
    <input type="text" id="roll" placeholder="Enter your roll number">

    <label for="reg">Registration No</label>
    <input type="text" id="reg" placeholder="Enter registration number">

    <button onclick="showResult()">Submit</button>

    <div class="result" id="result">
      <strong>Result Found!</strong><br>
      Name: Rahim Uddin<br>
      Roll: 123456<br>
      GPA: 5.00<br>
      Board: Dhaka<br>
      Year: 2025
    </div>
  </div>

  <script>
    function showResult() {
      const resultBox = document.getElementById("result");
      resultBox.style.display = "block";
    }
  </script>
</body>
</html>
