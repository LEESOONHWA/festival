# festival
2026 함께 성장 페스티벌 나의 대학생활 AI 콘텐츠 공모전
<!DOCTYPE html>
<html lang="ko" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 함께 성장 페스티벌 - AI 콘텐츠 공모전</title>
    <!-- Tailwind CSS (CDN) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f5f3ff',
                            100: '#ede9fe',
                            500: '#8b5cf6',
                            600: '#7c3aed',
                            700: '#6d28d9',
                            900: '#4c1d95',
                        },
                        neon: {
                            pink: '#ff2a85',
                            blue: '#00f0ff',
                            purple: '#9d00ff'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'Pretendard', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Pretendard:wght@400;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Chart.js for Admin Analytics -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Pretendard', sans-serif;
            background-color: #0b0f19;
            color: #f3f4f6;
            overflow-x: hidden;
        }
        
        .glow-effect {
            box-shadow: 0 0 25px rgba(139, 92, 246, 0.35);
        }

        .glow-card:hover {
            box-shadow: 0 0 30px rgba(0, 240, 255, 0.4);
            transform: translateY(-4px);
        }

        /* Glassmorphism styling */
        .glass {
            background: rgba(17, 24, 39, 0.7);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .gradient-text {
            background: linear-gradient(135deg, #00f0ff 0%, #ff2a85 50%, #9d00ff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .gradient-btn {
            background: linear-gradient(90deg, #7c3aed 0%, #ff2a85 100%);
            transition: all 0.3s ease;
        }

        .gradient-btn:hover {
            opacity: 0.95;
            box-shadow: 0 0 20px rgba(255, 42, 133, 0.6);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0f19;
        }
        ::-webkit-scrollbar-thumb {
            background: #374151;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #6b7280;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-brand-500 selection:text-white">

    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 glass border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3 cursor-pointer" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
                <div class="w-10 h-10 rounded-xl gradient-btn flex items-center justify-center text-white font-black text-xl shadow-lg">
                    AI
                </div>
                <div>
                    <span class="text-xs text-brand-500 font-bold tracking-widest block uppercase">2026 Festival</span>
                    <h1 class="text-lg font-extrabold text-white leading-tight">함께 성장 페스티벌</h1>
                </div>
            </div>

            <nav class="hidden md:flex items-center gap-8 font-semibold text-sm">
                <a href="#about" class="hover:text-brand-500 transition-colors">행사 소개</a>
                <a href="#categories" class="hover:text-brand-500 transition-colors">공모 분야</a>
                <a href="#apply" class="hover:text-brand-500 transition-colors">신청서 작성</a>
                <a href="#my-applications" class="hover:text-brand-500 transition-colors">작품 관람 & 투표</a>
            </nav>

            <div class="flex items-center gap-3">
                <button onclick="openAdminModal()" class="glass border border-brand-500/50 text-brand-300 hover:text-white px-4 py-2 rounded-full font-bold text-xs flex items-center gap-2 hover:bg-brand-500/20 transition-all">
                    <i class="fa-solid fa-chart-column text-brand-400"></i>
                    <span>관리자 투표 현황</span>
                </button>
                <a href="#apply" class="gradient-btn text-white px-5 py-2.5 rounded-full font-bold text-sm shadow-md flex items-center gap-2 hover:scale-105 transition-transform">
                    <span>참가 신청하기</span>
                    <i class="fa-solid fa-arrow-right text-xs"></i>
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Banner Section -->
    <section class="relative py-20 md:py-32 overflow-hidden flex items-center justify-center">
        <!-- Background Glowing Orbs -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-brand-600/20 rounded-full blur-[120px] pointer-events-none"></div>
        <div class="absolute top-1/3 right-10 w-[300px] h-[300px] bg-neon-pink/15 rounded-full blur-[100px] pointer-events-none"></div>
        
        <div class="max-w-5xl mx-auto px-4 text-center relative z-10">
            <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass border border-brand-500/30 text-brand-500 text-xs sm:text-sm font-semibold mb-6 animate-pulse">
                <i class="fa-solid fa-wand-magic-sparkles"></i> 2026 대학생 혁신 AI 콘텐츠 챌린지
            </div>
            
            <h1 class="text-4xl sm:text-6xl md:text-7xl font-black tracking-tight text-white mb-6 leading-tight sm:leading-none">
                AI로 넓히는 우리들의 <br>
                <span class="gradient-text">무한한 가능성 & 스토어</span>
            </h1>
            
            <p class="text-gray-400 text-base sm:text-lg md:text-xl max-w-2xl mx-auto mb-10 font-normal leading-relaxed">
                상상이 현실이 되는 대학 캠퍼스! AI 기술을 활용하여 당신만의 창의적인 학습 노하우와 즐거운 캠퍼스 라이프를 공유해주세요.
            </p>

            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                <a href="#apply" class="w-full sm:w-auto gradient-btn text-white px-8 py-4 rounded-2xl font-bold text-lg shadow-xl hover:scale-105 transition-all text-center flex items-center justify-center gap-2">
                    <i class="fa-solid fa-paper-plane"></i> 지금 바로 응모하기
                </a>
                <a href="#categories" class="w-full sm:w-auto glass text-gray-300 hover:text-white border border-gray-700 px-8 py-4 rounded-2xl font-bold text-lg hover:border-gray-500 transition-all text-center flex items-center justify-center gap-2">
                    <i class="fa-solid fa-circle-info"></i> 분야별 가이드 보기
                </a>
            </div>

            <!-- Stats/Badges -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-16 max-w-4xl mx-auto">
                <div class="glass p-4 rounded-2xl border border-gray-800">
                    <div class="text-2xl font-extrabold text-brand-500 mb-1">총 상금</div>
                    <div class="text-gray-300 text-sm">500만 원 및 총장상</div>
                </div>
                <div class="glass p-4 rounded-2xl border border-gray-800">
                    <div class="text-2xl font-extrabold text-neon-blue mb-1">접수 기간</div>
                    <div class="text-gray-300 text-sm">2026.11.01 ~ 11.25</div>
                </div>
                <div class="glass p-4 rounded-2xl border border-gray-800">
                    <div class="text-2xl font-extrabold text-neon-pink mb-1">참가 대상</div>
                    <div class="text-gray-300 text-sm">재학/휴학생 누구나</div>
                </div>
                <div class="glass p-4 rounded-2xl border border-gray-800">
                    <div class="text-2xl font-extrabold text-purple-400 mb-1">결과 발표</div>
                    <div class="text-gray-300 text-sm">2026.12.05 본선</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Section 1: Categories Overview -->
    <section id="categories" class="py-20 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-brand-500 mb-2">Category Guidelines</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">공모 영역 안내</h3>
                <p class="text-gray-400 mt-2">자신 있는 분야를 선택하여 여러분의 가치 있는 AI 콘텐츠를 제출하세요.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- AI 학습 부문 -->
                <div class="glass rounded-3xl p-8 border border-brand-500/30 hover:border-brand-500 transition-all glow-card relative overflow-hidden group">
                    <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-brand-600/10 rounded-full group-hover:scale-150 transition-transform pointer-events-none"></div>
                    
                    <div class="w-14 h-14 rounded-2xl bg-brand-500/20 text-brand-500 flex items-center justify-center text-2xl font-bold mb-6 border border-brand-500/30">
                        <i class="fa-solid fa-graduation-cap"></i>
                    </div>

                    <span class="px-3 py-1 bg-brand-500/20 text-brand-300 text-xs font-bold rounded-full mb-3 inline-block">CATEGORY 01</span>
                    <h4 class="text-2xl font-bold text-white mb-3">AI 학습 부문</h4>
                    <p class="text-gray-400 text-sm leading-relaxed mb-6">
                        학업 효율을 극대화한 AI 프롬프트 활용법, 전공 공부 및 시험 대비 튜토리얼, 직접 개발한 학습 보조 AI 챗봇 등 스마트한 학습 혁신 사례.
                    </p>

                    <div class="space-y-3 mb-8 text-sm">
                        <div class="flex items-start gap-2 text-gray-300">
                            <i class="fa-solid fa-check text-brand-500 mt-1"></i>
                            <span><b>예시 주제:</b> 전공 서적 요약 Prompt 노하우, AI 기반 시험 대비 문제 생성기, 논문 분석 팁</span>
                        </div>
                        <div class="flex items-start gap-2 text-gray-300">
                            <i class="fa-solid fa-check text-brand-500 mt-1"></i>
                            <span><b>제출 형식:</b> 활용 가이드 PDF, 시연 영상 (3분 이내), 프롬프트 템플릿 등</span>
                        </div>
                    </div>

                    <button onclick="selectCategory('study')" class="w-full py-3 rounded-xl bg-brand-600/30 border border-brand-500/50 text-white font-bold hover:bg-brand-600 transition-colors flex items-center justify-center gap-2">
                        <span>학습 부문으로 신청하기</span>
                        <i class="fa-solid fa-arrow-right text-xs"></i>
                    </button>
                </div>

                <!-- AI 캠퍼스라이프 부문 -->
                <div class="glass rounded-3xl p-8 border border-neon-pink/30 hover:border-neon-pink transition-all glow-card relative overflow-hidden group">
                    <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-neon-pink/10 rounded-full group-hover:scale-150 transition-transform pointer-events-none"></div>

                    <div class="w-14 h-14 rounded-2xl bg-neon-pink/20 text-neon-pink flex items-center justify-center text-2xl font-bold mb-6 border border-neon-pink/30">
                        <i class="fa-solid fa-icons"></i>
                    </div>

                    <span class="px-3 py-1 bg-neon-pink/20 text-pink-300 text-xs font-bold rounded-full mb-3 inline-block">CATEGORY 02</span>
                    <h4 class="text-2xl font-bold text-white mb-3">AI 캠퍼스라이프 부문</h4>
                    <p class="text-gray-400 text-sm leading-relaxed mb-6">
                        AI 생성 이미지를 활용한 웹툰/포스터, AI 음악/영상으로 제작한 대학 홍보/일상 숏폼, 캠퍼스 동아리/축제 관련 AI 크리에이티브 콘텐츠.
                    </p>

                    <div class="space-y-3 mb-8 text-sm">
                        <div class="flex items-start gap-2 text-gray-300">
                            <i class="fa-solid fa-check text-neon-pink mt-1"></i>
                            <span><b>예시 주제:</b> AI 생성 음악 숏폼 뮤직비디오, AI 화풍 캠퍼스 4컷 만화, AI 대학 로고 및 캐릭터</span>
                        </div>
                        <div class="flex items-start gap-2 text-gray-300">
                            <i class="fa-solid fa-check text-neon-pink mt-1"></i>
                            <span><b>제출 형식:</b> 이미지/디지털 아트워크, MP4 영상 파일, 음원 링크 등</span>
                        </div>
                    </div>

                    <button onclick="selectCategory('campus')" class="w-full py-3 rounded-xl bg-neon-pink/20 border border-neon-pink/50 text-white font-bold hover:bg-neon-pink/40 transition-colors flex items-center justify-center gap-2">
                        <span>캠퍼스라이프 부문으로 신청하기</span>
                        <i class="fa-solid fa-arrow-right text-xs"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Section 2: Application Form -->
    <section id="apply" class="py-20 relative bg-gray-900/40 border-y border-gray-800">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <span class="px-3 py-1 bg-purple-500/10 text-purple-400 text-xs font-bold rounded-full border border-purple-500/20">ONLINE REGISTRATION</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-white mt-3">참가 신청서 제출</h2>
                <p class="text-gray-400 mt-2">필요한 정보를 입력하고 작성한 AI 콘텐츠 양식을 제출해 주세요.</p>
            </div>

            <!-- Form Container -->
            <form id="applicationForm" onsubmit="handleFormSubmit(event)" class="glass p-6 sm:p-10 rounded-3xl border border-gray-700 shadow-2xl space-y-8">
                
                <!-- Category Select Option -->
                <div>
                    <label class="block text-sm font-bold text-gray-200 mb-3">공모 부문 선택 <span class="text-red-500">*</span></label>
                    <div class="grid grid-cols-2 gap-4">
                        <label id="label-study" class="flex items-center justify-center gap-3 p-4 rounded-xl border border-gray-700 cursor-pointer bg-gray-800/50 hover:bg-gray-800 transition-all">
                            <input type="radio" name="category" value="AI 학습부문" required class="text-brand-600 focus:ring-brand-500" onchange="updateCategoryStyle('study')">
                            <span class="font-bold text-sm text-gray-200"><i class="fa-solid fa-book-open mr-1"></i> AI 학습부문</span>
                        </label>
                        <label id="label-campus" class="flex items-center justify-center gap-3 p-4 rounded-xl border border-gray-700 cursor-pointer bg-gray-800/50 hover:bg-gray-800 transition-all">
                            <input type="radio" name="category" value="AI 캠퍼스라이프부문" required class="text-neon-pink focus:ring-neon-pink" onchange="updateCategoryStyle('campus')">
                            <span class="font-bold text-sm text-gray-200"><i class="fa-solid fa-camera-retro mr-1"></i> AI 캠퍼스라이프부문</span>
                        </label>
                    </div>
                </div>

                <!-- Personal Info Grid -->
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-2">참가자 이름 (팀장) <span class="text-red-500">*</span></label>
                        <input type="text" id="applicantName" required placeholder="홍길동" class="w-full bg-gray-800/80 border border-gray-700 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-brand-500 transition-colors">
                    </div>
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-2">학번 <span class="text-red-500">*</span></label>
                        <input type="text" id="studentId" required placeholder="20261234" class="w-full bg-gray-800/80 border border-gray-700 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-brand-500 transition-colors">
                    </div>
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-2">학과 / 학부 <span class="text-red-500">*</span></label>
                        <input type="text" id="department" required placeholder="인공지능소프트웨어학과" class="w-full bg-gray-800/80 border border-gray-700 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-brand-500 transition-colors">
                    </div>
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-2">연락처 <span class="text-red-500">*</span></label>
                        <input type="tel" id="phone" required placeholder="010-1234-5678" class="w-full bg-gray-800/80 border border-gray-700 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-brand-500 transition-colors">
                    </div>
                </div>

                <!-- Team Info -->
                <div>
                    <label class="block text-sm font-bold text-gray-200 mb-2">팀원 정보 <span class="text-xs font-normal text-gray-400">(개인 참가 시 생략 가능)</span></label>
                    <input type="text" id="teamMembers" placeholder="팀원 이름 및 학번 입력 (예: 김철수(20265678), 이영희(20269012))" class="w-full bg-gray-800/80 border border-gray-700 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-brand-500 transition-colors">
                </div>

                <!-- Content Info -->
                <div class="space-y-6 pt-4 border-t border-gray-800">
                    <div>
    <!-- Main Section 3: Applications List & Student Voting -->
    <section id="my-applications" class="py-20 relative">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-center justify-between mb-8 gap-4">
                <div>
                    <span class="px-3 py-1 bg-neon-blue/10 text-neon-blue text-xs font-bold rounded-full border border-neon-blue/20">STUDENT VOTE</span>
                    <h3 class="text-2xl font-bold text-white mt-1">작품 관람 & 학생 인기 투표</h3>
                    <p class="text-sm text-gray-400">학우들의 창의적인 AI 작품을 관람하고 가장 마음에 드는 작품에 투표하세요!</p>
                </div>
                <div class="flex items-center gap-2">
                    <button onclick="filterApplications('ALL')" class="px-3 py-1.5 rounded-lg text-xs font-bold glass text-white hover:bg-gray-800">전체</button>
                    <button onclick="filterApplications('AI 학습부문')" class="px-3 py-1.5 rounded-lg text-xs font-bold bg-brand-500/20 text-brand-300 border border-brand-500/30">학습부문</button>
                    <button onclick="filterApplications('AI 캠퍼스라이프부문')" class="px-3 py-1.5 rounded-lg text-xs font-bold bg-neon-pink/20 text-pink-300 border border-neon-pink/30">캠퍼스라이프부문</button>
                </div>
            </div>

            <!-- List Container -->
            <div id="applicationsList" class="space-y-4">
                <!-- JS will inject items here -->
            </div>
        </div>
    </section>

    <!-- Admin Live Vote Dashboard Modal -->
    <div id="adminModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md opacity-0 pointer-events-none transition-all duration-300">
        <div class="glass max-w-4xl w-full p-6 sm:p-8 rounded-3xl border border-brand-500/40 shadow-2xl relative max-h-[90vh] overflow-y-auto">
            <button onclick="closeAdminModal()" class="absolute top-6 right-6 text-gray-400 hover:text-white text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <div class="flex items-center gap-3 mb-6">
                <div class="w-10 h-10 rounded-xl bg-brand-500/20 text-brand-400 flex items-center justify-center text-lg font-bold border border-brand-500/30">
                    <i class="fa-solid fa-chart-line"></i>
                </div>
                <div>
                    <h3 class="text-xl font-bold text-white">관리자 실시간 투표 통계 대시보드</h3>
                    <p class="text-xs text-gray-400">실시간 관람 학생들의 인기 투표 현황 그래프입니다.</p>
                </div>
            </div>

            <!-- Stats Overview Cards -->
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8">
                <div class="bg-gray-900/60 p-4 rounded-2xl border border-gray-800">
                    <p class="text-xs text-gray-400 mb-1">총 누적 투표수</p>
                    <p id="totalVotesCount" class="text-2xl font-black text-brand-400">0표</p>
                </div>
                <div class="bg-gray-900/60 p-4 rounded-2xl border border-gray-800">
                    <p class="text-xs text-gray-400 mb-1">학습부문 1위</p>
                    <p id="topStudyWork" class="text-sm font-bold text-gray-200 truncate">-</p>
                </div>
                <div class="bg-gray-900/60 p-4 rounded-2xl border border-gray-800">
                    <p class="text-xs text-gray-400 mb-1">캠퍼스라이프부문 1위</p>
                    <p id="topCampusWork" class="text-sm font-bold text-gray-200 truncate">-</p>
                </div>
            </div>

            <!-- Graph Area -->
            <div class="bg-gray-900/80 p-6 rounded-2xl border border-gray-800 mb-6">
                <h4 class="text-sm font-bold text-gray-300 mb-4 flex items-center gap-2">
                    <i class="fa-solid fa-square-poll-vertical text-neon-blue"></i> 작품별 득표 실시간 그래프
                </h4>
                <div class="relative h-64 sm:h-80">
                    <canvas id="voteChart"></canvas>
                </div>
            </div>

            <div class="flex justify-end">
                <button onclick="closeAdminModal()" class="px-5 py-2.5 rounded-xl bg-gray-800 hover:bg-gray-700 text-white font-bold text-sm transition-colors">
                    닫기
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-gray-800 bg-black/50 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center sm:text-left flex flex-col sm:flex-row justify-between items-center gap-6">
            <div>
                <p class="font-bold text-gray-300 text-lg mb-1">2026 대학교 함께 성장 페스티벌</p>
                <p class="text-xs text-gray-500">주최: 대학 혁신지원사업단 | 문의: 051-123-4567 | ai_festival2026@univ.ac.kr</p>
            </div>
            <p class="text-xs text-gray-600">© 2026 University AI Festival. All rights reserved.</p>
        </div>
    </footer>

    <!-- Toast Notification Component -->
    <div id="toast" class="fixed bottom-8 right-8 z-50 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="glass px-6 py-4 rounded-2xl border border-brand-500 text-white font-bold flex items-center gap-3 shadow-2xl">
            <i class="fa-solid fa-circle-check text-brand-500 text-xl" id="toastIcon"></i>
            <span id="toastMessage">성공적으로 처리되었습니다.</span>
        </div>
    </div>

    <!-- JavaScript Logic -->
    <script>
        // Mock State Data with initial vote count and user voted status
        let applications = [
            {
                id: 1,
                category: 'AI 학습부문',
                applicantName: '김아인',
                studentId: '20261102',
                department: '컴퓨터공학과',
                phone: '010-9876-5432',
                teamMembers: '이배움(20261109)',
                title: 'AI 챗봇을 활용한 전공 가상 튜터 제작기',
                aiTools: 'ChatGPT, LangChain',
                description: '어려운 알고리즘 전공 개념을 질문-답변 형식으로 대화하며 복습할 수 있는 가상 튜터 프롬프트입니다.',
                linkUrl: 'https://notion.so/ai-tutor-example',
                votes: 42,
                date: '2026-11-02 14:30'
            },
            {
                id: 2,
                category: 'AI 캠퍼스라이프부문',
                applicantName: '박창작',
                studentId: '20263344',
                department: '시각디자인학과',
                phone: '010-1111-2222',
                teamMembers: '개인 참가',
                title: '2026 캠퍼스 봄 축제 AI 이미지 포스터 및 네온 굿즈 디자인',
                aiTools: 'Midjourney v6, Photoshop',
                description: '미래지향적인 우리 대학 캠퍼스의 봄 축제 모습을 미드저니로 시각화하여 포스터와 굿즈 디자인으로 확장했습니다.',
                linkUrl: 'https://youtube.com/watch?v=example',
                votes: 68,
                date: '2026-11-03 10:15'
            },
            {
                id: 3,
                category: 'AI 학습부문',
                applicantName: '최스마트',
                studentId: '20265511',
                department: '전자공학과',
                phone: '010-3333-4444',
                teamMembers: '정지능(20265512)',
                title: '자동 회로 해석 및 수식 풀이 AI 에이전트',
                aiTools: 'Claude 3.5, Python',
                description: '복잡한 회로도 이미지와 수학 방정식을 업로드하면 스텝별로 해석과 풀이를 알려주는 AI 보조 도구.',
                linkUrl: 'https://github.com/example',
                votes: 29,
                date: '2026-11-04 09:00'
            }
        ];

        let userVotedIds = new Set(); // Track voted items in session
        let currentFilter = 'ALL';
        let editingId = null;
        let voteChartInstance = null;

        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            renderApplications();
        });

        // Toggle Vote Function
        function toggleVote(id) {
            const app = applications.find(item => item.id === id);
            if(!app) return;

            if(userVotedIds.has(id)) {
                // Cancel Vote
                app.votes = Math.max(0, app.votes - 1);
                userVotedIds.delete(id);
                showToast("투표가 취소되었습니다.");
            } else {
                // Add Vote
                app.votes += 1;
                userVotedIds.add(id);
                showToast("👍 인기 투표에 반영되었습니다!");
            }

            renderApplications();
            if(document.getElementById('adminModal').classList.contains('opacity-100')) {
                updateAdminChart();
            }
        }

        // Handle File Selection Name UI
        function handleFileSelect(e) {
            const file = e.target.files[0];
            const display = document.getElementById('fileNameDisplay');
            if(file) {
                display.innerText = `선택된 파일: ${file.name} (${(file.size / 1024 / 1024).toFixed(2)}MB)`;
                display.classList.add('text-brand-500', 'font-bold');
            } else {
                display.innerText = 'PDF, ZIP, MP4 (최대 50MB)';
                display.classList.remove('text-brand-500', 'font-bold');
            }
        }

        // Category Select Helper
        function selectCategory(type) {
            const applySection = document.getElementById('apply');
            applySection.scrollIntoView({ behavior: 'smooth' });

            if(type === 'study') {
                const radio = document.querySelector('input[name="category"][value="AI 학습부문"]');
                if(radio) {
                    radio.checked = true;
                    updateCategoryStyle('study');
                }
            } else {
                const radio = document.querySelector('input[name="category"][value="AI 캠퍼스라이프부문"]');
                if(radio) {
                    radio.checked = true;
                    updateCategoryStyle('campus');
                }
            }
        }

        function updateCategoryStyle(selected) {
            const labelStudy = document.getElementById('label-study');
            const labelCampus = document.getElementById('label-campus');

            if(selected === 'study') {
                labelStudy.classList.add('border-brand-500', 'bg-brand-500/10');
                labelCampus.classList.remove('border-neon-pink', 'bg-neon-pink/10');
            } else {
                labelCampus.classList.add('border-neon-pink', 'bg-neon-pink/10');
                labelStudy.classList.remove('border-brand-500', 'bg-brand-500/10');
            }
        }

        // Form Submit Handler (Create or Update)
        function handleFormSubmit(e) {
            e.preventDefault();

            const category = document.querySelector('input[name="category"]:checked')?.value;
            const applicantName = document.getElementById('applicantName').value;
            const studentId = document.getElementById('studentId').value;
            const department = document.getElementById('department').value;
            const phone = document.getElementById('phone').value;
            const teamMembers = document.getElementById('teamMembers').value || '개인 참가';
            const title = document.getElementById('title').value;
            const aiTools = document.getElementById('aiTools').value;
            const description = document.getElementById('description').value;
            const linkUrl = document.getElementById('linkUrl').value || '#';

            const now = new Date();
            const dateStr = `${now.getFullYear()}-${String(now.getMonth()+1).padStart(2,'0')}-${String(now.getDate()).padStart(2,'0')} ${String(now.getHours()).padStart(2,'0')}:${String(now.getMinutes()).padStart(2,'0')}`;

            if(editingId) {
                // Update
                const idx = applications.findIndex(item => item.id === editingId);
                if(idx !== -1) {
                    applications[idx] = {
                        ...applications[idx],
                        category, applicantName, studentId, department, phone, teamMembers, title, aiTools, description, linkUrl
                    };
                    showToast("신청서가 성공적으로 수정되었습니다!");
                }
                editingId = null;
                document.getElementById('submitBtnText').innerText = "신청서 최종 제출하기";
            } else {
                // Create
                const newApp = {
                    id: Date.now(),
                    category,
                    applicantName,
                    studentId,
                    department,
                    phone,
                    teamMembers,
                    title,
                    aiTools,
                    description,
                    linkUrl,
                    votes: 0,
                    date: dateStr
                };
                applications.unshift(newApp);
                showToast("참가 신청서가 정상 접수되었습니다!");
            }

            // Reset Form
            document.getElementById('applicationForm').reset();
            document.getElementById('fileNameDisplay').innerText = 'PDF, ZIP, MP4 (최대 50MB)';
            document.getElementById('fileNameDisplay').classList.remove('text-brand-500', 'font-bold');
            updateCategoryStyle('');

            // Refresh List & Scroll
            renderApplications();
            document.getElementById('my-applications').scrollIntoView({ behavior: 'smooth' });
        }

        // Filter Applications
        function filterApplications(category) {
            currentFilter = category;
            renderApplications();
        }

        // Render Application Cards
        function renderApplications() {
            const listContainer = document.getElementById('applicationsList');
            const filtered = applications.filter(app => currentFilter === 'ALL' || app.category === currentFilter);

            if(filtered.length === 0) {
                listContainer.innerHTML = `
                    <div class="glass p-8 text-center text-gray-500 rounded-2xl">
                        <i class="fa-solid fa-folder-open text-3xl mb-2"></i>
                        <p>해당하는 신청 내역이 없습니다.</p>
                    </div>
                `;
                return;
            }

            listContainer.innerHTML = filtered.map(app => {
                const isStudy = app.category === 'AI 학습부문';
                const badgeColor = isStudy ? 'bg-brand-500/20 text-brand-300 border-brand-500/30' : 'bg-neon-pink/20 text-pink-300 border-neon-pink/30';
                const hasVoted = userVotedIds.has(app.id);
                
                return `
                    <div class="glass p-6 rounded-2xl border border-gray-800 hover:border-gray-700 transition-all relative group">
                        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 mb-3">
                            <div class="flex items-center gap-3">
                                <span class="px-3 py-1 rounded-full text-xs font-bold border ${badgeColor}">
                                    ${app.category}
                                </span>
                                <h4 class="text-xl font-bold text-white">${escapeHtml(app.title)}</h4>
                            </div>
                            <span class="text-xs text-gray-500"><i class="fa-regular fa-clock mr-1"></i>${app.date}</span>
                        </div>

                        <p class="text-gray-300 text-sm mb-4 leading-relaxed">${escapeHtml(app.description)}</p>

                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 text-xs text-gray-400 bg-gray-900/50 p-3 rounded-xl mb-4">
                            <div><b class="text-gray-200">참가자:</b> ${escapeHtml(app.applicantName)} (${escapeHtml(app.studentId)})</div>
                            <div><b class="text-gray-200">학과:</b> ${escapeHtml(app.department)}</div>
                            <div><b class="text-gray-200">AI 툴:</b> ${escapeHtml(app.aiTools)}</div>
                            <div class="col-span-1 sm:col-span-3"><b class="text-gray-200">팀원:</b> ${escapeHtml(app.teamMembers)}</div>
                        </div>

                        <div class="flex flex-wrap items-center justify-between gap-3 pt-3 border-t border-gray-800/80">
                            <div class="flex items-center gap-4">
                                <!-- Vote Button -->
                                <button onclick="toggleVote(${app.id})" class="flex items-center gap-2 px-4 py-2 rounded-xl text-xs font-extrabold transition-all ${
                                    hasVoted 
                                    ? 'bg-neon-pink text-white shadow-lg shadow-neon-pink/40 scale-105' 
                                    : 'bg-gray-800 text-gray-300 hover:bg-gray-700 border border-gray-700'
                                }">
                                    <i class="fa-solid fa-heart ${hasVoted ? 'animate-bounce text-white' : 'text-neon-pink'} text-sm"></i>
                                    <span>투표하기</span>
                                    <span class="ml-1 bg-black/30 px-2 py-0.5 rounded-full text-[11px]">${app.votes}</span>
                                </button>

                                ${app.linkUrl && app.linkUrl !== '#' ? `
                                    <a href="${escapeHtml(app.linkUrl)}" target="_blank" class="text-xs text-brand-400 hover:text-brand-300 hover:underline flex items-center gap-1">
                                        <i class="fa-solid fa-link"></i> 작품 원본 링크
                                    </a>
                                ` : ''}
                            </div>

                            <div class="flex items-center gap-2">
                                <button onclick="editApplication(${app.id})" class="px-3 py-1.5 rounded-lg text-xs font-bold bg-gray-800/80 text-gray-300 hover:bg-gray-700 transition-colors flex items-center gap-1">
                                    <i class="fa-solid fa-pen-to-square"></i> 수정
                                </button>
                                <button onclick="deleteApplication(${app.id})" class="px-3 py-1.5 rounded-lg text-xs font-bold bg-red-500/10 text-red-400 border border-red-500/20 hover:bg-red-500/20 transition-colors flex items-center gap-1">
                                    <i class="fa-solid fa-trash"></i> 삭제
                                </button>
                            </div>
                        </div>
                    </div>
                `;
            }).join('');
        }

        // Admin Modal Controls & Live Charting
        function openAdminModal() {
            const modal = document.getElementById('adminModal');
            modal.classList.remove('opacity-0', 'pointer-events-none');
            modal.classList.add('opacity-100', 'pointer-events-auto');
            updateAdminChart();
        }

        function closeAdminModal() {
            const modal = document.getElementById('adminModal');
            modal.classList.remove('opacity-100', 'pointer-events-auto');
            modal.classList.add('opacity-0', 'pointer-events-none');
        }

        function updateAdminChart() {
            const totalVotes = applications.reduce((sum, item) => sum + item.votes, 0);
            document.getElementById('totalVotesCount').innerText = `${totalVotes}표`;

            // Top items per category
            const studyItems = applications.filter(a => a.category === 'AI 학습부문').sort((a,b) => b.votes - a.votes);
            const campusItems = applications.filter(a => a.category === 'AI 캠퍼스라이프부문').sort((a,b) => b.votes - a.votes);

            document.getElementById('topStudyWork').innerText = studyItems.length > 0 ? `${studyItems[0].title} (${studyItems[0].votes}표)` : '없음';
            document.getElementById('topCampusWork').innerText = campusItems.length > 0 ? `${campusItems[0].title} (${campusItems[0].votes}표)` : '없음';

            // Prepare Chart Data
            const labels = applications.map(app => app.title.length > 12 ? app.title.substring(0, 12) + '...' : app.title);
            const dataVotes = applications.map(app => app.votes);
            const backgroundColors = applications.map(app => app.category === 'AI 학습부문' ? '#8b5cf6' : '#ff2a85');

            const ctx = document.getElementById('voteChart').getContext('2d');

            if(voteChartInstance) {
                voteChartInstance.destroy();
            }

            voteChartInstance = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: labels,
                    datasets: [{
                        label: '득표수',
                        data: dataVotes,
                        backgroundColor: backgroundColors,
                        borderRadius: 8,
                        borderSkipped: false
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { display: false },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `득표수: ${context.raw}표`;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            ticks: { color: '#9ca3af', font: { family: 'Pretendard', size: 11 } },
                            grid: { display: false }
                        },
                        y: {
                            beginAtZero: true,
                            ticks: { color: '#9ca3af', precision: 0 },
                            grid: { color: 'rgba(255, 255, 255, 0.05)' }
                        }
                    }
                }
            });
        }

        // Edit Item
        function editApplication(id) {
            const app = applications.find(item => item.id === id);
            if(!app) return;

            editingId = id;

            // Fill Form
            document.getElementById('applicantName').value = app.applicantName;
            document.getElementById('studentId').value = app.studentId;
            document.getElementById('department').value = app.department;
            document.getElementById('phone').value = app.phone;
            document.getElementById('teamMembers').value = app.teamMembers === '개인 참가' ? '' : app.teamMembers;
            document.getElementById('title').value = app.title;
            document.getElementById('aiTools').value = app.aiTools;
            document.getElementById('description').value = app.description;
            document.getElementById('linkUrl').value = app.linkUrl === '#' ? '' : app.linkUrl;

            if(app.category === 'AI 학습부문') {
                const radio = document.querySelector('input[name="category"][value="AI 학습부문"]');
                if(radio) radio.checked = true;
                updateCategoryStyle('study');
            } else {
                const radio = document.querySelector('input[name="category"][value="AI 캠퍼스라이프부문"]');
                if(radio) radio.checked = true;
                updateCategoryStyle('campus');
            }

            document.getElementById('submitBtnText').innerText = "수정 완료하기";

            // Scroll to Form
            document.getElementById('apply').scrollIntoView({ behavior: 'smooth' });
            showToast("수정 모드로 전환되었습니다. 내용을 변경 후 상단 버튼을 눌러주세요.");
        }

        // Delete Item
        function deleteApplication(id) {
            if(confirm("정말로 이 신청서를 삭제하시겠습니까?")) {
                applications = applications.filter(item => item.id !== id);
                userVotedIds.delete(id);
                renderApplications();
                showToast("신청서가 삭제되었습니다.");
            }
        }

        // Toast Helper
        function showToast(msg) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toastMessage');
            toastMsg.innerText = msg;

            toast.classList.remove('translate-y-20', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');

            setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }

        // HTML Escape for Security
        function escapeHtml(str) {
            if(!str) return '';
            return str.replace(/&/g, "&amp;")
                      .replace(/</g, "&lt;")
                      .replace(/>/g, "&gt;")
                      .replace(/"/g, "&quot;")
                      .replace(/'/g, "&#039;");
        }
    </script>
</body>
</html>
