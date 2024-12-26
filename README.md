<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy New Year 2025!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to right, #f0f8ff, #dff6ff);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
        .container {
            background-color: #ffffff;
            border-radius: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 600px;
            padding: 30px;
            text-align: center;
            animation: fadeIn 2s ease-in-out;
        }
        h1 {
            color: #ff6347;
            font-size: 36px;
            animation: bounce 2s infinite alternate;
        }
        p {
            color: #333;
            font-size: 18px;
            margin: 20px 0;
        }
        .contact-info {
            background-color: #f8f8f8;
            padding: 20px;
            border-radius: 10px;
            margin-top: 30px;
            animation: slideIn 2s ease-out;
        }
        .contact-info h3 {
            color: #333;
            font-size: 24px;
        }
        .contact-info p {
            font-size: 16px;
            color: #555;
        }
        .footer {
            margin-top: 20px;
            font-size: 14px;
            color: #888;
            position: absolute;
            bottom: 20px;
            width: 100%;
            text-align: center;
        }
        .button {
            background-color: #ff6347;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #e04e2b;
        }
        .input-field {
            padding: 10px;
            font-size: 18px;
            margin-top: 20px;
            border-radius: 5px;
            border: 1px solid #ccc;
            width: 80%;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes bounce {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>🎉 Happy New Year 2025! 🎉</h1>
        <p>Wishing you a year filled with prosperity, joy, and good health. May 2025 bring all your dreams and aspirations to life!</p>
        
        <!-- Input Field for User Name (For normal page use) -->
        <input type="text" id="userName" class="input-field" placeholder="Apna naam daalein" />

        <button class="button" onclick="showWish()">Wish Karein</button>

        <div id="wishContainer" style="display: none;">
            <p id="wishText"></p>
        </div>
        
        <div class="contact-info">
            <h3>Contact Information:</h3>
            <p><strong>Name:</strong> Shubham Singh</p>
            <p><strong>Mobile Number:</strong> 9565932733, 7309910784</p>
            <p><strong>Address:</strong> Village and Post Chhatai Kalan, Shahganj, Jaunpur, Uttar Pradesh - 223101</p>
        </div>

    </div>

    <div class="footer">
        <p>&copy; 2025 Shubham Singh. All Rights Reserved.</p>
    </div>

    <script>
        // Array of Hindi New Year Wishes
        const wishes = [
            "नया साल आपके जीवन में ढेर सारी खुशियाँ लेकर आए। शुभ नव वर्ष!",
            "आपका हर दिन नई खुशियों से भरा हो। नव वर्ष की हार्दिक शुभकामनाएँ!",
            "नव वर्ष के इस पावन अवसर पर, आपके जीवन में खुशियाँ और सफलता का प्रकाश हो।",
            "आपका हर दिन सुनहरा हो, आपका हर कदम आगे बढ़े। नया साल खुशियों से भरा हो!",
            "नव वर्ष आपके जीवन में सुख, शांति और समृद्धि लेकर आए। शुभ नव वर्ष!"
        ];

        // Get the user name from the URL parameter if available
        const urlParams = new URLSearchParams(window.location.search);
        const urlName = urlParams.get('name');  // 'name' will be passed in the URL

        if (urlName) {
            document.getElementById("userName").value = urlName;
            showWish();
        }

        // Function to Show Random Wish
        function showWish() {
            const userName = document.getElementById("userName").value;
            if (userName.trim() === "") {
                alert("कृपया अपना नाम डालें!");
                return;
            }
            // Randomly select a wish
            const randomWish = wishes[Math.floor(Math.random() * wishes.length)];
            document.getElementById("wishText").innerText = `${userName} जी, ${randomWish}`;
            document.getElementById("wishContainer").style.display = "block";
        }
    </script>

</body>
</html>
