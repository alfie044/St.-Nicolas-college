<!DOCTYPE html><html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>St. Nicolas College | Portal</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/qrcodejs@1.0.0/qrcode.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@700&display=swap');:root {
        --primary: #0A3D91;
        --secondary: #1E5CCB;
    }
    
    .glass {
        background: rgba(255, 255, 255, 0.85);
        backdrop-filter: blur(16px);
    }
    
    .dark .glass {
        background: rgba(15, 23, 42, 0.85);
    }
    
    .hero-bg {
        background: linear-gradient(rgba(10, 61, 145, 0.75), rgba(30, 92, 203, 0.85)), url('https://picsum.photos/id/1015/2000/1200');
        background-size: cover;
        background-position: center;
    }
    
    .nav-link {
        transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    .nav-link:hover {
        transform: translateY(-2px);
        color: #F4B400;
    }
    
    .card-hover {
        transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    
    .card-hover:hover {
        transform: translateY(-12px) scale(1.03);
        box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.25);
    }
    
    .ripple {
        position: relative;
        overflow: hidden;
    }
    
    .ripple:after {
        content: '';
        position: absolute;
        top: 50%;
        left: 50%;
        width: 0;
        height: 0;
        background: rgba(244, 180, 0, 0.3);
        border-radius: 50%;
        transform: translate(-50%, -50%);
        animation: ripple 0.8s linear;
        opacity: 0;
    }
    
    @keyframes ripple {
        to {
            width: 300px;
            height: 300px;
            opacity: 0;
        }
    }
    
    .floating-particle {
        position: absolute;
        border-radius: 50%;
        animation: floatParticle 25s linear infinite;
        opacity: 0.15;
    }
    
    @keyframes floatParticle {
        0% { transform: translateY(100vh) rotate(0deg); }
        100% { transform: translateY(-100vh) rotate(720deg); }
    }
    
    .section {
        display: none;
    }
    
    .section.active {
        display: block;
    }
    
    .toast {
        animation: toastIn 0.3s ease, toastOut 0.3s 2.7s ease forwards;
    }
</style>

</head>
<body class="bg-[#F8FAFC] text-[#1E293B] font-sans">
    <!-- LOADING SCREEN -->
    <div id="loading-screen" class="fixed inset-0 bg-[#0A3D91] flex items-center justify-center z-[9999]">
        <div class="text-center">
            <div class="w-24 h-24 mx-auto border-8 border-white/30 border-t-[#F4B400] rounded-full animate-spin"></div>
            <h1 class="text-white text-3xl font-bold mt-8 tracking-widest">ST. NICOLAS</h1>
            <p class="text-white/70 mt-2">College of Business &amp; Technology</p>
            <div class="mt-12 text-white/50 text-sm">Loading Portal...</div>
        </div>
    </div><!-- NAVBAR -->
<nav id="main-nav" class="bg-white border-b border-gray-200 sticky top-0 z-50 shadow-sm">
    <div class="max-w-screen-2xl mx-auto">
        <div class="px-8 py-5 flex items-center justify-between">
            <!-- LOGO -->
            <div class="flex items-center gap-x-3">
                <div class="w-10 h-10 bg-[#0A3D91] rounded-2xl flex items-center justify-center text-white font-bold text-2xl shadow-inner">S</div>
                <div>
                    <h1 class="font-bold text-2xl tracking-tighter text-[#0A3D91]">St. Nicolas</h1>
                    <p class="text-xs text-gray-500 -mt-1">College of Business &amp; Technology</p>
                </div>
            </div>
            
            <!-- DESKTOP MENU -->
            <div class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                <a onclick="navigateTo('home')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-home">Home</a>
                <a onclick="navigateTo('about')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-about">About</a>
                <a onclick="navigateTo('programs')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-programs">Programs</a>
                <a onclick="navigateTo('announcements')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-announcements">Announcements</a>
                <a onclick="navigateTo('admissions')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-admissions">Admissions</a>
                <a onclick="navigateTo('contact')" class="nav-link cursor-pointer text-[#1E293B] hover:text-[#F4B400]" id="nav-contact">Contact</a>
            </div>
            
            <div class="flex items-center gap-x-4">
                <button onclick="toggleDarkMode()" class="w-9 h-9 flex items-center justify-center rounded-2xl hover:bg-gray-100 transition-colors">
                    <i id="theme-icon" class="fas fa-moon text-[#1E293B]"></i>
                </button>
                
                <button onclick="showLoginModal()" id="login-btn"
                        class="px-6 py-2.5 bg-[#0A3D91] text-white rounded-3xl font-semibold text-sm ripple">
                    Login
                </button>
                
                <button onclick="showDashboard()" id="dashboard-btn" class="hidden px-6 py-2.5 bg-[#F4B400] text-[#0A3D91] rounded-3xl font-semibold text-sm items-center gap-x-2">
                    <i class="fas fa-tachometer-alt"></i>
                    <span>Dashboard</span>
                </button>
                
                <!-- Mobile Menu -->
                <button onclick="toggleMobileMenu()" class="md:hidden w-10 h-10 flex items-center justify-center text-2xl">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </div>
    
    <!-- MOBILE MENU -->
    <div id="mobile-menu" class="hidden md:hidden bg-white border-t py-4">
        <div class="px-6 flex flex-col gap-y-4 text-lg">
            <a onclick="navigateTo('home');toggleMobileMenu()" class="py-2">Home</a>
            <a onclick="navigateTo('about');toggleMobileMenu()" class="py-2">About</a>
            <a onclick="navigateTo('programs');toggleMobileMenu()" class="py-2">Programs</a>
            <a onclick="navigateTo('announcements');toggleMobileMenu()" class="py-2">Announcements</a>
            <a onclick="navigateTo('admissions');toggleMobileMenu()" class="py-2">Admissions</a>
            <a onclick="navigateTo('contact');toggleMobileMenu()" class="py-2">Contact</a>
            <div class="pt-4 border-t">
                <button onclick="showLoginModal();toggleMobileMenu()" class="w-full py-4 bg-[#0A3D91] text-white rounded-3xl">Login to Portal</button>
            </div>
        </div>
    </div>
</nav>

<!-- MAIN CONTENT -->
<div class="max-w-screen-2xl mx-auto">
    
    <!-- HOME SECTION -->
    <section id="home" class="section active">
        <div class="hero-bg h-screen flex items-center relative overflow-hidden">
            <!-- Floating Particles -->
            <div id="particles" class="absolute inset-0 pointer-events-none"></div>
            
            <div class="max-w-4xl mx-auto px-6 text-center text-white relative z-10">
                <h1 class="text-6xl md:text-7xl font-bold leading-none tracking-tighter mb-6">
                    Empowering Future<br>Leaders Through<br>Quality Education
                </h1>
                <p class="text-xl md:text-2xl text-white/90 max-w-lg mx-auto mb-10">
                    St. Nicolas College of Business and Technology - Where Excellence Meets Innovation
                </p>
                
                <div class="flex flex-wrap justify-center gap-4">
                    <button onclick="navigateTo('admissions')" 
                            class="px-10 py-5 bg-white text-[#0A3D91] rounded-3xl font-semibold text-lg shadow-xl hover:shadow-2xl transition-all active:scale-95">
                        Apply Now
                    </button>
                    <button onclick="navigateTo('programs')" 
                            class="px-10 py-5 border-2 border-white text-white rounded-3xl font-semibold text-lg hover:bg-white/10 transition-all">
                        View Programs
                    </button>
                </div>
                
                <!-- Stats -->
                <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mt-24">
                    <div class="text-center">
                        <div id="stat-students" class="text-5xl font-bold">2840</div>
                        <div class="text-white/70 text-sm tracking-widest">STUDENTS</div>
                    </div>
                    <div class="text-center">
                        <div id="stat-faculty" class="text-5xl font-bold">142</div>
                        <div class="text-white/70 text-sm tracking-widest">FACULTY</div>
                    </div>
                    <div class="text-center">
                        <div id="stat-programs" class="text-5xl font-bold">12</div>
                        <div class="text-white/70 text-sm tracking-widest">PROGRAMS</div>
                    </div>
                    <div class="text-center">
                        <div id="stat-graduates" class="text-5xl font-bold">8740</div>
                        <div class="text-white/70 text-sm tracking-widest">GRADUATES</div>
                    </div>
                </div>
            </div>
            
            <div class="absolute bottom-10 left-1/2 flex flex-col items-center">
                <div class="text-white/60 text-xs tracking-widest mb-2">SCROLL TO EXPLORE</div>
                <i class="fas fa-chevron-down animate-bounce text-3xl"></i>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="section py-24 bg-white">
        <div class="max-w-screen-xl mx-auto px-6">
            <div class="text-center mb-16">
                <span class="px-4 py-2 bg-[#F4B400]/10 text-[#F4B400] rounded-full text-sm font-medium">OUR STORY</span>
                <h2 class="text-5xl font-bold mt-4">About St. Nicolas College</h2>
            </div>
            
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div>
                    <img src="https://picsum.photos/id/1015/800/600" class="rounded-3xl shadow-2xl" alt="Campus">
                </div>
                <div class="space-y-10">
                    <div>
                        <h3 class="text-2xl font-semibold mb-3 flex items-center gap-3">
                            <span class="text-[#F4B400]">Mission</span>
                        </h3>
                        <p class="text-gray-600">To develop competent, ethical, and innovative leaders who will contribute to nation-building through quality business and technology education.</p>
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-3 flex items-center gap-3">
                            <span class="text-[#F4B400]">Vision</span>
                        </h3>
                        <p class="text-gray-600">To be the leading institution in business and technology education in the region, recognized globally for excellence and innovation.</p>
                    </div>
                    <div class="grid grid-cols-2 gap-6">
                        <div class="glass p-6 rounded-3xl border">
                            <h4 class="font-semibold mb-2">Core Values</h4>
                            <ul class="space-y-2 text-sm">
                                <li class="flex items-center gap-2"><i class="fas fa-check text-[#F4B400]"></i> Excellence</li>
                                <li class="flex items-center gap-2"><i class="fas fa-check text-[#F4B400]"></i> Integrity</li>
                                <li class="flex items-center gap-2"><i class="fas fa-check text-[#F4B400]"></i> Innovation</li>
                                <li class="flex items-center gap-2"><i class="fas fa-check text-[#F4B400]"></i> Service</li>
                            </ul>
                        </div>
                        <div class="glass p-6 rounded-3xl border">
                            <h4 class="font-semibold mb-4">Goals</h4>
                            <div class="space-y-4">
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full w-[92%] bg-[#0A3D91]"></div>
                                </div>
                                <div class="text-xs text-gray-500">Academic Excellence</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PROGRAMS SECTION -->
    <section id="programs" class="section py-24 bg-[#F8FAFC]">
        <div class="max-w-screen-xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-5xl font-bold">Academic Programs</h2>
                <p class="text-gray-500 mt-3">Choose your path to success</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8" id="programs-grid">
                <!-- Populated by JS -->
            </div>
        </div>
    </section>

    <!-- ANNOUNCEMENTS SECTION -->
    <section id="announcements" class="section py-24 bg-white">
        <div class="max-w-screen-xl mx-auto px-6">
            <h2 class="text-4xl font-bold mb-10">Announcements &amp; Events</h2>
            <div id="announcements-list" class="space-y-6">
                <!-- JS populated -->
            </div>
        </div>
    </section>

    <!-- ADMISSIONS SECTION -->
    <section id="admissions" class="section py-24 bg-[#F8FAFC]">
        <div class="max-w-2xl mx-auto px-6">
            <div class="glass rounded-3xl p-10">
                <h2 class="text-4xl font-bold text-center mb-8">Online Application</h2>
                <form id="application-form" onsubmit="submitApplication(event)" class="space-y-6">
                    <input type="text" placeholder="Full Name" class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                    <input type="date" class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                    <input type="text" placeholder="Address" class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                    <input type="tel" placeholder="Contact Number" class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                    <input type="email" placeholder="Email" class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                    <select class="w-full px-6 py-5 border rounded-3xl focus:outline-none" required>
                        <option value="">Select Program</option>
                        <option>BS Business Administration</option>
                        <option>BS Information Technology</option>
                        <option>BS Computer Science</option>
                        <option>BS Entrepreneurship</option>
                    </select>
                    <button type="submit" class="w-full py-6 bg-[#0A3D91] text-white rounded-3xl font-semibold">Submit Application</button>
                </form>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="section py-24 bg-white">
        <div class="max-w-screen-xl mx-auto px-6 grid md:grid-cols-2 gap-16">
            <div>
                <h2 class="text-4xl font-bold mb-8">Get In Touch</h2>
                <form id="contact-form" onsubmit="submitContact(event)" class="space-y-6">
                    <input type="text" placeholder="Your Name" class="w-full px-6 py-5 border rounded-3xl" required>
                    <input type="email" placeholder="Email" class="w-full px-6 py-5 border rounded-3xl" required>
                    <textarea placeholder="Message" rows="5" class="w-full px-6 py-5 border rounded-3xl" required></textarea>
                    <button type="submit" class="w-full py-6 bg-[#0A3D91] text-white rounded-3xl font-semibold">Send Message</button>
                </form>
            </div>
            <div class="space-y-8 pt-12">
                <div class="flex items-start gap-4">
                    <i class="fas fa-map-marker-alt text-2xl text-[#F4B400] mt-1"></i>
                    <div>
                        <div class="font-semibold">Address</div>
                        <div class="text-gray-600">123 Education Avenue, Manila, Philippines</div>
                    </div>
                </div>
                <div class="flex items-start gap-4">
                    <i class="fas fa-phone text-2xl text-[#F4B400] mt-1"></i>
                    <div>
                        <div class="font-semibold">Phone</div>
                        <div class="text-gray-600">(02) 8123-4567</div>
                    </div>
                </div>
                <div class="flex items-start gap-4">
                    <i class="fas fa-envelope text-2xl text-[#F4B400] mt-1"></i>
                    <div>
                        <div class="font-semibold">Email</div>
                        <div class="text-gray-600">info@sncbt.edu.ph</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- DASHBOARD SECTION -->
    <section id="dashboard-section" class="section hidden bg-gray-50 min-h-screen">
        <div class="flex h-screen">
            <!-- SIDEBAR -->
            <div class="w-72 bg-white border-r flex flex-col">
                <div class="p-6 border-b">
                    <div class="flex items-center gap-x-3">
                        <div onclick="showProfileModal()" class="w-11 h-11 bg-[#0A3D91] text-white rounded-2xl flex items-center justify-center cursor-pointer font-bold">SN</div>
                        <div>
                            <div id="user-name" class="font-semibold">Welcome back</div>
                            <div id="user-role" class="text-xs text-green-600">Student</div>
                        </div>
                    </div>
                </div>
                
                <div class="flex-1 overflow-auto py-6 px-3" id="sidebar-menu">
                    <!-- Populated by JS -->
                </div>
                
                <div class="p-6 border-t">
                    <button onclick="logout()" 
                            class="w-full flex items-center justify-center gap-x-3 py-4 text-red-600 hover:bg-red-50 rounded-3xl">
                        <i class="fas fa-sign-out-alt"></i>
                        <span class="font-medium">Sign Out</span>
                    </button>
                    <button onclick="backupData()" class="mt-3 w-full text-xs py-3 border rounded-3xl">Backup Data</button>
                    <button onclick="restoreData()" class="mt-2 w-full text-xs py-3 border rounded-3xl">Restore Data</button>
                </div>
            </div>
            
            <!-- MAIN DASHBOARD CONTENT -->
            <div class="flex-1 overflow-auto">
                <div class="bg-white border-b px-10 py-6 flex items-center justify-between sticky top-0 z-30">
                    <div class="flex items-center gap-x-6">
                        <h1 id="dashboard-title" class="text-3xl font-bold">Dashboard</h1>
                    </div>
                    
                    <div class="flex items-center gap-x-8">
                        <div onclick="showNotifications()" class="relative cursor-pointer">
                            <i class="fas fa-bell text-xl"></i>
                            <div id="notif-count" class="absolute -top-1 -right-1 bg-red-500 text-white text-[10px] w-4 h-4 rounded-full flex items-center justify-center">3</div>
                        </div>
                        <div class="flex items-center gap-x-2 cursor-pointer" onclick="showProfileModal()">
                            <div class="text-right">
                                <div id="dash-name" class="font-medium text-sm">Juan Dela Cruz</div>
                                <div class="text-xs text-gray-500">BSIT • 3rd Year</div>
                            </div>
                            <div class="w-9 h-9 bg-amber-200 rounded-2xl"></div>
                        </div>
                    </div>
                </div>
                
                <div class="p-10" id="main-content">
                    <!-- Default Dashboard View populated by JS -->
                </div>
            </div>
        </div>
    </section>

    <!-- QR SCANNER MODAL -->
    <div id="qr-scanner-modal" class="hidden fixed inset-0 bg-black/70 flex items-center justify-center z-[999]">
        <div class="bg-white rounded-3xl max-w-md w-full mx-4 overflow-hidden">
            <div class="p-6 border-b flex justify-between">
                <h3 class="font-semibold text-xl">QR Scanner</h3>
                <button onclick="closeQRScanner()" class="text-3xl leading-none">×</button>
            </div>
            <div class="p-8">
                <div id="qr-video-container" class="bg-black rounded-2xl aspect-video flex items-center justify-center text-white cursor-pointer" onclick="simulateQRScan()">
                    <p class="text-center">Click to simulate scan</p>
                </div>
                <div class="mt-8">
                    <input id="manual-qr-input" type="text" placeholder="Or enter Student Number" 
                           class="w-full px-6 py-5 border rounded-3xl focus:outline-none focus:border-[#F4B400]">
                </div>
            </div>
            <div class="p-6 border-t flex gap-4">
                <button onclick="simulateQRScan()" 
                        class="flex-1 py-6 bg-[#0A3D91] text-white rounded-3xl font-medium">Scan</button>
                <button onclick="closeQRScanner()" 
                        class="flex-1 py-6 border rounded-3xl font-medium">Cancel</button>
            </div>
        </div>
    </div>

    <!-- LOGIN MODAL -->
    <div id="login-modal" class="hidden fixed inset-0 bg-black/60 flex items-center justify-center z-[999]">
        <div class="glass rounded-3xl w-full max-w-md p-10 shadow-2xl">
            <h2 class="text-3xl font-bold text-center mb-8">Portal Login</h2>
            
            <div class="space-y-6">
                <div>
                    <label class="text-sm block mb-2 font-medium">Email / Student Number</label>
                    <input id="login-email" type="text" value="juan.delacruz@sncbt.edu.ph" 
                           class="w-full px-5 py-6 border rounded-3xl focus:outline-none">
                </div>
                <div>
                    <label class="text-sm block mb-2 font-medium">Password</label>
                    <input id="login-pass" type="password" value="password123" 
                           class="w-full px-5 py-6 border rounded-3xl focus:outline-none">
                </div>
                
                <div class="flex gap-3">
                    <button onclick="performLogin()" 
                            class="flex-1 py-6 bg-[#0A3D91] text-white rounded-3xl font-semibold">Login</button>
                    <button onclick="hideLoginModal()" 
                            class="flex-1 py-6 border rounded-3xl font-semibold">Cancel</button>
                </div>
                
                <div onclick="demoAdminLogin()" class="text-center text-xs text-[#F4B400] cursor-pointer hover:underline">
                    Demo as Admin
                </div>
            </div>
        </div>
    </div>

    <!-- TOAST -->
    <div id="toast" class="hidden fixed bottom-6 right-6 bg-[#1E293B] text-white px-6 py-4 rounded-3xl shadow-2xl flex items-center gap-3 toast">
        <i class="fas fa-check-circle text-[#F4B400]"></i>
        <span id="toast-text"></span>
    </div>
</div>

<footer class="bg-[#0A3D91] text-white py-12 text-center text-sm">
    <p>&copy; 2026 St. Nicolas College of Business and Technology. All Rights Reserved.</p>
</footer>

<script>
    let currentUser = null;
    let isAdmin = false;
    let students = [];
    let announcements = [];
    let payments = [];
    
    function initMockData() {
        students = [
            {id: "20230001", name: "Juan Dela Cruz", course: "BS Information Technology", year: "3", email: "juan.delacruz@sncbt.edu.ph", balance: 4250},
            {id: "20230045", name: "Maria Santos", course: "BS Business Administration", year: "2", email: "maria.santos@sncbt.edu.ph", balance: 8750}
        ];
        
        announcements = [
            {title: "Midterm Examination Schedule", date: "June 10, 2026", content: "All students are reminded to check their respective schedules."},
            {title: "Enrollment for SY 2026-2027 is Now Open", date: "May 28, 2026", content: "Please complete your enrollment on or before July 15."}
        ];
        
        payments = [
            {date: "Jun 01", amount: 5200, event: "Tuition Fee"},
            {date: "May 15", amount: 3000, event: "Lab Fee"}
        ];
    }
    
    function createParticles() {
        const container = document.getElementById('particles');
        container.innerHTML = '';
        for (let i = 0; i < 45; i++) {
            const particle = document.createElement('div');
            particle.className = 'floating-particle';
            particle.style.width = `${Math.random() * 6 + 3}px`;
            particle.style.height = particle.style.width;
            particle.style.left = `${Math.random() * 100}%`;
            particle.style.background = `hsl(${Math.random() * 30 + 200}, 80%, 70%)`;
            particle.style.animationDuration = `${Math.random() * 35 + 25}s`;
            particle.style.animationDelay = `-${Math.random() * 30}s`;
            container.appendChild(particle);
        }
    }
    
    function animateCounters() {
        const counters = [
            {el: 'stat-students', target: 2840},
            {el: 'stat-faculty', target: 142},
            {el: 'stat-programs', target: 12},
            {el: 'stat-graduates', target: 8740}
        ];
        
        counters.forEach(counter => {
            const element = document.getElementById(counter.el);
            let count = 0;
            const increment = Math.ceil(counter.target / 60);
            const timer = setInterval(() => {
                count += increment;
                if (count >= counter.target) {
                    count = counter.target;
                    clearInterval(timer);
                }
                element.textContent = count.toLocaleString();
            }, 30);
        });
    }
    
    function populatePrograms() {
        const programs = [
            {icon: "fa-briefcase", title: "BS Business Administration", desc: "Master the art of business leadership"},
            {icon: "fa-laptop-code", title: "BS Information Technology", desc: "Shape the digital future"},
            {icon: "fa-computer", title: "BS Computer Science", desc: "Algorithms & Systems Design"},
            {icon: "fa-seedling", title: "BS Entrepreneurship", desc: "Build your own legacy"}
        ];
        
        const container = document.getElementById('programs-grid');
        container.innerHTML = '';
        programs.forEach(prog => {
            const card = document.createElement('div');
            card.className = 'glass rounded-3xl p-8 card-hover';
            card.innerHTML = `
                <i class="fas ${prog.icon} text-5xl text-[#F4B400] mb-6"></i>
                <h4 class="font-semibold text-xl">${prog.title}</h4>
                <p class="text-gray-600 mt-3">${prog.desc}</p>
                <button onclick="alert('Program details would open here (Demo)')" 
                        class="mt-8 w-full py-4 border border-[#0A3D91] text-[#0A3D91] rounded-3xl text-sm font-medium hover:bg-[#0A3D91] hover:text-white transition-all">
                    LEARN MORE
                </button>
            `;
            container.appendChild(card);
        });
    }
    
    function populateAnnouncements() {
        const container = document.getElementById('announcements-list');
        container.innerHTML = '';
        announcements.forEach(ann => {
            const div = document.createElement('div');
            div.className = 'glass p-8 rounded-3xl flex gap-8';
            div.innerHTML = `
                <div class="w-28 h-28 bg-[#F4B400]/10 rounded-2xl flex-shrink-0 flex items-center justify-center">
                    <i class="fas fa-bullhorn text-5xl text-[#F4B400]"></i>
                </div>
                <div class="flex-1">
                    <div class="text-[#F4B400] text-sm">${ann.date}</div>
                    <h3 class="text-2xl font-semibold mt-2">${ann.title}</h3>
                    <p class="mt-4 text-gray-600">${ann.content}</p>
                </div>
            `;
            container.appendChild(div);
        });
    }
    
    function populateRecentPayments() {
        const container = document.getElementById('recent-payments') || document.createElement('div');
        if (!container.id) return;
        container.innerHTML = '';
        payments.forEach(p => {
            const item = document.createElement('div');
            item.className = 'flex justify-between items-center';
            item.innerHTML = `
                <div>
                    <div class="font-medium">${p.event}</div>
                    <div class="text-xs text-gray-500">${p.date}</div>
                </div>
                <div class="text-right">
                    <div class="font-semibold text-green-600">+₱${p.amount}</div>
                </div>
            `;
            container.appendChild(item);
        });
    }
    
    function renderSidebarMenu() {
        const menuHTML = `
            <div onclick="switchDashboardView('dashboard')" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer active">
                <i class="fas fa-tachometer-alt w-5"></i>
                <span class="font-medium">Dashboard</span>
            </div>
            <div onclick="switchDashboardView('students')" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer">
                <i class="fas fa-users w-5"></i>
                <span class="font-medium">Students</span>
            </div>
            <div onclick="switchDashboardView('payments')" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer">
                <i class="fas fa-credit-card w-5"></i>
                <span class="font-medium">Payments</span>
            </div>
            <div onclick="switchDashboardView('events')" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer">
                <i class="fas fa-calendar-alt w-5"></i>
                <span class="font-medium">Events</span>
            </div>
            <div onclick="showQRScanner()" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer">
                <i class="fas fa-qrcode w-5"></i>
                <span class="font-medium">QR Scanner</span>
            </div>
            ${isAdmin ? `
            <div onclick="switchDashboardView('admin')" class="sidebar-item flex items-center gap-3 px-6 py-5 hover:bg-gray-100 rounded-3xl cursor-pointer">
                <i class="fas fa-cog w-5"></i>
                <span class="font-medium">Admin Panel</span>
            </div>` : ''}
        `;
        document.getElementById('sidebar-menu').innerHTML = menuHTML;
    }
    
    function showToast(message) {
        const toast = document.getElementById('toast');
        document.getElementById('toast-text').innerHTML = message;
        toast.classList.remove('hidden');
        setTimeout(() => {
            toast.classList.add('hidden');
        }, 3000);
    }
    
    function performLogin() {
        const email = document.getElementById('login-email').value;
        hideLoginModal();
        
        currentUser = {
            name: "Juan Dela Cruz",
            email: email,
            role: "Student",
            studentId: "20230001"
        };
        
        isAdmin = false;
        
        document.getElementById('login-btn').classList.add('hidden');
        document.getElementById('dashboard-btn').classList.remove('hidden');
        
        showToast("Login successful! Welcome back.");
        showDashboard();
    }
    
    function demoAdminLogin() {
        hideLoginModal();
        currentUser = {
            name: "Dr. Elena Rodriguez",
            email: "admin@sncbt.edu.ph",
            role: "Administrator"
        };
        isAdmin = true;
        
        document.getElementById('login-btn').classList.add('hidden');
        document.getElementById('dashboard-btn').classList.remove('hidden');
        
        showToast("Admin access granted");
        showDashboard();
    }
    
    function logout() {
        currentUser = null;
        isAdmin = false;
        document.getElementById('dashboard-section').classList.add('hidden');
        document.getElementById('login-btn').classList.remove('hidden');
        document.getElementById('dashboard-btn').classList.add('hidden');
        showToast("Logged out successfully");
    }
    
    function showDashboard() {
        document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
        document.getElementById('dashboard-section').classList.remove('hidden');
        document.getElementById('dashboard-section').classList.add('active');
        
        renderSidebarMenu();
        populateRecentPayments();
        
        // Initialize Chart
        setTimeout(() => {
            const ctx = document.getElementById('collectionChart');
            if (ctx) {
                new Chart(ctx, {
                    type: 'line',
                    data: {
                        labels: ['Jan','Feb','Mar','Apr','May','Jun'],
                        datasets: [{
                            label: 'Collection',
                            data: [12400, 18900, 22100, 16700, 25400, 31200],
                            borderColor: '#F4B400',
                            tension: 0.4,
                            borderWidth: 4
                        }]
                    },
                    options: { plugins: { legend: { display: false } } }
                });
            }
        }, 600);
    }
    
    function switchDashboardView(view) {
        document.getElementById('dashboard-title').textContent = view.charAt(0).toUpperCase() + view.slice(1);
        
        let content = '';
        if (view === 'dashboard') {
            content = `
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
                    <div class="glass rounded-3xl p-6 shadow">
                        <div class="flex justify-between">
                            <div>
                                <div class="text-sm text-gray-500">Total Due</div>
                                <div class="text-4xl font-bold mt-1">₱12,450</div>
                            </div>
                            <i class="fas fa-wallet text-4xl text-[#F4B400]"></i>
                        </div>
                    </div>
                    <div class="glass rounded-3xl p-6 shadow">
                        <div class="flex justify-between">
                            <div>
                                <div class="text-sm text-gray-500">Paid This Month</div>
                                <div class="text-4xl font-bold mt-1 text-green-600">₱8,200</div>
                            </div>
                            <i class="fas fa-check-circle text-4xl text-green-500"></i>
                        </div>
                    </div>
                    <div class="glass rounded-3xl p-6 shadow">
                        <div class="flex justify-between">
                            <div>
                                <div class="text-sm text-gray-500">Balance</div>
                                <div class="text-4xl font-bold mt-1 text-red-500">₱4,250</div>
                            </div>
                            <i class="fas fa-exclamation-triangle text-4xl text-red-400"></i>
                        </div>
                    </div>
                    <div class="glass rounded-3xl p-6 shadow">
                        <div class="flex justify-between">
                            <div>
                                <div class="text-sm text-gray-500">Events</div>
                                <div class="text-4xl font-bold mt-1">4</div>
                            </div>
                            <i class="fas fa-calendar text-4xl text-[#1E5CCB]"></i>
                        </div>
                    </div>
                </div>
                
                <div class="glass rounded-3xl p-8 mb-8">
                    <h3 class="font-semibold mb-6">Collection Overview (2026)</h3>
                    <canvas id="collectionChart" height="120"></canvas>
                </div>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                    <div class="glass rounded-3xl p-8">
                        <h3 class="font-semibold mb-6">Recent Payments</h3>
                        <div id="recent-payments" class="space-y-6"></div>
                    </div>
                    <div class="glass rounded-3xl p-8">
                        <h3 class="font-semibold mb-6">Upcoming Events</h3>
                        <div class="space-y-6">
                            <div class="flex gap-4">
                                <div class="text-amber-500">Jun 15</div>
                                <div>Annual Recognition Day</div>
                            </div>
                        </div>
                    </div>
                </div>
            `;
        } else if (view === 'students') {
            content = `<h2 class="text-3xl font-bold mb-8">Student Management</h2><div class="glass rounded-3xl p-8">`;
            students.forEach(student => {
                content += `
                    <div class="flex justify-between items-center py-6 border-b last:border-none">
                        <div>
                            <div class="font-semibold">${student.name}</div>
                            <div class="text-sm text-gray-500">${student.id} • ${student.course}</div>
                        </div>
                        <div class="text-right">
                            <div class="text-red-500 font-medium">₱${student.balance}</div>
                            <button onclick="generateStudentQR('${student.id}')" class="text-xs mt-2 px-5 py-2 bg-[#0A3D91] text-white rounded-3xl">QR Code</button>
                        </div>
                    </div>
                `;
            });
            content += `</div>`;
        } else {
            content = `
                <div class="glass rounded-3xl p-10 md:p-16 shadow-xl">
                    <div class="text-center mb-10">
                        <div class="w-20 h-20 mx-auto rounded-full bg-[#F4B400]/10 flex items-center justify-center mb-6">
                            <i class="fas fa-tools text-3xl text-[#F4B400]"></i>
                        </div>
                        <h2 class="text-3xl font-bold mb-4">This module is under development</h2>
                        <p class="text-gray-500 max-w-2xl mx-auto">
                            We are still building the needed systems for this portal. More features will be added soon.
                        </p>
                    </div>

                    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-5">
                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-user-graduate text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Student Information System</h4>
                            <p class="text-sm text-gray-500">Store and manage student profiles, records, and status.</p>
                        </div>

                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-clipboard-list text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Enrollment System</h4>
                            <p class="text-sm text-gray-500">Handle online enrollment and application processing.</p>
                        </div>

                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-credit-card text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Payment System</h4>
                            <p class="text-sm text-gray-500">Track tuition fees, balances, and payment history.</p>
                        </div>

                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-bullhorn text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Announcements System</h4>
                            <p class="text-sm text-gray-500">Post school announcements, events, and reminders.</p>
                        </div>

                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-chart-line text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Reports System</h4>
                            <p class="text-sm text-gray-500">Generate reports for students, payments, and records.</p>
                        </div>

                        <div class="p-6 rounded-2xl bg-white border shadow-sm">
                            <i class="fas fa-cogs text-2xl text-[#0A3D91] mb-3"></i>
                            <h4 class="font-semibold mb-2">Admin Settings</h4>
                            <p class="text-sm text-gray-500">Control portal access, users, and system settings.</p>
                        </div>
                    </div>
                </div>
            `;
        }
        
        document.getElementById('main-content').innerHTML = content;
        populateRecentPayments();
    }
    
    function generateStudentQR(studentId) {
        const modal = document.createElement('div');
        modal.className = "fixed inset-0 bg-black/70 flex items-center justify-center z-[9999]";
        modal.innerHTML = `
            <div class="bg-white rounded-3xl p-10 max-w-xs w-full text-center">
                <div id="qrcode-container" class="mx-auto"></div>
                <p class="font-mono text-sm mt-8">${studentId}</p>
                <button onclick="this.closest('.fixed').remove()" 
                        class="mt-10 px-10 py-4 bg-[#0A3D91] text-white rounded-3xl">Close</button>
            </div>
        `;
        document.body.appendChild(modal);
        
        setTimeout(() => {
            new QRCode(document.getElementById("qrcode-container"), {
                text: studentId,
                width: 220,
                height: 220,
                colorDark : "#0A3D91",
                colorLight : "#ffffff"
            });
        }, 100);
    }
    
    function showQRScanner() {
        document.getElementById('qr-scanner-modal').classList.remove('hidden');
    }
    
    function closeQRScanner() {
        document.getElementById('qr-scanner-modal').classList.add('hidden');
    }
    
    function simulateQRScan() {
        const input = document.getElementById('manual-qr-input').value || "20230001";
        closeQRScanner();
        
        const student = students.find(s => s.id === input);
        
        if (student) {
            showToast(`Student found: ${student.name} | Balance: ₱${student.balance}`);
        } else {
            showToast("Student not found.");
        }
    }
    
    function showLoginModal() {
        document.getElementById('login-modal').classList.remove('hidden');
    }
    
    function hideLoginModal() {
        document.getElementById('login-modal').classList.add('hidden');
    }
    
    function showNotifications() {
        showToast("3 new notifications");
    }
    
    function showProfileModal() {
        showToast("Profile settings would open here");
    }
    
    function toggleDarkMode() {
        document.documentElement.classList.toggle('dark');
        const icon = document.getElementById('theme-icon');
        if (document.documentElement.classList.contains('dark')) {
            icon.classList.remove('fa-moon');
            icon.classList.add('fa-sun');
        } else {
            icon.classList.add('fa-moon');
            icon.classList.remove('fa-sun');
        }
    }
    
    function toggleMobileMenu() {
        const menu = document.getElementById('mobile-menu');
        menu.classList.toggle('hidden');
    }
    
    function navigateTo(section) {
        document.querySelectorAll('.section').forEach(sec => {
            sec.classList.remove('active');
            if (sec.id === section) sec.classList.add('active');
        });
        
        document.querySelectorAll('.nav-link').forEach(link => {
            link.classList.remove('text-[#F4B400]');
            if (link.id === `nav-${section}`) link.classList.add('text-[#F4B400]');
        });
    }
    
    function submitApplication(e) {
        e.preventDefault();
        showToast("Application submitted successfully! (Demo)");
    }
    
    function submitContact(e) {
        e.preventDefault();
        showToast("Message sent! Thank you. (Demo)");
    }
    
    function backupData() {
        const data = {students, announcements, payments};
        const blob = new Blob([JSON.stringify(data, null, 2)], {type: 'application/json'});
        const url = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = 'sncbt_backup.json';
        a.click();
        showToast("Backup downloaded");
    }
    
    function restoreData() {
        const input = document.createElement('input');
        input.type = 'file';
        input.accept = '.json';
        input.onchange = e => {
            const file = e.target.files[0];
            const reader = new FileReader();
            reader.onload = ev => {
                try {
                    const data = JSON.parse(ev.target.result);
                    students = data.students || students;
                    announcements = data.announcements || announcements;
                    payments = data.payments || payments;
                    showToast("Data restored successfully");
                } catch(err) {
                    showToast("Invalid backup file");
                }
            };
            reader.readAsText(file);
        };
        input.click();
    }
    
    function handleKeyboard(e) {
        if (e.metaKey && e.key === "k") {
            e.preventDefault();
            showToast("Command palette would appear here");
        }
    }
    
    function initializeApp() {
        setTimeout(() => {
            document.getElementById('loading-screen').style.opacity = '0';
            setTimeout(() => {
                document.getElementById('loading-screen').style.display = 'none';
            }, 800);
        }, 1200);
        
        initMockData();
        createParticles();
        populatePrograms();
        populateAnnouncements();
        animateCounters();
        
        document.getElementById('dashboard-btn').addEventListener('click', showDashboard);
        document.addEventListener('keydown', handleKeyboard);
        
        navigateTo('home');
        showToast("Welcome to St. Nicolas College Portal");
    }
    
    window.onload = initializeApp;
</script>

</body>
</html>
