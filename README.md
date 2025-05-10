<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>کافه ما</title>
  <style>
    body {
      direction: rtl;
      font-family: 'Vazir', sans-serif;
      background-color: #f9f9f9;
      text-align: center;
      padding: 50px;
      color: #333;
    }
    form {
      background-color: #fff;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      display: inline-block;
    }
    input, button {
      font-size: 16px;
      padding: 10px;
      margin: 10px 0;
      width: 80%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      background-color: #4CAF50;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>
  <h2>به کافه ما خوش اومدی</h2>
  <form id="userForm">
    <label>اسمت چیه؟</label><br>
    <input type="text" id="name" required><br>

    <label>چند سالته؟</label><br>
    <input type="number" id="age" required><br>

    <button type="submit">ثبت</button>
  </form>

  <script>
    const form = document.getElementById('userForm');
    form.onsubmit = function(event) {
      event.preventDefault();
      const name = document.getElementById('name').value;
      const age = document.getElementById('age').value;

      // انتقال به صفحه جدید با اطلاعات در URL
      window.location.href = `result.html?name=${encodeURIComponent(name)}&age=${encodeURIComponent(age)}`;
    };
  </script>
</body>
</html>
