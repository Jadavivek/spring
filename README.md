<%@ taglib prefix="form" uri="http://www.springframework.org/tags/form" %>
 
<html>
<head>
    <title>Student Form</title>
 
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f8;
 
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
 
        .container {
            background: white;
            padding: 25px;
            width: 320px;
            border-radius: 10px;
            box-shadow: 0px 0px 15px rgba(0,0,0,0.2);
        }
 
        h2 {
            text-align: center;
            margin-bottom: 20px;
        }
 
        label {
            font-weight: bold;
        }
 
        input, select {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
 
        input[type="submit"] {
            background-color: green;
            color: white;
            border: none;
            cursor: pointer;
        }
 
        input[type="submit"]:hover {
            background-color: darkgreen;
        }
    </style>
 
</head>
<body>
 
<div class="container">
 
<h2>Student Registration Form</h2>
 
  <form:form action="result" method="post" modelAttribute="student">
    <label>Name:</label>
     <form:input path="name"/>
     
     <label>Name:</label>
     <form:input path="email"/>
     
       <label>Course:</label>
         <form:select path="course">
            <form:option value="Java" label="Java"/>
             <form:option value="Spring" label="Spring"/>
              <form:option value="Hibernate" label="Hibernate"/>
         </form:select>
         
         <input type="submit" value="Register">
  </form:form>
</div>
 
</body>
</html>
 
