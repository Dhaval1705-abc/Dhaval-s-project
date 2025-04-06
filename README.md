<!DOCTYPE html>
<html lang="en">
<head>

<style>
/* Global Styles */
:root {
    --primary-color: #4CAF50;
    --secondary-color: #2E7D32;
    --accent-color: #8BC34A;
    --dark-color: #333;
    --light-color: #f9f9f9;
    --gray-color: #777;
    --danger-color: #f44336;
    --warning-color: #ff9800;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--dark-color);
    background-color: #f5f5f6;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}

/* Typography */
h1, h2, h3, h4, h5, h6 {
    margin-bottom: 1rem;
    font-weight: 600;
}

h1 {
    font-size: 2.5rem;
}

h2 {
    font-size: 2rem;
    margin-bottom: 1.5rem;
}

p {
    margin-bottom: 1rem;
}

a {
    text-decoration: none;
    color: var(--primary-color);
}

/* Buttons */
.btn {
    display: inline-block;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn-primary {
    background-color: var(--primary-color);
    color: white;
}

.btn-primary:hover {
    background-color: var(--secondary-color);
}

.btn-secondary {
    background-color: white;
    color: var(--primary-color);
    border: 1px solid var(--primary-color);
}

.btn-secondary:hover {
    background-color: var(--primary-color);
    color: white;
}

.btn-large {
    padding: 12px 30px;
    font-size: 1.1rem;
}

/* Header */
header {
    background-color: white;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;
}

.logo i {
    font-size: 2rem;
    color: var(--primary-color);
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 20px;
}

nav a {
    color: var(--dark-color);
    font-weight: 500;
    padding: 5px 0;
    position: relative;
}

nav a.active {
    color: var(--primary-color);
}

nav a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--primary-color);
    transition: width 0.3s ease;
}

nav a:hover::after {
    width: 100%;
}

/* Hero Section */
.hero {
    padding: 120px 0 80px;
    background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
}

.hero .container {
    display: flex;
    align-items: center;
    gap: 50px;
}

.hero-content {
    flex: 1;
}

.hero-image {
    flex: 1;
}

.hero-image img {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.hero h2 {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
    color: var(--dark-color);
}

.hero p {
    font-size: 1.1rem;
    margin-bottom: 2rem;
    color: var(--gray-color);
}

/* How It Works Section */
.how-it-works {
    padding: 80px 0;
    background-color: white;
    text-align: center;
}

.steps {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 40px;
}

.step {
    flex: 1;
    min-width: 200px;
    padding: 30px 20px;
    background-color: var(--light-color);
    border-radius: 10px;
    transition: transform 0.3s ease;
}

.step:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.step-number {
    width: 40px;
    height: 40px;
    background-color: var(--primary-color);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 15px;
    font-weight: bold;
}

.step i {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 15px;
}

.step h3 {
    margin-bottom: 10px;
}

/* Rewards Preview Section */
.rewards-preview {
    padding: 80px 0;
    background-color: var(--light-color);
    text-align: center;
}

.rewards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 25px;
    margin: 40px 0;
}

.reward-card {
    background-color: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}

.reward-card:hover {
    transform: translateY(-5px);
}

.reward-image {
    height: 180px;
    background-color: #eee;
    display: flex;
    align-items: center;
    justify-content: center;
}

.reward-image i {
    font-size: 4rem;
    color: var(--gray-color);
}

.reward-info {
    padding: 20px;
}

.reward-info h3 {
    margin-bottom: 10px;
}

.reward-points {
    color: var(--primary-color);
    font-weight: bold;
    margin-bottom: 15px;
}

.reward-btn {
    width: 100%;
}

/* Impact Section */
.impact {
    padding: 60px 0;
    background-color: var(--primary-color);
    color: white;
    text-align: center;
}

.impact-stats {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 20px;
}

.stat {
    padding: 20px;
}

.stat h3 {
    font-size: 2.5rem;
    margin-bottom: 5px;
}

/* Footer */
footer {
    background-color: var(--dark-color);
    color: white;
    padding: 60px 0 0;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 40px;
    margin-bottom: 40px;
}

.footer-section {
    flex: 1;
    min-width: 250px;
}

.footer-section h3 {
    margin-bottom: 20px;
    position: relative;
    padding-bottom: 10px;
}

.footer-section h3::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 50px;
    height: 2px;
    background-color: var(--primary-color);
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 10px;
}

.footer-section ul li a {
    color: #ccc;
    transition: color 0.3s ease;
}

.footer-section ul li a:hover {
    color: white;
}

.social-icons {
    display: flex;
    gap: 15px;
    margin-top: 20px;
}

.social-icons a {
    color: white;
    font-size: 1.2rem;
    transition: color 0.3s ease;
}

.social-icons a:hover {
    color: var(--accent-color);
}

.footer-bottom {
    text-align: center;
    padding: 20px 0;
    border-top: 1px solid #444;
}

/* Modals */
.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 2000;
    overflow-y: auto;
}

.modal-content {
    background-color: white;
    margin: 5% auto;
    padding: 30px;
    border-radius: 8px;
    width: 90%;
    max-width: 600px;
    position: relative;
    animation: modalopen 0.5s;
}

@keyframes modalopen {
    from {
        opacity: 0;
        transform: translateY(-50px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.close {
    position: absolute;
    top: 15px;
    right: 15px;
    font-size: 1.5rem;
    cursor: pointer;
    color: var(--gray-color);
}

.close:hover {
    color: var(--dark-color);
}

/* Forms */
.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: 500;
}

.form-group input,
.form-group select,
.form-group textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 1rem;
}

.form-group textarea {
    min-height: 100px;
    resize: vertical;
}

/* Responsive Design */
@media (max-width: 768px) {
    header .container {
        flex-direction: column;
        text-align: center;
    }

    nav ul {
        margin-top: 15px;
        flex-wrap: wrap;
        justify-content: center;
    }

    .hero .container {
        flex-direction: column;
    }

    .hero-content {
        text-align: center;
        margin-bottom: 30px;
    }

    .steps {
        flex-direction: column;
    }

    .impact-stats {
        flex-direction: column;
    }
}
</style>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoCycle - E-Waste Management</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">
                <i class="fas fa-recycle"></i>
                <h1>EcoCycle</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active">Home</a></li>
                    <li><a href="#how-it-works">How It Works</a></li>
                    <li><a href="#rewards">Rewards</a></li>
                    <li><a href="#about">About</a></li>
                    <li><button id="loginBtn" class="btn">Login</button></li>
                    <li><button id="registerBtn" class="btn btn-primary">Register</button></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h2>Recycle Your E-Waste, Earn Rewards</h2>
                    <p>Responsibly dispose of your electronic waste and get rewarded with points redeemable for electronics and gadgets.</p>
                    <button id="schedulePickupBtn" class="btn btn-primary btn-large">Schedule a Pickup</button>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="E-Waste Recycling">
                </div>
            </div>
        </section>

        <section id="how-it-works" class="how-it-works">
            <div class="container">
                <h2>How It Works</h2>
                <div class="steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <i class="fas fa-user-plus"></i>
                        <h3>Register</h3>
                        <p>Create your free account in minutes</p>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <i class="fas fa-laptop"></i>
                        <h3>Submit E-Waste</h3>
                        <p>Tell us what you want to recycle</p>
                    </div>
                    <div class="step">
                        <div class="step-number">3</div>
                        <i class="fas fa-calendar-alt"></i>
                        <h3>Schedule Pickup</h3>
                        <p>Choose a convenient time for collection</p>
                    </div>
                    <div class="step">
                        <div class="step-number">4</div>
                        <i class="fas fa-gift"></i>
                        <h3>Get Rewards</h3>
                        <p>Earn points redeemable for electronics</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="rewards" class="rewards-preview">
            <div class="container">
                <h2>Redeem Your Points</h2>
                <p>Earn EcoPoints for every e-waste item you recycle and redeem them for exciting rewards.</p>
                <div class="rewards-grid">
                    <!-- Rewards will be populated by JavaScript -->
                </div>
                <button id="viewAllRewardsBtn" class="btn btn-secondary">View All Rewards</button>
            </div>
        </section>

        <section class="impact">
            <div class="container">
                <div class="impact-stats">
                    <div class="stat">
                        <h3>12,548</h3>
                        <p>Items Recycled</p>
                    </div>
                    <div class="stat">
                        <h3>8,742</h3>
                        <p>Users Registered</p>
                    </div>
                    <div class="stat">
                        <h3>3,215</h3>
                        <p>Rewards Redeemed</p>
                    </div>
                    <div class="stat">
                        <h3>28,450</h3>
                        <p>Points Awarded</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Modals -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Login to Your Account</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="loginEmail">Email</label>
                    <input type="email" id="loginEmail" required>
                </div>
                <div class="form-group">
                    <label for="loginPassword">Password</label>
                    <input type="password" id="loginPassword" required>
                </div>
                <button type="submit" class="btn btn-primary">Login</button>
            </form>
            <p>Don't have an account? <a href="#" id="switchToRegister">Register here</a></p>
        </div>
    </div>

    <div id="registerModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Create Your Account</h2>
            <form id="registerForm">
                <div class="form-group">
                    <label for="registerName">Full Name</label>
                    <input type="text" id="registerName" required>
                </div>
                <div class="form-group">
                    <label for="registerEmail">Email</label>
                    <input type="email" id="registerEmail" required>
                </div>
                <div class="form-group">
                    <label for="registerPassword">Password</label>
                    <input type="password" id="registerPassword" required>
                </div>
                <div class="form-group">
                    <label for="registerPhone">Phone Number</label>
                    <input type="tel" id="registerPhone" required>
                </div>
                <button type="submit" class="btn btn-primary">Register</button>
            </form>
            <p>Already have an account? <a href="#" id="switchToLogin">Login here</a></p>
        </div>
    </div>

    <div id="pickupModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Schedule Your E-Waste Pickup</h2>
            <form id="pickupForm">
                <div class="form-group">
                    <label for="ewasteType">E-Waste Type</label>
                    <select id="ewasteType" required>
                        <option value="">Select Type</option>
                        <option value="laptop">Laptop/Computer</option>
                        <option value="phone">Mobile Phone</option>
                        <option value="tv">TV/Monitor</option>
                        <option value="appliance">Home Appliance</option>
                        <option value="battery">Batteries</option>
                        <option value="other">Other</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="ewasteCondition">Condition</label>
                    <select id="ewasteCondition" required>
                        <option value="">Select Condition</option>
                        <option value="working">Working</option>
                        <option value="repairable">Repairable</option>
                        <option value="scrap">Scrap/Not Working</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="ewasteQuantity">Quantity</label>
                    <input type="number" id="ewasteQuantity" min="1" value="1" required>
                </div>
                <div class="form-group">
                    <label for="pickupDate">Pickup Date</label>
                    <input type="date" id="pickupDate" required>
                </div>
                <div class="form-group">
                    <label for="pickupTime">Pickup Time</label>
                    <select id="pickupTime" required>
                        <option value="">Select Time Slot</option>
                        <option value="morning">9:00 AM - 12:00 PM</option>
                        <option value="afternoon">1:00 PM - 4:00 PM</option>
                        <option value="evening">5:00 PM - 8:00 PM</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="pickupAddress">Pickup Address</label>
                    <textarea id="pickupAddress" rows="3" required></textarea>
                </div>
                <div class="form-group">
                    <label for="ewastePhotos">Upload Photos (Optional)</label>
                    <input type="file" id="ewastePhotos" multiple accept="image/*">
                </div>
                <button type="submit" class="btn btn-primary">Schedule Pickup</button>
            </form>
        </div>
    </div>

    <div id="rewardModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>Redeem Your Reward</h2>
            <div id="rewardDetails">
                <!-- Reward details will be populated by JavaScript -->
            </div>
            <form id="redeemForm">
                <div class="form-group">
                    <label for="shippingAddress">Shipping Address</label>
                    <textarea id="shippingAddress" rows="3" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Redeem Now</button>
            </form>
        </div>
    </div>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>EcoCycle</h3>
                    <p>Making e-waste recycling simple and rewarding.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#how-it-works">How It Works</a></li>
                        <li><a href="#rewards">Rewards</a></li>
                        <li><a href="#about">About Us</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-envelope"></i> info@ecocycle.com</p>
                    <p><i class="fas fa-phone"></i> +1 (555) 123-4567</p>
                    <p><i class="fas fa-map-marker-alt"></i> 123 Green St, Eco City</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 EcoCycle. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
document.addEventListener('DOMContentLoaded', function() {
    // DOM Elements
    const loginBtn = document.getElementById('loginBtn');
    const registerBtn = document.getElementById('registerBtn');
    const schedulePickupBtn = document.getElementById('schedulePickupBtn');
    const viewAllRewardsBtn = document.getElementById('viewAllRewardsBtn');
    const switchToRegister = document.getElementById('switchToRegister');
    const switchToLogin = document.getElementById('switchToLogin');
    
   // Modals
    const loginModal = document.getElementById('loginModal');
    const registerModal = document.getElementById('registerModal');
    const pickupModal = document.getElementById('pickupModal');
    const rewardModal = document.getElementById('rewardModal');
    
  
    const loginForm = document.getElementById('loginForm');
    const registerForm = document.getElementById('registerForm');
    const pickupForm = document.getElementById('pickupForm');
    const redeemForm = document.getElementById('redeemForm');
    
    
    const rewardsGrid = document.querySelector('.rewards-grid');
    
    
    const closeButtons = document.querySelectorAll('.close');
    
    
    const rewards = [
        {
            id: 1,
            name: "Wireless Earbuds",
            description: "Premium quality wireless earbuds with 20hrs battery life",
            points: 1500,
            category: "audio",
            icon: "fas fa-headphones"
        },
        {
            id: 2,
            name: "Smart Watch",
            description: "Fitness tracker with heart rate monitor and notifications",
            points: 3000,
            category: "wearables",
            icon: "fas fa-clock"
        },
        {
            id: 3,
            name: "Bluetooth Speaker",
            description: "Portable waterproof speaker with 10hrs playtime",
            points: 2000,
            category: "audio",
            icon: "fas fa-volume-up"
        },
        {
            id: 4,
            name: "Power Bank",
            description: "10000mAh fast charging portable battery",
            points: 1000,
            category: "accessories",
            icon: "fas fa-battery-full"
        }
    ];
    
    
    function displayRewards() {
        rewardsGrid.innerHTML = '';
        rewards.forEach(reward => {
            const rewardCard = document.createElement('div');
            rewardCard.className = 'reward-card';
            rewardCard.innerHTML = `
                <div class="reward-image">
                    <i class="${reward.icon}"></i>
                </div>
                <div class="reward-info">
                    <h3>${reward.name}</h3>
                    <p>${reward.description}</p>
                    <div class="reward-points">${reward.points} EcoPoints</div>
                    <button class="btn btn-primary reward-btn" data-id="${reward.id}">Redeem</button>
                </div>
            `;
            rewardsGrid.appendChild(rewardCard);
        });
        
        
        document.querySelectorAll('.reward-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const rewardId = parseInt(this.getAttribute('data-id'));
                showRewardDetails(rewardId);
            });
        });
    }
    
    
    function showRewardDetails(rewardId) {
        const reward = rewards.find(r => r.id === rewardId);
        if (reward) {
            const rewardDetails = document.getElementById('rewardDetails');
            rewardDetails.innerHTML = `
                <div class="reward-detail">
                    <div class="reward-image-large">
                        <i class="${reward.icon}"></i>
                    </div>
                    <div class="reward-info-large">
                        <h3>${reward.name}</h3>
                        <p>${reward.description}</p>
                        <div class="reward-points-large">${reward.points} EcoPoints</div>
                    </div>
                </div>
            `;
            rewardModal.style.display = 'block';
        }
    }
    
    
    function calculatePoints(type, condition, quantity) {
        const basePoints = {
            'laptop': 40,
            'phone': 30,
            'tv': 25,
            'appliance': 20,
            'battery': 50,
            'other': 15
        };
        
        const conditionMultiplier = {
            'working': 1.5,
            'repairable': 1.2,
            'scrap': 1.0
        };
        
        const base = basePoints[type] || 15;
        const multiplier = conditionMultiplier[condition] || 1.0;
        
        return Math.round(base * multiplier * quantity);
    }
    
    
    function showModal(modal) {
        modal.style.display = 'block';
        document.body.style.overflow = 'hidden';
    }
    
    // Hide modal function
    function hideModal(modal) {
        modal.style.display = 'none';
        document.body.style.overflow = 'auto';
    }
    
    // Event listeners for buttons
    loginBtn.addEventListener('click', () => showModal(loginModal));
    registerBtn.addEventListener('click', () => showModal(registerModal));
    schedulePickupBtn.addEventListener('click', () => showModal(pickupModal));
    viewAllRewardsBtn.addEventListener('click', () => alert('All rewards page coming soon!'));
    
    
    switchToRegister.addEventListener('click', (e) => {
        e.preventDefault();
        hideModal(loginModal);
        showModal(registerModal);
    });
    
    switchToLogin.addEventListener('click', (e) => {
        e.preventDefault();
        hideModal(registerModal);
        showModal(loginModal);
    });
    
    // Close modals when clicking X
    closeButtons.forEach(btn => {
        btn.addEventListener('click', function() {
            const modal = this.closest('.modal');
            hideModal(modal);
        });
    });
    
    // Close modals when clicking outside
    window.addEventListener('click', (e) => {
        if (e.target.classList.contains('modal')) {
            hideModal(e.target);
        }
    });
    
    // Form submissions
    loginForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const email = document.getElementById('loginEmail').value;
        const password = document.getElementById('loginPassword').value;
        
        // In a real app, you would validate and send to server
        console.log('Login attempt with:', email, password);
        alert('Login functionality will be implemented with backend');
        hideModal(loginModal);
    });
    
    registerForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const name = document.getElementById('registerName').value;
        const email = document.getElementById('registerEmail').value;
        const password = document.getElementById('registerPassword').value;
        const phone = document.getElementById('registerPhone').value;
        
        // In a real app, you would validate and send to server
        console.log('Registration with:', name, email, password, phone);
        alert('Account created successfully!');
        hideModal(registerModal);
    });
    
    pickupForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const type = document.getElementById('ewasteType').value;
        const condition = document.getElementById('ewasteCondition').value;
        const quantity = parseInt(document.getElementById('ewasteQuantity').value);
        const date = document.getElementById('pickupDate').value;
        const time = document.getElementById('pickupTime').value;
        const address = document.getElementById('pickupAddress').value;
        
        const points = calculatePoints(type, condition, quantity);
        
        // In a real app, you would send this data to the server
        console.log('Pickup scheduled:', { type, condition, quantity, date, time, address, points });
        
        alert(`Pickup scheduled successfully!\nYou will earn ${points} EcoPoints for this contribution.`);
        hideModal(pickupModal);
        
        // Reset form
        pickupForm.reset();
    });
    
    redeemForm.addEventListener('submit', (e) => {
        e.preventDefault();
        const address = document.getElementById('shippingAddress').value;
        
        // In a real app, you would send this data to the server
        console.log('Reward redemption with shipping address:', address);
        alert('Reward redemption successful! Your item will be shipped soon.');
        hideModal(rewardModal);
        
        // Reset form
        redeemForm.reset();
    });
    
     Set minimum pickup date to tomorrow
    const today = new Date();
    const tomorrow = new Date(today);
    tomorrow.setDate(tomorrow.getDate() + 1);
    
    const pickupDateInput = document.getElementById('pickupDate');
    pickupDateInput.min = tomorrow.toISOString().split('T')[0];
    
     Initialize the page
    displayRewards();
});
</script>
</body>
</html>
