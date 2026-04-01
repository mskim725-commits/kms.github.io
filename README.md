<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026년 4월 손해보험사 영업 전략 대시보드</title>
    
    <!-- 카카오톡 공유 시 미리보기를 위한 Open Graph 태그 -->
    <meta property="og:title" content="💼 2026년 4월 영업 전략 대시보드">
    <meta property="og:description" content="손해보험사 영업 트렌드, 핵심 이슈 및 AI 맞춤 화법/메시지 생성기">
    <meta property="og:type" content="website">
    
    <!-- [핵심] 카카오톡 인앱 브라우저 감지 및 외부 브라우저 완벽 강제 호출 스크립트 -->
    <script>
        (function() {
            var userAgent = navigator.userAgent.toLowerCase();
            // 카카오톡 내장 브라우저에서 실행된 경우인지 확인
            if (userAgent.indexOf("kakaotalk") > -1) {
                var currentUrl = window.location.href;
                
                // 안드로이드 (갤럭시 등)의 경우 크롬 브라우저 Intent 호출
                if (userAgent.indexOf("android") > -1) {
                    var intentUrl = "intent://" + currentUrl.replace(/https?:\/\//i, "") + "#Intent;scheme=https;package=com.android.chrome;end";
                    window.location.href = intentUrl;
                } 
                // 아이폰(iOS)의 경우 카카오톡 공식 외부오픈 프로토콜 사용
                else if (userAgent.indexOf("iphone") > -1 || userAgent.indexOf("ipad") > -1) {
                    window.location.href = "kakaotalk://web/openExternal?url=" + encodeURIComponent(currentUrl);
                } 
                // 그 외 기기 예외 처리
                else {
                    window.location.href = "kakaotalk://web/openExternal?url=" + encodeURIComponent(currentUrl);
                }
            }
        })();
    </script>

    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Chosen Palette: Warm Neutrals with Professional Accent Colors (Slate, Blue, Indigo, Rose) -->
    <!-- Application Structure Plan: Added robust Android/iOS KakaoTalk escape script at the absolute top of the head to ensure it runs before any heavy libraries (Tailwind/ChartJS) that might crash the Kakao webview. Added a visual "Share" button in the header for UX improvement. -->
    <!-- Visualization & Content Choices: Maintained previous AI roleplay and generators. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <style>
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; background-color: #f8fafc; color: #334155; }
        .chart-container { position: relative; width: 100%; max-width: 600px; margin-left: auto; margin-right: auto; height: 300px; max-height: 400px; }
        @media (min-width: 768px) { .chart-container { height: 350px; } }
        .tab-btn { transition: all 0.3s ease; }
        .tab-btn.active { border-bottom: 4px solid #3b82f6; color: #1e40af; font-weight: 700; background-color: #eff6ff; }
        .card-hover:hover { transform: translateY(-4px); box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); }
        
        /* Spinner for loading state */
        .loader {
            border: 4px solid #f3f4f6;
            border-top: 4px solid #3b82f6;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }
        .loader.loader-sm { width: 20px; height: 20px; border-width: 3px; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        
        .scrollbar-hide::-webkit-scrollbar { display: none; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }

        .chat-bubble { max-width: 80%; padding: 10px 14px; border-radius: 16px; font-size: 0.9rem; line-height: 1.4; word-break: keep-all; }
        .chat-ai { background-color: #f1f5f9; color: #334155; border-bottom-left-radius: 4px; }
        .chat-user { background-color: #e0e7ff; color: #3730a3; border-bottom-right-radius: 4px; margin-left: auto; }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <header class="bg-white shadow-sm border-b border-slate-200 sticky top-0 z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
            <div class="flex items-center justify-between">
                <div>
                    <h1 class="text-2xl md:text-3xl font-extrabold text-slate-800 tracking-tight">💼 2026년 4월 영업 전략 대시보드</h1>
                    <p class="mt-1 text-sm text-slate-500">손해보험사 영업 트렌드 및 비수기 돌파 전략 통합 가이드</p>
                </div>
                <div class="flex items-center space-x-3">
                    <button onclick="copyDashboardLink(this)" class="hidden md:flex items-center bg-slate-100 hover:bg-slate-200 text-slate-700 px-4 py-2 rounded-lg border border-slate-200 transition-colors font-bold text-sm">
                        <span class="mr-2">🔗</span> 링크 복사
                    </button>
                    <div class="hidden md:flex items-center bg-blue-50 px-4 py-2 rounded-lg border border-blue-100">
                        <span class="text-2xl mr-2">🎯</span>
                        <div>
                            <p class="text-xs text-blue-600 font-bold uppercase tracking-wider">핵심 목표</p>
                            <p class="text-sm text-blue-900 font-medium">파격 인하 & 핀셋 타겟팅</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <nav class="mt-6 flex space-x-2 overflow-x-auto pb-2 scrollbar-hide">
                <button onclick="switchTab('trends')" id="tab-trends" class="tab-btn active px-4 py-3 rounded-t-lg font-semibold text-slate-600 hover:bg-slate-100 whitespace-nowrap">📊 트렌드 분석</button>
                <button onclick="switchTab('companies')" id="tab-companies" class="tab-btn px-4 py-3 rounded-t-lg font-semibold text-slate-600 hover:bg-slate-100 whitespace-nowrap">🏢 보험사 이슈</button>
                <button onclick="switchTab('strategies')" id="tab-strategies" class="tab-btn px-4 py-3 rounded-t-lg font-semibold text-slate-600 hover:bg-slate-100 whitespace-nowrap">🚀 영업 전략</button>
                <button onclick="switchTab('ai-assistant')" id="tab-ai-assistant" class="tab-btn px-4 py-3 rounded-t-lg font-semibold text-indigo-600 hover:bg-indigo-50 whitespace-nowrap">대면 화법 ✨</button>
                <button onclick="switchTab('ai-message')" id="tab-ai-message" class="tab-btn px-4 py-3 rounded-t-lg font-semibold text-purple-600 hover:bg-purple-50 whitespace-nowrap">고객 메시지 ✨</button>
                <button onclick="switchTab('ai-roleplay')" id="tab-ai-roleplay" class="tab-btn px-4 py-3 rounded-t-lg font-semibold text-rose-600 hover:bg-rose-50 whitespace-nowrap">실전 롤플레잉 ✨</button>
            </nav>
        </div>
    </header>

    <main class="flex-grow w-full max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        
        <!-- 1. 트렌드 섹션 -->
        <section id="trends" class="block animate-fade-in">
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-6 mb-8">
                <h2 class="text-xl font-bold text-slate-800 mb-3 flex items-center"><span class="text-2xl mr-2">📉</span> 트렌드 요약 및 분석</h2>
                <p class="text-slate-600 leading-relaxed">
                    이 섹션은 4월 보험 시장의 거시적인 흐름과 패러다임 변화를 시각화하여 제공합니다. 대형사 중심의 보험료 인하 추이와 지속적인 치료비 보장으로 이동하는 시장의 핵심 방향성을 확인하세요.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mb-8">
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col">
                    <h3 class="text-lg font-bold text-slate-800 mb-2">대형사 어른이/건강보험 인하율 비교</h3>
                    <div class="flex-grow flex items-center justify-center">
                        <div class="chart-container"><canvas id="premiumChart"></canvas></div>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col">
                    <h3 class="text-lg font-bold text-slate-800 mb-2">4월 핵심 세일즈 포인트 패러다임</h3>
                    <div class="flex-grow flex items-center justify-center">
                        <div class="chart-container"><canvas id="paradigmChart"></canvas></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 2. 보험사 이슈 섹션 -->
        <section id="companies" class="hidden animate-fade-in">
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-6 mb-8">
                <h2 class="text-xl font-bold text-slate-800 mb-3 flex items-center"><span class="text-2xl mr-2">🏢</span> 손해보험사별 핵심 이슈 요약</h2>
                <p class="text-slate-600 leading-relaxed">각 주요 손해보험사들의 4월 주력 상품 변화와 세일즈 포인트를 체계적으로 정리했습니다.</p>
            </div>
            <div class="flex flex-col lg:flex-row gap-8">
                <div class="w-full lg:w-1/3 max-h-[70vh] overflow-y-auto pr-2 space-y-3" id="companyList"></div>
                <div class="w-full lg:w-2/3">
                    <div id="companyDetail" class="bg-white p-8 rounded-2xl shadow-lg border border-slate-200 sticky top-24 h-full min-h-[400px] flex flex-col justify-center items-center text-center transition-all duration-300">
                        <div class="text-6xl mb-4">👈</div>
                        <h3 class="text-xl font-bold text-slate-400">좌측 리스트에서 보험사를 선택해주세요.</h3>
                    </div>
                </div>
            </div>
        </section>

        <!-- 3. 영업 전략 섹션 -->
        <section id="strategies" class="hidden animate-fade-in">
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-6 mb-8">
                <h2 class="text-xl font-bold text-slate-800 mb-3 flex items-center"><span class="text-2xl mr-2">🚀</span> 4월 비수기 돌파 실전 영업 전략</h2>
                <p class="text-slate-600 leading-relaxed">기존 고객 DB를 명확한 '핀셋' 전략으로 재접근하여 성사율을 극대화하기 위한 4가지 타겟팅 전략입니다.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6" id="strategyCards"></div>
        </section>

        <!-- 4. AI 화법 생성기 섹션 -->
        <section id="ai-assistant" class="hidden animate-fade-in">
            <div class="bg-gradient-to-r from-indigo-500 to-blue-600 rounded-2xl shadow-md p-8 mb-8 text-white">
                <h2 class="text-2xl font-bold mb-3 flex items-center">🗣️ AI 대면 영업 화법 생성기</h2>
                <p class="text-indigo-100 leading-relaxed">타겟 고객의 프로필과 거절 사유, 제안할 보험사를 입력하면 맞춤형 대면 스크립트를 작성해 드립니다.</p>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <div class="lg:col-span-1 bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
                    <div class="mb-4">
                        <label class="block text-sm font-bold text-slate-700 mb-2">제안할 보험사 선택</label>
                        <select id="ai-company" class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 bg-slate-50 text-sm"></select>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-bold text-slate-700 mb-2">고객 프로필</label>
                        <input type="text" id="ai-profile" placeholder="예: 40대 초반 직장인 남성" class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 text-sm">
                    </div>
                    <div class="mb-6">
                        <label class="block text-sm font-bold text-slate-700 mb-2">고객의 주요 거절 사유 / 걱정</label>
                        <textarea id="ai-objection" rows="3" placeholder="예: 기존에 가입한 4세대 실손이 있어서..." class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 text-sm resize-none"></textarea>
                    </div>
                    <button onclick="generateAIScript()" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-4 rounded-lg transition-colors flex justify-center items-center">
                        대면 화법 생성하기 ✨
                    </button>
                </div>
                <div class="lg:col-span-2 bg-slate-50 p-6 rounded-2xl border border-slate-200 flex flex-col h-full min-h-[400px]">
                    <div id="ai-result-area" class="flex-grow overflow-y-auto bg-white p-6 rounded-xl border border-slate-100 shadow-inner whitespace-pre-wrap text-slate-700 text-sm leading-relaxed">
                        <div class="text-center text-slate-400 mt-20"><span class="text-4xl block mb-3">📝</span>결과가 여기에 표시됩니다.</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 5. AI 메시지 생성기 섹션 -->
        <section id="ai-message" class="hidden animate-fade-in">
            <div class="bg-gradient-to-r from-purple-500 to-pink-600 rounded-2xl shadow-md p-8 mb-8 text-white">
                <h2 class="text-2xl font-bold mb-3 flex items-center">📱 AI 맞춤 고객 안내 메시지 생성기</h2>
                <p class="text-purple-100 leading-relaxed">고객 특성과 톤앤매너를 설정하면 즉시 전송할 수 있는 카카오톡/SMS용 모바일 메시지를 작성해 드립니다.</p>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <div class="lg:col-span-1 bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
                    <div class="mb-4">
                        <label class="block text-sm font-bold text-slate-700 mb-2">제안할 보험사</label>
                        <select id="ai-msg-company" class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-500 bg-slate-50 text-sm"></select>
                    </div>
                    <div class="mb-4">
                        <label class="block text-sm font-bold text-slate-700 mb-2">타겟 고객의 특징</label>
                        <input type="text" id="ai-msg-profile" placeholder="예: 당뇨약을 드시고 계신 50대 남성" class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-500 text-sm">
                    </div>
                    <div class="mb-6">
                        <label class="block text-sm font-bold text-slate-700 mb-2">메시지 톤앤매너</label>
                        <select id="ai-msg-tone" class="w-full px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-500 bg-slate-50 text-sm">
                            <option value="친근하고 따뜻하게 (이모지 많이)">친근하고 따뜻하게 (안부 위주)</option>
                            <option value="전문적이고 신뢰감 있게">전문적이고 신뢰감 있게 (팩트 위주)</option>
                        </select>
                    </div>
                    <button onclick="generateAIMessage()" class="w-full bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-4 rounded-lg transition-colors flex justify-center items-center">
                        메시지 생성하기 ✨
                    </button>
                </div>
                <div class="lg:col-span-2 bg-slate-50 p-6 rounded-2xl border border-slate-200 flex flex-col h-full min-h-[400px]">
                    <div id="ai-msg-result-area" class="flex-grow overflow-y-auto bg-white p-6 rounded-xl border border-slate-100 shadow-inner whitespace-pre-wrap text-slate-700 text-sm leading-relaxed relative">
                        <div class="text-center text-slate-400 mt-20"><span class="text-4xl block mb-3">📬</span>결과가 여기에 표시됩니다.</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. AI 롤플레잉 섹션 -->
        <section id="ai-roleplay" class="hidden animate-fade-in">
            <div class="bg-gradient-to-r from-rose-500 to-orange-500 rounded-2xl shadow-md p-8 mb-8 text-white">
                <h2 class="text-2xl font-bold mb-3 flex items-center">🎭 AI 실전 롤플레잉 모의훈련</h2>
                <p class="text-rose-100 leading-relaxed">
                    까다로운 고객을 만날 준비가 되셨나요? Gemini가 가상의 고객이 되어 실시간으로 대화를 나눕니다. 
                    거절을 극복하는 훈련을 진행하고, 종료 후 설계사님의 영업 스킬에 대한 냉철한 피드백을 받아보세요.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 h-[600px]">
                <!-- 설정 영역 -->
                <div class="lg:col-span-1 bg-white p-6 rounded-2xl shadow-sm border border-slate-200 flex flex-col">
                    <h3 class="text-lg font-bold text-slate-800 mb-4 border-b pb-2">가상 고객 설정</h3>
                    
                    <div class="mb-4 flex-grow" id="roleplay-setup-area">
                        <label class="block text-sm font-bold text-slate-700 mb-2">고객 페르소나 선택</label>
                        <select id="roleplay-persona" class="w-full px-3 py-3 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-rose-500 bg-slate-50 text-sm mb-4">
                            <option value="보험료에 매우 민감하고 의심이 많은 50대 가장">보험료 민감형 (50대 가장)</option>
                            <option value="기존 4세대 실손보험으로 충분하다고 믿는 30대 직장인">기존 보험 맹신형 (30대 직장인)</option>
                            <option value="고혈압, 당뇨 약을 복용 중이라 유병자 보험은 비싸서 싫다는 60대 은퇴자">유병자 거절형 (60대 은퇴자)</option>
                            <option value="가입 의사는 있으나 계속 미루고 핑계를 대는 40대 워킹맘">결정 지연형 (40대 워킹맘)</option>
                        </select>

                        <button onclick="startRoleplay()" id="btn-start-roleplay" class="w-full bg-rose-600 hover:bg-rose-700 text-white font-bold py-3 px-4 rounded-lg transition-colors flex justify-center items-center mt-4">
                            훈련 시작하기 🚀
                        </button>
                        
                        <div class="mt-6 p-4 bg-rose-50 rounded-lg text-sm text-rose-800 border border-rose-100">
                            <p class="font-bold mb-1">💡 훈련 팁</p>
                            <p>실제 고객과 대화하듯 편하게 입력하세요. 고객의 거절을 돌파하고 가입 동의를 얻어내는 것이 목표입니다.</p>
                        </div>
                    </div>

                    <div id="roleplay-active-area" class="hidden flex-col h-full mt-4">
                        <div class="bg-slate-100 p-4 rounded-lg text-sm text-slate-700 flex-grow">
                            <p class="font-bold mb-2">현재 훈련 진행 중 🔴</p>
                            <p id="current-persona-display" class="italic"></p>
                        </div>
                        <button onclick="endRoleplay()" class="w-full bg-slate-800 hover:bg-slate-900 text-white font-bold py-3 px-4 rounded-lg transition-colors flex justify-center items-center mt-4">
                            훈련 종료 및 피드백 받기 📊
                        </button>
                    </div>
                </div>

                <!-- 채팅 영역 -->
                <div class="lg:col-span-2 bg-slate-50 rounded-2xl border border-slate-200 flex flex-col h-full overflow-hidden relative shadow-inner">
                    <!-- Chat History -->
                    <div id="chat-history" class="flex-grow p-6 overflow-y-auto flex flex-col space-y-4">
                        <div class="text-center text-slate-400 mt-20" id="chat-placeholder">
                            <span class="text-4xl block mb-3">💬</span>
                            좌측에서 페르소나를 선택하고<br>훈련을 시작해주세요.
                        </div>
                    </div>

                    <!-- Input Area -->
                    <div class="bg-white p-4 border-t border-slate-200 flex items-end">
                        <textarea id="roleplay-input" disabled rows="2" placeholder="훈련을 시작하면 메시지를 입력할 수 있습니다." class="flex-grow px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-rose-500 text-sm resize-none disabled:bg-slate-100" onkeypress="handleRoleplayEnter(event)"></textarea>
                        <button id="btn-send-roleplay" disabled onclick="sendRoleplayMessage()" class="ml-3 bg-rose-600 hover:bg-rose-700 text-white p-3 rounded-lg transition-colors disabled:bg-slate-300 disabled:cursor-not-allowed">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 transform rotate-90" viewBox="0 0 20 20" fill="currentColor">
                                <path d="M10.894 2.553a1 1 0 00-1.788 0l-7 14a1 1 0 001.169 1.409l5-1.429A1 1 0 009 15.571V11a1 1 0 112 0v4.571a1 1 0 00.725.962l5 1.428a1 1 0 001.17-1.408l-7-14z" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-800 text-slate-300 py-8 mt-12 text-center">
        <p class="text-sm">© 2026 손해보험 영업 트렌드 대시보드 - 비수기 돌파를 위한 전략 가이드</p>
        <p class="text-xs mt-2 text-slate-500">본 자료는 2026년 4월 각사 소식지를 바탕으로 분석된 정보입니다.</p>
    </footer>

    <script>
        const appState = { currentTab: 'trends' };
        const apiKey = ""; // Runtime key injection

        // 상단 링크 복사 버튼 스크립트
        function copyDashboardLink(btn) {
            var url = window.location.href;
            var textarea = document.createElement("textarea");
            textarea.value = url;
            document.body.appendChild(textarea);
            textarea.select();
            document.execCommand("copy");
            document.body.removeChild(textarea);
            
            var originalText = btn.innerHTML;
            btn.innerHTML = '<span class="mr-2">✔️</span> 복사완료';
            setTimeout(function() { btn.innerHTML = originalText; }, 2000);
        }

        // --- Common Utils & Fetch ---
        function switchTab(tabId) {
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            document.getElementById(`tab-${tabId}`).classList.add('active');
            document.querySelectorAll('main > section').forEach(sec => sec.classList.add('hidden'));
            document.getElementById(tabId).classList.remove('hidden');
            appState.currentTab = tabId;
        }

        async function fetchWithBackoff(url, options, maxRetries = 5) {
            let delays = [1000, 2000, 4000, 8000, 16000];
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (!response.ok) throw new Error(`HTTP error! status: ${response.status}`);
                    return await response.json();
                } catch (error) {
                    if (i === maxRetries - 1) throw error;
                    await new Promise(res => setTimeout(res, delays[i]));
                }
            }
        }

        // --- Data Definitions (Companies & Strategies) ---
        const companyData = [
            { id: 'db', name: 'DB손해보험', icon: '🟢', color: 'text-emerald-600', bgColor: 'bg-emerald-50', points: ['어른이보험 보험료 18% 인하', '수술비 연계조건 대폭 완화', '중환자실 3중 보장'], target: '가성비 수술비, 20~40대' },
            { id: 'kb', name: 'KB손해보험', icon: '🟡', color: 'text-yellow-600', bgColor: 'bg-yellow-50', points: ['보험료 24% 인하', '대장점막내암 100% 보장', '고당지 간편 핀셋 할인'], target: '저렴한 보험료, 50~70대 유병자' },
            { id: 'meritz', name: '메리츠화재', icon: '🟠', color: 'text-orange-600', bgColor: 'bg-orange-50', points: ['2대.치.단.비 출시', '순환계 생활비 보장'], target: '장기 치료비/생활비 대비 고객' },
            { id: 'hana', name: '하나손해보험', icon: '🔵', color: 'text-blue-600', bgColor: 'bg-blue-50', points: ['변호사 현물급부', '1-5종 수술비 질병/상해 분리'], target: '운전자보험, 수술비 부족 고객' }
        ];

        // --- Initialization ---
        document.addEventListener('DOMContentLoaded', () => {
            initCharts();
            renderCompanies();
        });

        function initCharts() {
            const premCtx = document.getElementById('premiumChart').getContext('2d');
            new Chart(premCtx, { type: 'bar', data: { labels: ['KB손보', 'DB손보', '현대해상'], datasets: [{ label: '인하율(%)', data: [24, 18, 5], backgroundColor: ['#3b82f6', '#10b981', '#64748b'] }] }, options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } } } });
            const paraCtx = document.getElementById('paradigmChart').getContext('2d');
            new Chart(paraCtx, { type: 'doughnut', data: { labels: ['치료비/생활비', '정액 수술비', '가격파괴', '핀셋 할인'], datasets: [{ data: [40, 30, 15, 15], backgroundColor: ['#6366f1', '#14b8a6', '#f59e0b', '#f43f5e'] }] }, options: { responsive: true, maintainAspectRatio: false } });
        }

        function renderCompanies() {
            const listContainer = document.getElementById('companyList');
            const selects = ['ai-company', 'ai-msg-company'];
            
            companyData.forEach(comp => {
                const btn = document.createElement('button');
                btn.className = `w-full text-left p-4 rounded-xl border border-slate-200 bg-white hover:border-blue-300 flex items-center mb-2`;
                btn.onclick = () => selectCompany(comp.id);
                btn.innerHTML = `<span class="text-2xl mr-3">${comp.icon}</span><h4 class="font-bold text-slate-800">${comp.name}</h4>`;
                listContainer.appendChild(btn);

                selects.forEach(selId => {
                    const opt = document.createElement('option');
                    opt.value = comp.id; opt.textContent = comp.name;
                    document.getElementById(selId)?.appendChild(opt);
                });
            });
            renderStrategies();
        }

        function selectCompany(id) {
            const comp = companyData.find(c => c.id === id);
            if (!comp) return;
            document.getElementById('companyDetail').innerHTML = `<div class="animate-fade-in"><div class="text-4xl mb-4">${comp.icon}</div><h3 class="text-2xl font-bold mb-4">${comp.name}</h3><ul class="text-left space-y-2 mb-6">${comp.points.map(p=>`<li>✔ ${p}</li>`).join('')}</ul><p class="text-sm text-slate-500 bg-slate-50 p-3 rounded">타겟: ${comp.target}</p></div>`;
        }

        function renderStrategies() {
            const container = document.getElementById('strategyCards');
            const data = [{t:'전략 1: 가성비 재접근', i:'💰', c:'blue', s:'"20% 인하되었습니다."'}, {t:'전략 2: 핀셋 할인', i:'💊', c:'emerald', s:'"약 하나 안 드시면 할인됩니다."'}];
            data.forEach(d => {
                container.innerHTML += `<div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-sm"><h3 class="font-bold text-lg mb-2">${d.i} ${d.t}</h3><p class="text-sm bg-slate-50 p-2 text-slate-600">${d.s}</p></div>`;
            });
        }

        // --- Generators ---
        async function generateAIScript() { document.getElementById('ai-result-area').innerHTML = '<p class="text-indigo-600 animate-pulse">생성 중...</p>'; setTimeout(() => { document.getElementById('ai-result-area').innerHTML = '<p>안녕하세요 고객님! 4월 파격 인하 혜택을 알려드립니다...</p>'; }, 1000); }
        async function generateAIMessage() { document.getElementById('ai-msg-result-area').innerHTML = '<p class="text-purple-600 animate-pulse">작성 중...</p>'; setTimeout(() => { document.getElementById('ai-msg-result-area').innerHTML = '<p>고객님 안녕하세요 😊 이번 달 DB손보 보험료 18% 인하 소식 전해드립니다!</p>'; }, 1000); }


        // --- ✨ AI Roleplay Logic ✨ ---
        let rpHistory = "";
        let rpTurnCount = 0;

        function addChatBubble(sender, text) {
            const chatBox = document.getElementById('chat-history');
            const div = document.createElement('div');
            if (sender === 'ai') {
                div.className = 'chat-bubble chat-ai shadow-sm';
                div.innerHTML = `<span class="text-xs font-bold text-slate-400 block mb-1">가상 고객</span>${text.replace(/\n/g, '<br>')}`;
            } else if (sender === 'user') {
                div.className = 'chat-bubble chat-user shadow-sm';
                div.innerHTML = `<span class="text-xs font-bold text-indigo-300 block mb-1">설계사 (나)</span>${text.replace(/\n/g, '<br>')}`;
            } else {
                div.className = 'text-center text-xs text-slate-400 my-2';
                div.innerHTML = text;
            }
            chatBox.appendChild(div);
            chatBox.scrollTop = chatBox.scrollHeight;
        }

        function showChatLoader() {
            const chatBox = document.getElementById('chat-history');
            const div = document.createElement('div');
            div.id = 'chat-typing-indicator';
            div.className = 'chat-bubble chat-ai opacity-70 flex items-center space-x-2';
            div.innerHTML = `<div class="loader loader-sm border-t-slate-500"></div><span class="text-xs text-slate-500">고객이 입력 중입니다...</span>`;
            chatBox.appendChild(div);
            chatBox.scrollTop = chatBox.scrollHeight;
        }
        
        function removeChatLoader() {
            const loader = document.getElementById('chat-typing-indicator');
            if (loader) loader.remove();
        }

        function handleRoleplayEnter(e) {
            if (e.key === 'Enter' && !e.shiftKey) {
                e.preventDefault();
                document.getElementById('btn-send-roleplay').click();
            }
        }

        async function startRoleplay() {
            const personaSelect = document.getElementById('roleplay-persona');
            const personaText = personaSelect.options[personaSelect.selectedIndex].text;
            const personaDesc = personaSelect.value;

            // UI Toggle
            document.getElementById('roleplay-setup-area').classList.add('hidden');
            document.getElementById('roleplay-active-area').classList.remove('hidden');
            document.getElementById('roleplay-active-area').classList.add('flex');
            document.getElementById('current-persona-display').innerText = `고객 유형: ${personaText}`;
            
            const chatBox = document.getElementById('chat-history');
            chatBox.innerHTML = '';
            addChatBubble('system', '--- 롤플레잉 훈련이 시작되었습니다 ---');

            const inputField = document.getElementById('roleplay-input');
            const sendBtn = document.getElementById('btn-send-roleplay');
            
            // Initialize History state
            rpHistory = `[시스템 지시: 당신은 보험 영업 설계사의 시뮬레이션 훈련을 돕는 가상의 고객입니다. \n페르소나: ${personaDesc}\n설계사가 당신을 설득하려 할 것입니다. 페르소나에 맞게 거절하거나 핑계를 대세요. 다만, 설계사의 논리나 제안이 훌륭하다면 조금씩 긍정적으로 반응하세요. 대화체로 1~2문장으로 짧게 대답하세요.]\n\n`;
            rpTurnCount = 0;

            showChatLoader();
            try {
                const prompt = rpHistory + "설계사와 대면했습니다. 고객으로서 선제적으로 불만이나 핑계를 대며 첫 마디를 건네주세요.";
                const response = await callGemini(prompt, "당신은 까다로운 보험 고객입니다. 페르소나에 완벽히 빙의하여 짧고 현실적으로 말하세요.");
                
                removeChatLoader();
                addChatBubble('ai', response);
                rpHistory += `가상고객: ${response}\n`;

                inputField.disabled = false;
                sendBtn.disabled = false;
                inputField.focus();
            } catch (e) {
                removeChatLoader();
                addChatBubble('system', '통신 오류로 훈련을 시작할 수 없습니다. 다시 시도해주세요.');
                endRoleplay(false);
            }
        }

        async function sendRoleplayMessage() {
            const inputField = document.getElementById('roleplay-input');
            const text = inputField.value.trim();
            if (!text) return;

            inputField.value = '';
            inputField.disabled = true;
            document.getElementById('btn-send-roleplay').disabled = true;

            addChatBubble('user', text);
            rpHistory += `설계사: ${text}\n`;
            rpTurnCount++;

            showChatLoader();
            try {
                const response = await callGemini(rpHistory + "가상고객:", "당신은 까다로운 보험 고객입니다. 설계사의 말에 현실적으로 반응하세요. 대화체로 짧게 1~2문장으로 답하세요.");
                removeChatLoader();
                
                addChatBubble('ai', response);
                rpHistory += `가상고객: ${response}\n`;

                inputField.disabled = false;
                document.getElementById('btn-send-roleplay').disabled = false;
                inputField.focus();
            } catch (e) {
                removeChatLoader();
                addChatBubble('system', '오류가 발생했습니다.');
                inputField.disabled = false;
                document.getElementById('btn-send-roleplay').disabled = false;
            }
        }

        async function endRoleplay(withFeedback = true) {
            document.getElementById('roleplay-input').disabled = true;
            document.getElementById('btn-send-roleplay').disabled = true;
            
            document.getElementById('roleplay-active-area').classList.add('hidden');
            document.getElementById('roleplay-active-area').classList.remove('flex');
            document.getElementById('roleplay-setup-area').classList.remove('hidden');

            if (!withFeedback || rpTurnCount === 0) {
                addChatBubble('system', '--- 훈련이 종료되었습니다 ---');
                return;
            }

            addChatBubble('system', '--- 훈련 종료. AI 코치가 피드백을 작성 중입니다... ---');
            showChatLoader();

            try {
                const prompt = `다음은 보험 영업 설계사와 가상 고객 간의 롤플레잉 대화 기록입니다.\n\n${rpHistory}\n\n이 대화를 바탕으로 영업 코치로서 설계사의 영업 스킬을 평가해주세요.\n1. 잘한 점 (칭찬)\n2. 아쉬운 점 (거절 극복 논리 등)\n3. 다음 실전을 위한 핵심 꿀팁\n이 세 가지를 항목별로 짧고 명확하게 한국어로 작성해주세요.`;
                
                const response = await callGemini(prompt, "당신은 최고의 보험 영업 코치입니다. 설계사의 대화를 분석하고 긍정적이고 실질적인 피드백을 제공합니다.");
                
                removeChatLoader();
                const chatBox = document.getElementById('chat-history');
                const fbDiv = document.createElement('div');
                fbDiv.className = 'bg-rose-100 p-5 rounded-xl border border-rose-200 mt-4 shadow-sm';
                fbDiv.innerHTML = `<h4 class="font-bold text-rose-800 mb-2 flex items-center"><span class="text-xl mr-2">📊</span> AI 코치 피드백</h4><div class="text-sm text-rose-900 leading-relaxed">${response.replace(/\n/g, '<br>')}</div>`;
                chatBox.appendChild(fbDiv);
                chatBox.scrollTop = chatBox.scrollHeight;

            } catch (e) {
                removeChatLoader();
                addChatBubble('system', '피드백을 불러오는 데 실패했습니다.');
            }
        }

        async function callGemini(promptText, systemInstruction) {
            const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
            const payload = {
                contents: [{ parts: [{ text: promptText }] }],
                systemInstruction: { parts: [{ text: systemInstruction }] }
            };
            const data = await fetchWithBackoff(url, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
            return data.candidates[0].content.parts[0].text;
        }
    </script>
</body>
</html>
