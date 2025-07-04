
# HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Python Quizzes</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 800px;
      margin: auto;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: darkslateblue;
    }
    fieldset {
      margin-bottom: 20px;
      padding: 15px;
    }
    label {
      display: block;
      margin: 8px 0;
    }
  </style>
</head>
<body>

  <h1>Python Quizzes</h1>

  <!-- Question 1: Radio -->
  <fieldset>
    <legend>1. What does PIP stand for in Python?</legend>
    <label><input type="radio" name="q1" value="a"> Python Installation Program</label>
    <label><input type="radio" name="q1" value="b"> Package Installer for Python</label>
    <label><input type="radio" name="q1" value="c"> Python Integrated Package</label>
  </fieldset>

  <!-- Question 2: Text -->
  <fieldset>
    <legend>2. Which command is used to install a package using PIP?</legend>
    <label for="q2">Your Answer:</label>
    <input type="text" id="q2" name="q2" placeholder="e.g. pip install flask">
  </fieldset>

  <!-- Question 3: Number -->
  <fieldset>
    <legend>3. What version of pip is considered stable and recent? (Enter the version number)</legend>
    <label for="q3">Your Answer:</label>
    <input type="number" id="q3" name="q3" min="1" step="0.1" placeholder="e.g. 24.0">
  </fieldset>

  <!-- Question 4: Checkbox -->
  <fieldset>
    <legend>4. Which of the following can be done with pip? (Select all that apply)</legend>
    <label><input type="checkbox" name="q4" value="install"> Install packages</label>
    <label><input type="checkbox" name="q4" value="uninstall"> Uninstall packages</label>
    <label><input type="checkbox" name="q4" value="update-python"> Update Python itself</label>
    <label><input type="checkbox" name="q4" value="list"> List installed packages</label>
  </fieldset>

  <!-- Question 5: Select -->
  <fieldset>
    <legend>5. Which of these is the correct way to check the version of pip?</legend>
    <label for="q5">Choose one:</label>
    <select id="q5" name="q5">
      <option value="">--Select an option--</option>
      <option value="a">python pip --version</option>
      <option value="b">pip show</option>
      <option value="c">pip --version</option>
      <option value="d">pip check-version</option>
    </select>
  </fieldset>

  <!-- Bonus: Textarea -->
  <fieldset>
    <legend>6. Explain why PIP is important in Python development.</legend>
    <label for="q6">Your Answer:</label>
    <textarea id="q6" name="q6" rows="4" cols="50" placeholder="Write your thoughts here..."></textarea>
  </fieldset>

</body>
</html>


```