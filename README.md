<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>PromoConnect</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI', sans-serif;
}

body{
    margin:0;
    background:#0b0f1a;
    color:white;
}

/* COLORS */
:root{
    --blue:#3b82f6;
    --blue-dark:#2563eb;
    --card:#111827;
    --border:#1f2937;
}

/* LAYOUT */
.layout{
    display:flex;
    min-height:100vh;
}

/* LEFT SIDE */
.left{
    flex:1;
    background:linear-gradient(135deg,#0f172a,#0b0f1a);
    display:flex;
    flex-direction:column;
    justify-content:center;
    padding:60px;
    border-right:1px solid var(--border);
}

.brand-logo{
    width:80px;
    height:80px;
    border-radius:20px;
    background:var(--blue);
    display:flex;
    align-items:center;
    justify-content:center;
    margin-bottom:20px;
}

.brand-title{
    font-size:36px;
    font-weight:800;
    margin:0;
}

.brand-title span{
    color:var(--blue);
}

.brand-text{
    color:#94a3b8;
    margin-top:10px;
    max-width:420px;
    line-height:1.6;
}

/* RIGHT SIDE */
.right{
    flex:1;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.container{
    width:100%;
    max-width:450px;
    background:var(--card);
    padding:24px;
    border-radius:16px;
    border:1px solid var(--border);
    box-shadow:0 10px 30px rgba(0,0,0,0.5);
}

/* SCREENS */
.screen{
    display:none;
    animation:fade .4s ease;
}

.active{
    display:block;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(10px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* TEXT */
h1{
    color:white;
    margin-bottom:10px;
}

h2{
    color:var(--blue);
    margin:18px 0 8px;
    font-size:18px;
}

p{
    color:#cbd5e1;
    line-height:1.6;
    font-size:14px;
}

.list{
    margin-top:10px;
    color:#cbd5e1;
    line-height:1.8;
    font-size:14px;
}

/* BUTTONS */
.button-group{
    display:flex;
    gap:10px;
    margin-top:20px;
}

button{
    flex:1;
    border:none;
    padding:12px;
    border-radius:12px;
    cursor:pointer;
    font-weight:bold;
    transition:.3s;
}

.primary-btn{
    background:var(--blue);
    color:white;
}

.primary-btn:hover{
    background:var(--blue-dark);
}

.secondary-btn{
    background:#1e293b;
    color:white;
}

/* INPUTS */
input, select{
    width:100%;
    padding:12px;
    margin:8px 0;
    border-radius:10px;
    border:1px solid var(--border);
    background:#0f172a;
    color:white;
    outline:none;
}

input::placeholder{
    color:#64748b;
}

/* TABS */
.tabs{
    display:flex;
    gap:10px;
    margin-bottom:18px;
}

.tab{
    flex:1;
    text-align:center;
    padding:10px;
    border-radius:10px;
    cursor:pointer;
    font-weight:bold;
    background:#0f172a;
    border:1px solid var(--border);
    color:#94a3b8;
}

.tab.active-tab{
    background:var(--blue);
    color:white;
}

.hidden{
    display:none;
}

/* MOBILE */
@media(max-width:900px){

    .layout{
        flex-direction:column;
    }

    .left{
        padding:35px;
        text-align:center;
    }

    .brand-text{
        margin:auto;
    }
}

</style>
</head>

<body>

<div class="layout">

    <!-- LEFT -->
    <div class="left">

        <div class="brand-logo">
            <svg width="40" height="40" viewBox="0 0 24 24" fill="none">
                <path d="M6 6H4" stroke="white" stroke-width="2"/>
                <path d="M4 6L6 14C6.5 16 8 17 10 17H16C18 17 19.5 16 20 14L22 8H6" stroke="white" stroke-width="2"/>
                <path d="M9 21C9.5 21 10 20.5 10 20C10 19.5 9.5 19 9 19C8.5 19 8 19.5 8 20C8 20.5 8.5 21 9 21Z" stroke="white"/>
                <path d="M17 21C17.5 21 18 20.5 18 20C18 19.5 17.5 19 17 19C16.5 19 16 19.5 16 20C16 20.5 16.5 21 17 21Z" stroke="white"/>
            </svg>
        </div>

        <h1 class="brand-title">Promo<span>Connect</span></h1>

        <p class="brand-text">
            Helping Small Businesses Connect, Promote, and Grow.
        </p>

    </div>

    <!-- RIGHT -->
    <div class="right">

        <div class="container">

            <!-- SCREEN 1 -->
            <div class="screen active" id="screen1">

                <h1>PromoConnect</h1>

                <p>
                    Mobile Application
                </p>

                <p>
                    Helping Small Businesses Connect, Promote, and Grow
                </p>

                <div class="button-group">
                    <button class="primary-btn" onclick="showScreen('screen2')">
                        Next
                    </button>
                </div>

            </div>

            <!-- SCREEN 2 -->
            <div class="screen" id="screen2">

                <h1>Group 2</h1>

                <div class="list">
                    • Caranay, John Reinier P.<br>
                    • Chico, Ronianne Kim<br>
                    • Dela Cruz, Janelle Anne R.<br>
                    • Regalado, Wendel Mark G.<br>
                    • Lopez, Khenji T.
                </div>

                <div class="button-group">
                    <button class="secondary-btn" onclick="showScreen('screen1')">
                        Back
                    </button>

                    <button class="primary-btn" onclick="showScreen('screen3')">
                        Next
                    </button>
                </div>

            </div>

            <!-- SCREEN 3 -->
            <div class="screen" id="screen3">

                <h1>What the App Does</h1>

                <p>
                    PromoConnect is a mobile and web application that helps users discover nearby promotions, discounts, rewards, and special deals from local small businesses. It also allows customers to claim promos, earn loyalty points, and communicate directly with businesses through the platform.
                </p>

                <h2>Target Users</h2>

                <div class="list">
                    • Students<br>
                    • Young professionals<br>
                    • Working adults<br>
                    • Budget-conscious consumers<br>
                    • Small business owners such as cafés, food stalls, retail shops, salons, and online sellers
                </div>

                <h2>Business Problem It Solves</h2>

                <p>
                    Many small businesses struggle to attract customers, promote their products effectively, and compete with larger brands due to limited marketing budgets. At the same time, customers often find it difficult to discover affordable deals and trusted local promotions. PromoConnect solves this by connecting businesses with potential customers in one digital platform.
                </p>

                <h2>Why It Is Useful</h2>

                <p>
                    PromoConnect is useful because it helps customers save money while discovering nearby businesses and rewards. For businesses, it provides an affordable way to promote offers, increase visibility, attract repeat customers, and monitor campaign performance through analytics.
                </p>

                <div class="button-group">
                    <button class="secondary-btn" onclick="showScreen('screen2')">
                        Back
                    </button>

                    <button class="primary-btn" onclick="showScreen('signupScreen')">
                        Continue
                    </button>
                </div>

            </div>

            <!-- SIGN UP SCREEN -->
            <div class="screen" id="signupScreen">

                <div class="tabs">
                    <div class="tab active-tab" id="customerTab" onclick="showTab('customer')">
                        Customer
                    </div>

                    <div class="tab" id="adminTab" onclick="showTab('admin')">
                        Admin
                    </div>
                </div>

                <!-- CUSTOMER -->
                <div id="customerSection">

                    <h1>Create Customer Account</h1>

                    <p>
                        Join promos and earn rewards instantly.
                    </p>

                    <input type="text" placeholder="Full Name">
                    <input type="email" placeholder="Email Address">
                    <input type="password" placeholder="Password">

                    <select>
                        <option>Preferred Category</option>
                        <option>Food</option>
                        <option>Drinks</option>
                        <option>Coffee</option>
                    </select>

                    <div class="button-group">
                        <button class="secondary-btn" onclick="showScreen('screen3')">
                            Back
                        </button>

                        <button class="primary-btn" onclick="register('Customer')">
                            Sign Up
                        </button>
                    </div>

                </div>

                <!-- ADMIN -->
                <div id="adminSection" class="hidden">

                    <h1>Create Admin Account</h1>

                    <p>
                        Promote your shop and attract customers.
                    </p>

                    <input type="text" placeholder="Business Name">
                    <input type="text" placeholder="Owner Name">
                    <input type="email" placeholder="Business Email">
                    <input type="password" placeholder="Password">
                    <input type="text" placeholder="Business Address">

                    <select>
                        <option>Business Category</option>
                        <option>Restaurant</option>
                        <option>Cafe</option>
                        <option>Retail Shop</option>
                    </select>

                    <div class="button-group">
                        <button class="secondary-btn" onclick="showScreen('screen3')">
                            Back
                        </button>

                        <button class="primary-btn" onclick="register('Admin')">
                            Sign Up
                        </button>
                    </div>

                </div>

            </div>

        </div>

    </div>

</div>

<script>

/* SCREEN FUNCTION */
function showScreen(id){

    const screens = document.querySelectorAll('.screen');

    screens.forEach(screen => {
        screen.classList.remove('active');
    });

    document.getElementById(id).classList.add('active');
}

/* TAB FUNCTION */
function showTab(type){

    document.getElementById('customerSection').classList.add('hidden');
    document.getElementById('adminSection').classList.add('hidden');

    document.getElementById('customerTab').classList.remove('active-tab');
    document.getElementById('adminTab').classList.remove('active-tab');

    if(type === 'customer'){

        document.getElementById('customerSection').classList.remove('hidden');
        document.getElementById('customerTab').classList.add('active-tab');

    } else {

        document.getElementById('adminSection').classList.remove('hidden');
        document.getElementById('adminTab').classList.add('active-tab');
    }
}

/* SIGN UP */
function register(type){

    alert(type + " Account Successfully Created!");

}

</script>

</body>
</html>
