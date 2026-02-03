<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MindCare - Professional Psychology Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .section { display: none; }
        .section.active { display: block; }
        .section.active.flex { display: flex; }
        .section.active.grid { display: grid; }
        
        /* Custom scrollbar for a cleaner look */
        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #c7d2fe; border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: #818cf8; }
    </style>
</head>
<body class="bg-gray-50 font-sans text-gray-900">
    <div class="flex h-screen overflow-hidden">
        <!-- Sidebar Navigation -->
        <aside class="w-64 bg-indigo-700 text-white flex-shrink-0 flex flex-col shadow-xl">
            <div class="p-6">
                <div class="flex items-center space-x-3">
                    <div class="w-10 h-10 bg-white rounded-lg flex items-center justify-center text-indigo-700">
                        <i class="fas fa-brain text-xl"></i>
                    </div>
                    <h1 class="text-2xl font-bold tracking-tight">MindCare</h1>
                </div>
            </div>
            
            <nav class="flex-1 px-4 py-4 space-y-2 overflow-y-auto">
                <a href="#" data-section="home" class="nav-link flex items-center p-3 rounded-xl bg-indigo-800 text-white transition-all">
                    <i class="fas fa-home w-6"></i>
                    <span class="font-medium">Dashboard</span>
                </a>
                <a href="#" data-section="facetime" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-video w-6"></i>
                    <span class="font-medium">Online Facetime</span>
                </a>
                <a href="#" data-section="chatbot" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-robot w-6"></i>
                    <span class="font-medium">AI Chatbot</span>
                </a>
                <a href="#" data-section="scheduling" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-calendar-alt w-6"></i>
                    <span class="font-medium">Scheduling</span>
                </a>
                <a href="#" data-section="contacts" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-users w-6"></i>
                    <span class="font-medium">Contact List</span>
                </a>
                <a href="#" data-section="group" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-user-friends w-6"></i>
                    <span class="font-medium">Group Sessions</span>
                </a>
                <a href="#" data-section="universities" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-university w-6"></i>
                    <span class="font-medium">Universities</span>
                </a>
                <a href="#" data-section="community" class="nav-link flex items-center p-3 rounded-xl hover:bg-indigo-600 transition-all">
                    <i class="fas fa-comments w-6"></i>
                    <span class="font-medium">Community</span>
                </a>
            </nav>

            <div class="p-4 border-t border-indigo-600 bg-indigo-800/50">
                <div class="flex items-center space-x-3">
                    <img src="https://i.pravatar.cc/150?u=john" alt="Profile" class="w-10 h-10 rounded-full border-2 border-indigo-400">
                    <div>
                        <p class="text-sm font-bold">John Doe</p>
                        <p class="text-xs text-indigo-200">Premium Member</p>
                    </div>
                </div>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 flex flex-col overflow-hidden">
            <!-- Header -->
            <header class="h-16 border-b border-gray-200 flex items-center justify-between px-8 bg-white shadow-sm z-10">
                <h2 id="section-title" class="text-xl font-bold text-gray-800">Dashboard</h2>
                <div class="flex items-center space-x-5">
                    <div class="relative">
                        <i class="fas fa-bell text-gray-400 hover:text-indigo-600 cursor-pointer"></i>
                        <span class="absolute -top-1 -right-1 w-2 h-2 bg-red-500 rounded-full"></span>
                    </div>
                    <button class="bg-indigo-50 text-indigo-700 px-4 py-2 rounded-lg text-sm font-bold hover:bg-indigo-100 transition-colors">
                        <i class="fas fa-plus mr-2"></i>New Session
                    </button>
                </div>
            </header>

            <!-- Scrollable Content -->
            <div id="content" class="flex-1 overflow-y-auto p-8">
                
                <!-- Dashboard Section -->
                <section id="home-section" class="section active">
                    <div class="flex items-center justify-between mb-8">
                        <div>
                            <h3 class="text-3xl font-extrabold text-gray-900">Hello, John! 👋</h3>
                            <p class="text-gray-500 mt-1">"The best way to predict your future is to create it."</p>
                        </div>
                        <div class="bg-white p-4 rounded-2xl shadow-sm border border-gray-100 text-right">
                            <p class="text-xs font-bold text-gray-400 uppercase tracking-widest">Wellness Score</p>
                            <p class="text-2xl font-black text-green-500">82%</p>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-10">
                        <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-indigo-100 rounded-xl flex items-center justify-center text-indigo-600 mb-4">
                                <i class="fas fa-video text-xl"></i>
                            </div>
                            <h4 class="text-lg font-bold text-gray-800">Next Video Call</h4>
                            <p class="text-sm text-gray-500 mt-1">Dr. Sarah Smith</p>
                            <div class="mt-4 flex items-center justify-between">
                                <span class="text-indigo-600 font-bold">Tomorrow, 10:00 AM</span>
                                <i class="fas fa-arrow-right text-gray-300"></i>
                            </div>
                        </div>

                        <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center text-purple-600 mb-4">
                                <i class="fas fa-robot text-xl"></i>
                            </div>
                            <h4 class="text-lg font-bold text-gray-800">AI Check-in</h4>
                            <p class="text-sm text-gray-500 mt-1">Last seen 2 hours ago</p>
                            <div class="mt-4">
                                <button class="text-purple-600 font-bold hover:underline">Continue Chat</button>
                            </div>
                        </div>

                        <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow">
                            <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center text-orange-600 mb-4">
                                <i class="fas fa-users text-xl"></i>
                            </div>
                            <h4 class="text-lg font-bold text-gray-800">Group Session</h4>
                            <p class="text-sm text-gray-500 mt-1">Stress Management</p>
                            <div class="mt-4 flex items-center justify-between">
                                <span class="text-orange-600 font-bold">Friday, 4:00 PM</span>
                                <i class="fas fa-arrow-right text-gray-300"></i>
                            </div>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100">
                            <h4 class="text-xl font-bold text-gray-800 mb-6">Recommended Specialists</h4>
                            <div class="space-y-6">
                                <div class="flex items-center">
                                    <img src="https://i.pravatar.cc/150?u=david" class="w-14 h-14 rounded-full mr-4">
                                    <div class="flex-1">
                                        <p class="font-bold">Dr. David Wilson</p>
                                        <p class="text-xs text-indigo-600">Addiction Specialist</p>
                                    </div>
                                    <button class="bg-gray-50 text-gray-700 px-4 py-2 rounded-lg text-xs font-bold hover:bg-indigo-600 hover:text-white transition-all">Book</button>
                                </div>
                                <div class="flex items-center">
                                    <img src="https://i.pravatar.cc/150?u=lisa" class="w-14 h-14 rounded-full mr-4">
                                    <div class="flex-1">
                                        <p class="font-bold">Dr. Lisa Thompson</p>
                                        <p class="text-xs text-indigo-600">Child & Adolescent</p>
                                    </div>
                                    <button class="bg-gray-50 text-gray-700 px-4 py-2 rounded-lg text-xs font-bold hover:bg-indigo-600 hover:text-white transition-all">Book</button>
                                </div>
                            </div>
                        </div>
                        <div class="bg-indigo-900 rounded-2xl p-8 text-white relative overflow-hidden">
                            <i class="fas fa-quote-left absolute top-4 right-4 text-white/10 text-8xl"></i>
                            <h4 class="text-2xl font-bold mb-4 relative z-10">Emergency Support</h4>
                            <p class="text-indigo-200 mb-6 relative z-10 leading-relaxed">Feeling overwhelmed? Connect with an on-call counselor immediately. We are here for you 24/7.</p>
                            <button class="bg-white text-indigo-900 px-8 py-3 rounded-xl font-bold hover:bg-indigo-50 transition-colors relative z-10 shadow-lg">Get Immediate Help</button>
                        </div>
                    </div>
                </section>

                <!-- Online Facetime Section -->
                <section id="facetime-section" class="section h-full hidden">
                    <div class="h-full flex flex-col">
                        <div class="flex-1 bg-gray-900 rounded-3xl overflow-hidden relative shadow-2xl border-8 border-white">
                            <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?auto=format&fit=crop&q=80&w=1000" class="w-full h-full object-cover opacity-80">
                            
                            <!-- Participant Name Overlay -->
                            <div class="absolute bottom-10 left-10">
                                <div class="bg-black/30 backdrop-blur-md px-6 py-3 rounded-2xl border border-white/20">
                                    <h4 class="text-white font-black text-xl">Dr. Sarah Smith</h4>
                                    <p class="text-indigo-300 text-sm font-medium">Session in progress • 12:45</p>
                                </div>
                            </div>

                            <!-- Self View -->
                            <div class="absolute top-10 right-10 w-64 h-40 bg-gray-800 rounded-2xl border-4 border-white shadow-2xl overflow-hidden">
                                <div class="w-full h-full bg-indigo-500 flex items-center justify-center text-white">
                                    <i class="fas fa-user text-6xl opacity-30"></i>
                                </div>
                                <div class="absolute bottom-3 left-3 bg-black/50 px-3 py-1 rounded-lg">
                                    <p class="text-white text-xs font-bold">You (John)</p>
                                </div>
                            </div>

                            <!-- Controls Bar -->
                            <div class="absolute bottom-10 left-1/2 -translate-x-1/2 flex items-center space-x-6">
                                <button class="w-14 h-14 bg-white/20 backdrop-blur-xl text-white rounded-full flex items-center justify-center hover:bg-white/40 transition-all border border-white/30">
                                    <i class="fas fa-microphone text-xl"></i>
                                </button>
                                <button class="w-14 h-14 bg-white/20 backdrop-blur-xl text-white rounded-full flex items-center justify-center hover:bg-white/40 transition-all border border-white/30">
                                    <i class="fas fa-video text-xl"></i>
                                </button>
                                <button class="w-20 h-14 bg-red-500 text-white rounded-2xl flex items-center justify-center hover:bg-red-600 transition-all shadow-lg">
                                    <i class="fas fa-phone-slash text-2xl rotate-[135deg]"></i>
                                </button>
                                <button class="w-14 h-14 bg-white/20 backdrop-blur-xl text-white rounded-full flex items-center justify-center hover:bg-white/40 transition-all border border-white/30">
                                    <i class="fas fa-comment-alt text-xl"></i>
                                </button>
                                <button class="w-14 h-14 bg-white/20 backdrop-blur-xl text-white rounded-full flex items-center justify-center hover:bg-white/40 transition-all border border-white/30">
                                    <i class="fas fa-ellipsis-h text-xl"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- AI Chatbot Section -->
                <section id="chatbot-section" class="section h-full flex flex-col hidden">
                    <div class="flex-1 flex flex-col bg-white rounded-3xl shadow-xl border border-gray-100 overflow-hidden">
                        <div class="p-6 border-b border-gray-100 flex items-center justify-between bg-indigo-50/30">
                            <div class="flex items-center">
                                <div class="w-12 h-12 bg-indigo-600 rounded-2xl flex items-center justify-center text-white mr-4 shadow-lg shadow-indigo-200">
                                    <i class="fas fa-robot text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-black text-gray-800">MindCare AI</h4>
                                    <p class="text-xs text-green-500 font-bold flex items-center uppercase tracking-tighter">
                                        <span class="w-2 h-2 bg-green-500 rounded-full mr-2 animate-pulse"></span> Always Online
                                    </p>
                                </div>
                            </div>
                            <button class="text-gray-400 hover:text-indigo-600 transition-colors"><i class="fas fa-history"></i></button>
                        </div>
                        <div id="chat-messages" class="flex-1 overflow-y-auto p-8 space-y-6 bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] [background-size:20px_20px]">
                            <!-- Welcome Message -->
                            <div class="flex items-start">
                                <div class="w-10 h-10 bg-indigo-100 rounded-xl flex items-center justify-center text-indigo-600 flex-shrink-0 mr-4">
                                    <i class="fas fa-robot"></i>
                                </div>
                                <div class="bg-white p-5 rounded-2xl rounded-tl-none shadow-sm border border-gray-100 max-w-xl leading-relaxed">
                                    <p class="text-gray-800">Hi John! I'm your private AI companion. Whatever is on your mind, you can share it here safely. How are you feeling right now?</p>
                                </div>
                            </div>
                        </div>
                        <div class="p-6 bg-white border-t border-gray-100">
                            <form id="chat-form" class="flex space-x-4">
                                <input type="text" id="chat-input" placeholder="Type what's on your mind..." class="flex-1 bg-gray-50 border-none rounded-2xl px-6 py-4 focus:ring-2 focus:ring-indigo-500 focus:bg-white transition-all text-gray-800">
                                <button type="submit" class="bg-indigo-600 text-white w-14 h-14 rounded-2xl hover:bg-indigo-700 transition-all shadow-lg shadow-indigo-200 flex items-center justify-center">
                                    <i class="fas fa-paper-plane"></i>
                                </button>
                            </form>
                        </div>
                    </div>
                </section>

                <!-- Scheduling Section -->
                <section id="scheduling-section" class="section hidden">
                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                        <!-- Calendar Placeholder -->
                        <div class="lg:col-span-2 bg-white rounded-3xl p-8 shadow-sm border border-gray-100">
                            <div class="flex items-center justify-between mb-10">
                                <h3 class="text-2xl font-black text-gray-800">October 2023</h3>
                                <div class="flex space-x-3">
                                    <button class="w-10 h-10 border border-gray-200 rounded-xl hover:bg-gray-50"><i class="fas fa-chevron-left text-xs"></i></button>
                                    <button class="w-10 h-10 border border-gray-200 rounded-xl hover:bg-gray-50"><i class="fas fa-chevron-right text-xs"></i></button>
                                </div>
                            </div>
                            <div class="grid grid-cols-7 gap-4 text-center">
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Sun</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Mon</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Tue</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Wed</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Thu</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Fri</div>
                                <div class="text-xs font-black text-gray-400 uppercase tracking-widest mb-4">Sat</div>
                                
                                <!-- Mock Dates -->
                                <div class="h-20 bg-gray-50 rounded-2xl flex flex-col items-center justify-center text-gray-300">28</div>
                                <div class="h-20 bg-gray-50 rounded-2xl flex flex-col items-center justify-center text-gray-300">29</div>
                                <div class="h-20 bg-gray-50 rounded-2xl flex flex-col items-center justify-center text-gray-300">30</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">1</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold bg-indigo-600 text-white shadow-lg">2</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">3</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">4</div>
                                
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">5</div>
                                <div class="h-20 border border-indigo-200 bg-indigo-50/50 rounded-2xl flex flex-col items-center justify-center font-bold relative">
                                    6
                                    <span class="absolute bottom-3 w-1.5 h-1.5 bg-indigo-600 rounded-full"></span>
                                </div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">7</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">8</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">9</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">10</div>
                                <div class="h-20 border border-gray-100 rounded-2xl flex flex-col items-center justify-center font-bold">11</div>
                            </div>
                        </div>

                        <div class="space-y-8">
                            <div class="bg-white rounded-3xl p-6 shadow-sm border border-gray-100">
                                <h4 class="font-black text-gray-800 mb-6">Upcoming</h4>
                                <div class="space-y-4">
                                    <div class="p-4 bg-indigo-50/50 rounded-2xl border-l-4 border-indigo-600">
                                        <p class="text-[10px] font-black text-indigo-600 uppercase mb-1">Tomorrow, 10 AM</p>
                                        <p class="text-sm font-bold text-gray-800">Dr. Sarah Smith</p>
                                    </div>
                                    <div class="p-4 bg-purple-50/50 rounded-2xl border-l-4 border-purple-600">
                                        <p class="text-[10px] font-black text-purple-600 uppercase mb-1">Oct 15, 4 PM</p>
                                        <p class="text-sm font-bold text-gray-800">Group Session #4</p>
                                    </div>
                                </div>
                            </div>
                            <div class="bg-indigo-600 rounded-3xl p-8 text-white shadow-xl shadow-indigo-100">
                                <h4 class="font-bold text-xl mb-4">Plan Ahead</h4>
                                <p class="text-indigo-100 text-sm leading-relaxed mb-6">Regular check-ins lead to 40% better outcomes. Book your sessions for the next month today.</p>
                                <button class="w-full bg-white text-indigo-600 py-4 rounded-2xl font-black text-sm hover:bg-indigo-50 transition-colors">Schedule All</button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Contact List Section -->
                <section id="contacts-section" class="section hidden">
                    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-8">
                        <!-- Expert Card 1 -->
                        <div class="bg-white p-8 rounded-3xl shadow-sm border border-gray-100 hover:shadow-xl transition-all group">
                            <div class="flex flex-col items-center text-center">
                                <div class="relative mb-6">
                                    <img src="https://i.pravatar.cc/150?u=sarah" class="w-24 h-24 rounded-3xl object-cover ring-4 ring-indigo-50 group-hover:ring-indigo-200 transition-all">
                                    <span class="absolute bottom-0 right-0 w-6 h-6 bg-green-500 border-4 border-white rounded-full"></span>
                                </div>
                                <h4 class="text-xl font-black text-gray-800">Dr. Sarah Smith</h4>
                                <p class="text-indigo-600 font-bold text-sm mb-4">Clinical Psychologist</p>
                                <div class="flex space-x-2 mb-6">
                                    <span class="px-3 py-1 bg-gray-100 rounded-lg text-[10px] font-bold text-gray-500">Anxiety</span>
                                    <span class="px-3 py-1 bg-gray-100 rounded-lg text-[10px] font-bold text-gray-500">CBT</span>
                                    <span class="px-3 py-1 bg-gray-100 rounded-lg text-[10px] font-bold text-gray-500">Stress</span>
                                </div>
                                <div class="grid grid-cols-2 gap-3 w-full">
                                    <button class="bg-indigo-600 text-white py-3 rounded-xl text-xs font-black hover:bg-indigo-700 transition-colors shadow-lg shadow-indigo-100">Book Session</button>
                                    <button class="bg-gray-50 text-gray-600 py-3 rounded-xl text-xs font-black hover:bg-gray-100 transition-colors">View Profile</button>
                                </div>
                            </div>
                        </div>

                        <!-- Expert Card 2 -->
                        <div class="bg-white p-8 rounded-3xl shadow-sm border border-gray-100 hover:shadow-xl transition-all group">
                            <div class="flex flex-col items-center text-center">
                                <div class="relative mb-6">
                                    <img src="https://i.pravatar.cc/150?u=michael" class="w-24 h-24 rounded-3xl object-cover ring-4 ring-indigo-50 group-hover:ring-indigo-200 transition-all">
                                    <span class="absolute bottom-0 right-0 w-6 h-6 bg-green-500 border-4 border-white rounded-full"></span>
                                </div>
                                <h4 class="text-xl font-black text-gray-800">Dr. Michael Chen</h4>
                                <p class="text-indigo-600 font-bold text-sm mb-4">Behavioral Expert</p>
                                <div class="flex space-x-2 mb-6">
                                    <span class="px-3 py-1 bg-gray-100 rounded-lg text-[10px] font-bold text-gray-500">OCD</span>
                                    <span class="px-3 py-1 bg-gray-100 rounded-lg text-[10px] font-bold text-gray-500">Habits</span>
                                </div>
                                <div class="grid grid-cols-2 gap-3 w-full">
                                    <button class="bg-indigo-600 text-white py-3 rounded-xl text-xs font-black hover:bg-indigo-700 transition-colors shadow-lg shadow-indigo-100">Book Session</button>
                                    <button class="bg-gray-50 text-gray-600 py-3 rounded-xl text-xs font-black hover:bg-gray-100 transition-colors">View Profile</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Group Session Section -->
                <section id="group-section" class="section h-full hidden">
                    <div class="h-full flex flex-col lg:flex-row gap-8">
                        <div class="flex-1 bg-gray-900 rounded-3xl relative overflow-hidden flex flex-col">
                            <div class="flex-1 grid grid-cols-2 gap-4 p-6">
                                <div class="bg-gray-800 rounded-2xl relative overflow-hidden">
                                    <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?auto=format&fit=crop&q=80&w=400" class="w-full h-full object-cover opacity-60">
                                    <div class="absolute bottom-4 left-4 bg-black/50 backdrop-blur-md px-3 py-1 rounded-lg text-[10px] text-white font-bold">Dr. Sarah (Host)</div>
                                </div>
                                <div class="bg-gray-800 rounded-2xl relative overflow-hidden">
                                    <img src="https://i.pravatar.cc/400?u=mark" class="w-full h-full object-cover opacity-50">
                                    <div class="absolute bottom-4 left-4 bg-black/50 backdrop-blur-md px-3 py-1 rounded-lg text-[10px] text-white font-bold">Mark</div>
                                </div>
                                <div class="bg-gray-800 rounded-2xl relative overflow-hidden border-4 border-indigo-500 shadow-[0_0_20px_rgba(79,70,229,0.3)]">
                                    <div class="w-full h-full flex items-center justify-center bg-indigo-900/40">
                                        <i class="fas fa-user text-6xl text-indigo-400"></i>
                                    </div>
                                    <div class="absolute bottom-4 left-4 bg-indigo-600 px-3 py-1 rounded-lg text-[10px] text-white font-bold">You (John)</div>
                                </div>
                                <div class="bg-gray-800 rounded-2xl relative overflow-hidden">
                                    <img src="https://i.pravatar.cc/400?u=lisa" class="w-full h-full object-cover opacity-50">
                                    <div class="absolute bottom-4 left-4 bg-black/50 backdrop-blur-md px-3 py-1 rounded-lg text-[10px] text-white font-bold">Lisa</div>
                                </div>
                            </div>
                            <div class="h-20 bg-black/40 backdrop-blur-xl flex items-center justify-center space-x-6 border-t border-white/10">
                                <button class="w-12 h-12 bg-white/10 text-white rounded-full flex items-center justify-center hover:bg-white/20 transition-all"><i class="fas fa-microphone"></i></button>
                                <button class="w-12 h-12 bg-white/10 text-white rounded-full flex items-center justify-center hover:bg-white/20 transition-all"><i class="fas fa-video"></i></button>
                                <button class="w-16 h-12 bg-red-500 text-white rounded-xl flex items-center justify-center hover:bg-red-600 transition-all shadow-lg shadow-red-500/30"><i class="fas fa-phone-slash"></i></button>
                            </div>
                        </div>

                        <div class="w-full lg:w-80 bg-white rounded-3xl border border-gray-100 shadow-sm flex flex-col overflow-hidden">
                            <div class="p-6 border-b border-gray-100 bg-gray-50/50">
                                <h4 class="font-black text-gray-800">Participants <span class="ml-2 text-indigo-600 bg-indigo-50 px-2 py-0.5 rounded text-xs">12</span></h4>
                            </div>
                            <div class="flex-1 overflow-y-auto p-6 space-y-4">
                                <div class="flex items-center">
                                    <div class="w-8 h-8 bg-indigo-600 rounded-lg flex items-center justify-center text-white mr-3 text-xs font-black">S</div>
                                    <span class="text-sm font-bold text-gray-700">Dr. Sarah Smith</span>
                                    <i class="fas fa-crown text-amber-400 ml-auto text-xs"></i>
                                </div>
                                <div class="flex items-center">
                                    <div class="w-8 h-8 bg-gray-100 rounded-lg flex items-center justify-center text-gray-600 mr-3 text-xs font-black">Y</div>
                                    <span class="text-sm font-bold text-gray-900">You</span>
                                    <i class="fas fa-microphone-slash text-red-400 ml-auto text-xs"></i>
                                </div>
                            </div>
                            <div class="p-6 bg-indigo-50/30">
                                <p class="text-[10px] text-gray-400 font-black uppercase mb-3">Group Chat</p>
                                <div class="bg-white p-3 rounded-xl border border-indigo-100 text-xs text-gray-600 shadow-sm">
                                    <span class="font-bold text-indigo-600">Mark:</span> Welcome to the session!
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Universities Section -->
                <section id="universities-section" class="section hidden">
                    <div class="mb-10">
                        <h3 class="text-3xl font-black text-gray-900">University Hub</h3>
                        <p class="text-gray-500 mt-2">Find localized support and campus-specific mental health resources.</p>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div class="bg-white rounded-3xl p-8 border border-gray-100 shadow-sm hover:shadow-xl transition-all">
                            <div class="flex items-center mb-8">
                                <div class="w-16 h-16 bg-red-50 rounded-2xl flex items-center justify-center text-red-600 mr-5">
                                    <i class="fas fa-university text-2xl"></i>
                                </div>
                                <div>
                                    <h4 class="text-xl font-black text-gray-800">Stanford University</h4>
                                    <p class="text-sm text-gray-400">Vaden Health Services</p>
                                </div>
                            </div>
                            <div class="space-y-3 mb-10">
                                <div class="flex items-center text-sm text-gray-600 bg-gray-50 p-3 rounded-xl"><i class="fas fa-phone-alt mr-3 text-indigo-500"></i> 24/7 Crisis Line</div>
                                <div class="flex items-center text-sm text-gray-600 bg-gray-50 p-3 rounded-xl"><i class="fas fa-map-marker-alt mr-3 text-indigo-500"></i> 866 Campus Dr, Stanford</div>
                            </div>
                            <button class="w-full bg-indigo-600 text-white py-4 rounded-2xl font-black shadow-lg shadow-indigo-100 hover:bg-indigo-700 transition-all">Connect to Portal</button>
                        </div>
                    </div>
                </section>

                <!-- Community Section -->
                <section id="community-section" class="section hidden">
                    <div class="flex flex-col lg:flex-row gap-10">
                        <div class="flex-1 space-y-8">
                            <!-- Post Box -->
                            <div class="bg-white p-8 rounded-3xl shadow-sm border border-gray-100">
                                <textarea placeholder="Share your wellness journey or a word of encouragement..." class="w-full bg-gray-50 border-none rounded-2xl p-6 text-sm focus:ring-2 focus:ring-indigo-500 transition-all mb-4" rows="3"></textarea>
                                <div class="flex items-center justify-between">
                                    <div class="flex space-x-4 text-gray-400">
                                        <i class="far fa-image hover:text-indigo-600 cursor-pointer"></i>
                                        <i class="far fa-smile hover:text-indigo-600 cursor-pointer"></i>
                                    </div>
                                    <button class="bg-indigo-600 text-white px-10 py-3 rounded-2xl font-black text-sm shadow-lg shadow-indigo-100 hover:bg-indigo-700 transition-all">Post</button>
                                </div>
                            </div>

                            <!-- Feed -->
                            <div class="bg-white p-8 rounded-3xl shadow-sm border border-gray-100 group">
                                <div class="flex items-center mb-6">
                                    <img src="https://i.pravatar.cc/100?u=emily" class="w-12 h-12 rounded-xl mr-4">
                                    <div>
                                        <h5 class="font-black text-gray-800">Emily M.</h5>
                                        <p class="text-[10px] font-bold text-gray-400 uppercase tracking-widest">2 hours ago</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 leading-relaxed mb-6 italic">"Just finished my therapy session through MindCare. It feels amazing to finally talk about my exam stress. Remember: it's okay not to be okay! 💙"</p>
                                <div class="flex items-center space-x-8 text-gray-400">
                                    <button class="flex items-center text-xs font-bold hover:text-red-500 transition-colors"><i class="far fa-heart mr-2"></i> 142</button>
                                    <button class="flex items-center text-xs font-bold hover:text-indigo-600 transition-colors"><i class="far fa-comment mr-2"></i> 28</button>
                                </div>
                            </div>
                        </div>

                        <div class="lg:w-80 space-y-8">
                            <div class="bg-white p-8 rounded-3xl shadow-sm border border-gray-100">
                                <h4 class="font-black text-gray-800 mb-6">Trending Topics</h4>
                                <div class="space-y-4">
                                    <p class="text-sm font-bold text-indigo-600 cursor-pointer hover:underline">#MindfulMonday</p>
                                    <p class="text-sm font-bold text-indigo-600 cursor-pointer hover:underline">#ExamSeasonWellness</p>
                                    <p class="text-sm font-bold text-indigo-600 cursor-pointer hover:underline">#SleepHygieneTips</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

            </div>
        </main>
    </div>

    <script>
        // Smooth Navigation Logic
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const sectionId = link.getAttribute('data-section');
                
                // Active link UI
                document.querySelectorAll('.nav-link').forEach(l => {
                    l.classList.remove('bg-indigo-800');
                    l.classList.add('hover:bg-indigo-600');
                });
                link.classList.add('bg-indigo-800');
                link.classList.remove('hover:bg-indigo-600');

                // Switch sections
                document.querySelectorAll('.section').forEach(section => {
                    section.classList.add('hidden');
                    section.classList.remove('active');
                });
                const activeSection = document.getElementById(`${sectionId}-section`);
                activeSection.classList.remove('hidden');
                activeSection.classList.add('active');

                // Page Title mapping
                const titles = {
                    'home': 'Dashboard',
                    'facetime': 'Online Facetime',
                    'chatbot': 'AI Chatbot',
                    'scheduling': 'Scheduling',
                    'contacts': 'Professional Directory',
                    'group': 'Group Support',
                    'universities': 'University Hub',
                    'community': 'MindCare Community'
                };
                document.getElementById('section-title').innerText = titles[sectionId];
                
                // Scroll to top of content
                document.getElementById('content').scrollTop = 0;
            });
        });

        // Interactive AI Chatbot Logic
        const chatForm = document.getElementById('chat-form');
        const chatInput = document.getElementById('chat-input');
        const chatMessages = document.getElementById('chat-messages');

        const aiResponses = [
            "That's very insightful. How long have you been feeling this way?",
            "I'm here for you. Take a deep breath and tell me more.",
            "That sounds like a lot to handle. Remember, you're making progress just by being here.",
            "It's completely normal to feel that way during the semester. Would you like to try a quick grounding exercise?",
            "I understand. Have you spoken with a professional specialist about this before?",
            "You're being very brave by sharing this. What does self-care look like for you today?",
            "Small steps lead to big changes. What's one tiny thing you can do for yourself tonight?"
        ];

        function addMessage(text, isUser = false) {
            const messageDiv = document.createElement('div');
            messageDiv.className = `flex items-start ${isUser ? 'justify-end' : ''}`;
            
            const content = isUser 
                ? `<div class="bg-indigo-600 text-white p-5 rounded-2xl rounded-tr-none shadow-md max-w-xl leading-relaxed">
                        <p class="text-sm font-medium">${text}</p>
                   </div>`
                : `<div class="w-10 h-10 bg-indigo-100 rounded-xl flex items-center justify-center text-indigo-600 flex-shrink-0 mr-4">
                        <i class="fas fa-robot"></i>
                   </div>
                   <div class="bg-white p-5 rounded-2xl rounded-tl-none shadow-sm border border-gray-100 max-w-xl leading-relaxed">
                        <p class="text-sm text-gray-800">${text}</p>
                   </div>`;
            
            messageDiv.innerHTML = content;
            chatMessages.appendChild(messageDiv);
            
            // Auto-scroll with smooth effect
            chatMessages.scrollTo({
                top: chatMessages.scrollHeight,
                behavior: 'smooth'
            });
        }

        chatForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const message = chatInput.value.trim();
            if (message) {
                addMessage(message, true);
                chatInput.value = '';
                
                // Show AI 'typing' delay
                setTimeout(() => {
                    const randomResponse = aiResponses[Math.floor(Math.random() * aiResponses.length)];
                    addMessage(randomResponse, false);
                }, 1200);
            }
        });
    </script>
</body>
</html>
