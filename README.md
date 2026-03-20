<html>
<head>
    <title>Result</title>
 
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
            text-align: center;
        }
 
        h2 {
            margin-bottom: 20px;
        }
 
        .detail {
            text-align: left;
            margin-bottom: 10px;
            font-size: 16px;
        }
 
        .label {
            font-weight: bold;
        }
 
        .btn {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 15px;
            background-color:red;
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
 
        .btn:hover {
            background-color: #0056b3;
        }
    </style>
 
</head>
<body>
 
<div class="container">
 
      <h2> Student Details</h2>
        <div class="detail">
            <span class="label">Name:</span>${student.name}
        </div>  
 
         <div class="detail">
            <span class="label">Course:</span>${student.course}
        </div>  
        
        <div class="detail">
            <span class="label">Email:</span>${student.email}
        </div>  
        
        <a href="/form" class="btn">Back to Form</a>
</div>
 
</body>
</html>
 
 
 
 
 
 
 
 
 
 
