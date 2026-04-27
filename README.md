<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Billionaire Data City</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body class="bg-gray-100 font-sans">

    <div id="app" class="max-w-md mx-auto min-h-screen bg-white shadow-xl relative">
        
        <div id="auth-screen" class="p-8">
            <div class="text-center mt-10">
                <i class="fas fa-wallet text-6xl text-blue-900"></i>
                <h1 class="text-2xl font-bold mt-4 tracking-tight">BILLIONAIRE DATA CITY</h1>
                <p id="auth-subtitle" class="text-gray-500 text-sm">Create an account to start</p>
            </div>

            <div class="mt-10 space-y-4">
                <input type="text" id="reg-name" placeholder="Full Name" class="w-full p-4 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900">
                <div class="flex">
                    <span class="p-4 bg-gray-200 border border-r-0 rounded-l-lg">+233</span>
                    <input type="number" id="reg-phone" placeholder="Phone Number" class="w-full p-4 border rounded-r-lg focus:outline-none focus:ring-2 focus:ring-blue-900">
                </div>
                <input type="text" id="reg-location" placeholder="Location (Landmark/City)" class="w-full p-4 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-900">
                
                <button onclick="handleAuth()" class="w-full bg-blue-900 text-white p-4 rounded-lg font-bold hover:bg-blue-800 transition">REGISTER</button>
                
                <div class="text-center my-4 text-gray-400">OR</div>
                
                <button class="w-full border p-4 rounded-lg flex items-center justify-center space-x-2">
                    <i class="fab fa-google text-red-500"></i>
                    <span>Continue with Google</span>
                </button>
            </div>
        </div>

        <div id="admin-screen" class="hidden p-6">
            <div class="flex justify-between items-center border-b pb-4">
                <h2 class="text-xl font-bold">Admin Panel</h2>
                <span class="bg-blue-100 text-blue-800 text-xs font-semibold px-2.5 py-0.5 rounded">Owner</span>
            </div>
            <div class="mt-8 grid grid-cols-2 gap-4">
                <div onclick="showPostForm()" class="bg-blue-50 p-6 rounded-xl border border-blue-100 text-center cursor-pointer">
                    <i class="fas fa-plus-circle text-3xl text-blue-900"></i>
                    <p class="mt-2 font-bold text-sm">Post Items</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl border text-center">
                    <i class="fas fa-shopping-cart text-3xl text-gray-400"></i>
                    <p class="mt-2 font-bold text-sm text-gray-500">0 Orders</p>
                </div>
            </div>
        </div>

    </div>

    <script>
        // Simple logic to simulate "The Pro" experience
        function handleAuth() {
            const phone = document.getElementById('reg-phone').value;
            
            // IF THE PHONE NUMBER IS YOURS (Example: 0541234567)
            // It switches to your Admin Dashboard
            if(phone === "0541234567") { 
                document.getElementById('auth-screen').classList.add('hidden');
                document.getElementById('admin-screen').classList.remove('hidden');
                alert("Welcome back, Boss!");
            } else {
                alert("Registration Successful! OTP sent to +233" + phone);
            }
        }

        function showPostForm() {
            alert("Upload Form Opening... (Next step: Connect Firebase)");
        }
    </script>
</body>
</html>
