# Ridelens <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vehicle Rating System</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: linear-gradient(135deg, #2c3e50, #4a6491);
            color: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .description {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .rating-form {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }
        
        .form-title {
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
        }
        
        input, select, textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        .rating-input {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .rating-input input {
            width: 80px;
            text-align: center;
        }
        
        .rating-scale {
            color: #666;
            font-size: 14px;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        .ratings-list {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .ratings-title {
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
        }
        
        .rating-item {
            padding: 15px;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .rating-item:last-child {
            border-bottom: none;
        }
        
        .vehicle-info {
            flex: 1;
        }
        
        .vehicle-name {
            font-weight: 600;
            font-size: 18px;
            color: #2c3e50;
        }
        
        .vehicle-type {
            color: #7f8c8d;
            font-size: 14px;
        }
        
        .rating-value {
            font-size: 24px;
            font-weight: 700;
            color: #e74c3c;
            min-width: 80px;
            text-align: center;
        }
        
        .comment {
            margin-top: 10px;
            color: #34495e;
            font-style: italic;
        }
        
        .no-ratings {
            text-align: center;
            color: #7f8c8d;
            padding: 20px;
        }
        
        .stats {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
            text-align: center;
        }
        
        .stat-box {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            flex: 1;
            margin: 0 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        
        .stat-value {
            font-size: 24px;
            font-weight: 700;
            color: #3498db;
        }
        
        .stat-label {
            color: #7f8c8d;
            font-size: 14px;
        }
        
        @media (max-width: 768px) {
            .rating-item {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .rating-value {
                margin-top: 10px;
                align-self: flex-end;
            }
            
            .stats {
                flex-direction: column;
            }
            
            .stat-box {
                margin: 10px 0;
            }
