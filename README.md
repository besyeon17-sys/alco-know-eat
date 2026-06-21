# alco-know-eat
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>알코알먹 — 맞춤형 음주 절제 및 멘탈케어 솔루션</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pretendard:wght@300;400;500;600;700;800&display=swap');
        body {
            font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, Roboto, sans-serif;
        }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex flex-col justify-between">

    <!-- Header Section -->
    <header class="border-b border-slate-800 bg-slate-950/80 backdrop-blur sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-amber-500 to-rose-500 flex items-center justify-center shadow-lg shadow-rose-500/20">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z" />
                    </svg>
                </div>
                <div>
                    <h1 class="text-lg font-bold tracking-tight bg-gradient-to-r from-amber-400 to-rose-400 bg-clip-text text-transparent">알코올 알고먹자 (알코알먹)</h1>
                    <p class="text-xs text-slate-400 font-medium">인지적 비용 제로 기반 개인 맞춤형 음주 모니터링</p>
                </div>
            </div>
            <div class="hidden sm:flex items-center space-x-2 text-xs bg-slate-800/80 px-3 py-1.5 rounded-full border border-slate-700/50">
                <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
                <span class="text-slate-300 font-semibold">임상 알고리즘 엔진 v1.2</span>
            </div>
        </div>
    </header>

    <!-- Main Container -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 flex-grow w-full grid grid-cols-1 lg:grid-cols-12 gap-8">
        
        <!-- Left Panel: Input Forms (lg:col-span-5) -->
        <section class="lg:col-span-5 space-y-6">
            
            <!-- 1. 신체 데이터 및 유전 정보 -->
            <div class="bg-slate-950/40 p-6 rounded-2xl border border-slate-800/80 backdrop-blur-md">
                <div class="flex items-center space-x-2.5 mb-5 pb-3 border-b border-slate-800/60">
                    <span class="text-xl">🧬</span>
                    <h2 class="text-base font-semibold text-slate-100">신체 프로필 및 유전학적 대사 속성</h2>
                </div>
                
                <div class="space-y-4">
                    <!-- 성별 및 연령 -->
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">생물학적 성별</label>
                            <div class="grid grid-cols-2 gap-2">
                                <button type="button" id="btnGenderM" class="py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-amber-500/10 border-amber-500/50 text-amber-400 shadow-md shadow-amber-500/5" onclick="setGender('M')">남성</button>
                                <button type="button" id="btnGenderF" class="py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-slate-900 border-slate-800 text-slate-400 hover:border-slate-700" onclick="setGender('F')">여성</button>
                            </div>
                        </div>
                        <div>
                            <label for="inputAge" class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">연령 (만 나이)</label>
                            <input type="number" id="inputAge" value="20" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500/50 focus:ring-1 focus:ring-amber-500/50 transition-all">
                        </div>
                    </div>

                    <!-- 신장 및 체중 -->
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label for="inputHeight" class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">신장 (cm)</label>
                            <input type="number" id="inputHeight" value="178" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500/50 focus:ring-1 focus:ring-amber-500/50 transition-all">
                        </div>
                        <div>
                            <label for="inputWeight" class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">체중 (kg)</label>
                            <input type="number" id="inputWeight" value="72" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500/50 focus:ring-1 focus:ring-amber-500/50 transition-all">
                        </div>
                    </div>

                    <!-- 안면 홍조 반응 (ALDH2 결핍 여부) -->
                    <div class="bg-slate-900/60 p-4 rounded-xl border border-slate-800/80 mt-2">
                        <div class="flex items-start justify-between">
                            <div class="pr-4">
                                <h3 class="text-sm font-bold text-slate-200">안면 홍조 반응 (ALDH2 유전자 변이)</h3>
                                <p class="text-xs text-slate-400 mt-1 leading-relaxed">술을 한두 잔만 마셔도 얼굴이 쉽게 붉어지거나 심박수가 급격히 상승합니까?</p>
                            </div>
                            <label class="relative inline-flex items-center cursor-pointer mt-1">
                                <input type="checkbox" id="checkFlusher" checked class="sr-only peer" onchange="calculateAll()">
                                <div class="w-11 h-6 bg-slate-800 rounded-full peer peer-focus:ring-2 peer-focus:ring-rose-500/30 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[2px] after:bg-slate-400 after:border-slate-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-gradient-to-r peer-checked:from-rose-500 peer-checked:to-amber-500 peer-checked:after:bg-white"></div>
                            </label>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 2. 심리적 인지 성향 설정 -->
            <div class="bg-slate-950/40 p-6 rounded-2xl border border-slate-800/80 backdrop-blur-md">
                <div class="flex items-center space-x-2.5 mb-5 pb-3 border-b border-slate-800/60">
                    <span class="text-xl">🧠</span>
                    <h2 class="text-base font-semibold text-slate-100">심리적 특성 및 인지 성향</h2>
                </div>

                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <label for="selectMBTI" class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">성격 유형 (MBTI)</label>
                        <select id="selectMBTI" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-3 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500/50 transition-all" onchange="calculateAll()">
                            <option value="INTJ" selected>INTJ (과학적 분석가)</option>
                            <option value="INTP">INTP (학구적 탐구자)</option>
                            <option value="INFJ">INFJ (통찰적인 멘토)</option>
                            <option value="INFP">INFP (감성적인 낭만파)</option>
                            <option value="ISTJ">ISTJ (신뢰성 있는 관리인)</option>
                            <option value="ISFJ">ISFJ (헌신적인 조력자)</option>
                            <option value="ISTP">ISTP (냉철한 해결사)</option>
                            <option value="ISFP">ISFP (조화로운 예술가)</option>
                            <option value="ENTJ">ENTJ (전략적 리더)</option>
                            <option value="ENTP">ENTP (재기발랄한 혁신가)</option>
                            <option value="ENFJ">ENFJ (따뜻한 안내자)</option>
                            <option value="ENFP">ENFP (열정적 중재자)</option>
                            <option value="ESTJ">ESTJ (체계적 정치가)</option>
                            <option value="ESFJ">ESFJ (다정다감한 외교관)</option>
                            <option value="ESTP">ESTP (모험을 즐기는 자)</option>
                            <option value="ESFP">ESFP (활기찬 에너지원)</option>
                        </select>
                    </div>
                    <div>
                        <label for="selectBlackout" class="block text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">과거 블랙아웃/구토 경험</label>
                        <select id="selectBlackout" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-3 py-2.5 text-sm text-slate-100 focus:outline-none focus:border-amber-500/50 transition-all" onchange="calculateAll()">
                            <option value="0" selected>전혀 없음 (0점)</option>
                            <option value="1">가끔 있음 (감점 0.5잔)</option>
                            <option value="2">자주 경험함 (감점 1.0잔)</option>
                        </select>
                    </div>
                </div>
            </div>

            <!-- 3. 실시간 음주 기록 수집 -->
            <div class="bg-slate-950/40 p-6 rounded-2xl border border-slate-800/80 backdrop-blur-md">
                <div class="flex items-center space-x-2.5 mb-5 pb-3 border-b border-slate-800/60">
                    <span class="text-xl">🍷</span>
                    <h2 class="text-base font-semibold text-slate-100">현재 세션 음주량 수집 기록</h2>
                </div>

                <div class="space-y-4">
                    <!-- 소주, 맥주, 와인 조절 -->
                    <div class="grid grid-cols-3 gap-3">
                        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-850 text-center">
                            <span class="text-xs font-semibold text-emerald-400 block mb-1">소주 (360ml 병)</span>
                            <div class="flex items-center justify-between mt-2">
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('soju', -0.5)">-</button>
                                <span id="valSoju" class="text-sm font-bold text-slate-200">0.0</span>
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('soju', 0.5)">+</button>
                            </div>
                        </div>
                        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-850 text-center">
                            <span class="text-xs font-semibold text-amber-400 block mb-1">맥주 (350ml 캔)</span>
                            <div class="flex items-center justify-between mt-2">
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('beer', -1)">-</button>
                                <span id="valBeer" class="text-sm font-bold text-slate-200">0</span>
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('beer', 1)">+</button>
                            </div>
                        </div>
                        <div class="bg-slate-900/80 p-3 rounded-xl border border-slate-850 text-center">
                            <span class="text-xs font-semibold text-rose-400 block mb-1">와인 (150ml 잔)</span>
                            <div class="flex items-center justify-between mt-2">
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('wine', -1)">-</button>
                                <span id="valWine" class="text-sm font-bold text-slate-200">0</span>
                                <button type="button" class="w-7 h-7 bg-slate-800 hover:bg-slate-700 text-slate-100 font-bold rounded-lg flex items-center justify-center transition-colors" onclick="adjustDrinks('wine', 1)">+</button>
                            </div>
                        </div>
                    </div>

                    <!-- 경과 시간 -->
                    <div>
                        <div class="flex justify-between items-center mb-1">
                            <label for="rangeHours" class="block text-xs font-bold text-slate-400 uppercase tracking-wider">음주 시작 후 경과 시간: <span id="lblHours" class="text-amber-400 font-extrabold text-sm ml-1">1</span>시간</label>
                        </div>
                        <input type="range" id="rangeHours" min="0.5" max="12" step="0.5" value="1" class="w-full h-1.5 bg-slate-800 rounded-lg appearance-none cursor-pointer accent-amber-500" oninput="updateHoursLabel(this.value)">
                    </div>

                    <!-- 초기화 버튼 -->
                    <button type="button" class="w-full bg-slate-900 hover:bg-slate-800 text-slate-400 hover:text-slate-200 border border-slate-800 hover:border-slate-700 py-2.5 rounded-xl text-xs font-semibold tracking-wider transition-all duration-200" onclick="resetIntake()">음주 기록 초기화</button>
                </div>
            </div>
        </section>

        <!-- Right Panel: Real-time Dashboard & Mentoring (lg:col-span-7) -->
        <section class="lg:col-span-7 space-y-6">
            
            <!-- 동적 위험 알림 및 게이지 요약 판 -->
            <div id="pnlStatus" class="p-8 rounded-2xl border transition-all duration-300 relative overflow-hidden flex flex-col justify-between h-full min-h-[380px] bg-emerald-500/5 border-emerald-500/20 shadow-xl shadow-emerald-500/2">
                
                <!-- 백그라운드 불빛 효과 -->
                <div id="radialGlow" class="absolute -right-20 -top-20 w-60 h-60 rounded-full filter blur-3xl opacity-20 bg-emerald-500"></div>

                <!-- 상단 헤더 -->
                <div class="relative z-10">
                    <div class="flex items-center justify-between">
                        <span class="text-xs font-bold tracking-widest text-slate-400 uppercase">동적 위험 모니터링 시스템</span>
                        <span id="badgeRisk" class="px-4 py-1.5 rounded-full text-xs font-bold tracking-wide border bg-emerald-500/10 border-emerald-500/30 text-emerald-400">안전 및 유지</span>
                    </div>

                    <!-- 거대 BAC 수치 -->
                    <div class="mt-8">
                        <div class="flex items-baseline space-x-1.5">
                            <span id="txtBAC" class="text-6xl font-black tracking-tight text-slate-100 transition-all duration-300">0.000</span>
                            <span class="text-lg font-bold text-slate-400">%</span>
                        </div>
                        <p class="text-xs text-slate-400 font-semibold mt-1">체내 왓슨-위드마크 보정 알고리즘에 따른 예상 혈중알코올농도</p>
                    </div>
                </div>

                <!-- 중간 게이지 바 -->
                <div class="relative z-10 my-8">
                    <div class="flex justify-between items-center mb-2.5">
                        <span class="text-xs font-bold text-slate-300 flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-amber-500 mr-1.5"></span>개인 한계 대사 진척도</span>
                        <span id="txtProgressRatio" class="text-xs font-extrabold text-slate-100">0.0%</span>
                    </div>
                    <div class="w-full bg-slate-950/80 h-3 rounded-full overflow-hidden p-[2px] border border-slate-800">
                        <div id="barProgress" class="h-full rounded-full transition-all duration-500 ease-out bg-emerald-500 shadow-inner" style="width: 0%"></div>
                    </div>
                    <div class="flex justify-between items-center mt-2 text-[10px] text-slate-500 font-bold tracking-wide">
                        <span>현재: <span id="txtCurrentDrinks">0.0</span> 잔</span>
                        <span>안전 한계 임계치: <span id="txtMaxLimit">3.0</span> 잔</span>
                    </div>
                </div>

                <!-- 하단 보조 세부 속성 데이터 -->
                <div class="relative z-10 grid grid-cols-3 gap-4 pt-4 border-t border-slate-800/60 text-center">
                    <div>
                        <span class="text-[10px] font-bold text-slate-400 uppercase block mb-1">체질량지수 (BMI)</span>
                        <span id="txtBMI" class="text-sm font-extrabold text-slate-200">22.7</span>
                    </div>
                    <div>
                        <span class="text-[10px] font-bold text-slate-400 uppercase block mb-1">위드마크 r 상수</span>
                        <span id="txtWidmarkR" class="text-sm font-extrabold text-slate-200">0.742</span>
                    </div>
                    <div>
                        <span class="text-[10px] font-bold text-slate-400 uppercase block mb-1">알코올 질량</span>
                        <span id="txtAlcoholG" class="text-sm font-extrabold text-slate-200">0.0g</span>
                    </div>
                </div>
            </div>

            <!-- 성향 맞춤형 심리 멘탈케어 개입 박스 -->
            <div class="bg-slate-950/40 p-6 rounded-2xl border border-slate-800/80 backdrop-blur-md relative overflow-hidden">
                <div class="flex items-center space-x-2.5 mb-4 pb-3 border-b border-slate-800/60 relative z-10">
                    <span class="text-xl">🛡️</span>
                    <div>
                        <h2 class="text-base font-semibold text-slate-100">성향 기반 맞춤 심리 멘탈케어</h2>
                        <p class="text-[10px] text-slate-400 font-medium">CBT · MI · ACT 임상 원칙 기반 방어적 메시징 기법 적용</p>
                    </div>
                </div>

                <div class="relative z-10 bg-slate-900/60 border border-slate-800/80 p-5 rounded-xl min-h-[140px] flex flex-col justify-between">
                    <div class="text-sm leading-relaxed text-slate-300 font-medium" id="txtMentalCareMessage">
                        현재 안전한 저위험 음주 구간을 유지하고 있습니다. 스스로 설정한 가치를 기억하며, 알코올 섭취 속도를 늦추고 중간에 충분한 수분을 섭취하여 통제력을 유지하십시오.
                    </div>
                    <div class="mt-4 flex items-center justify-between text-[11px] text-slate-500 font-bold border-t border-slate-850 pt-3">
                        <span id="txtCbtMethod" class="flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-rose-500/80 mr-1.5"></span>적용 모델: 자기 모니터링 (Self-Monitoring)</span>
                        <span id="txtTargetMBTI" class="text-amber-500/80">대상군: ALL</span>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-800/80 bg-slate-950/30 py-4 text-center text-xs text-slate-500 font-medium">
        <div class="max-w-7xl mx-auto px-4">
            <p>© 2026 알코올 알고먹자(알코알먹) Project. 임경민 PRD 및 알코올 치료 상담 지침 준수.</p>
        </div>
    </footer>

    <!-- Core Business Logic JavaScript -->
    <script>
        // State 관리 변수
        let state = {
            gender: 'M',
            soju: 0.0,
            beer: 0,
            wine: 0,
            hours: 1.0
        };

        // DOM 로드 완료 후 실행
        window.onload = function() {
            // 초기 연산 수행
            calculateAll();

            // 입력 필드들에 자동 계산 바인딩
            document.getElementById('inputAge').addEventListener('input', calculateAll);
            document.getElementById('inputHeight').addEventListener('input', calculateAll);
            document.getElementById('inputWeight').addEventListener('input', calculateAll);
        };

        // 성별 스위칭 기능
        function setGender(g) {
            state.gender = g;
            const btnM = document.getElementById('btnGenderM');
            const btnF = document.getElementById('btnGenderF');

            if (g === 'M') {
                btnM.className = "py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-amber-500/10 border-amber-500/50 text-amber-400 shadow-md shadow-amber-500/5";
                btnF.className = "py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-slate-900 border-slate-800 text-slate-400 hover:border-slate-700";
            } else {
                btnF.className = "py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-amber-500/10 border-amber-500/50 text-amber-400 shadow-md shadow-amber-500/5";
                btnM.className = "py-2.5 px-3 rounded-xl border text-sm font-semibold transition-all duration-200 bg-slate-900 border-slate-800 text-slate-400 hover:border-slate-700";
            }
            calculateAll();
        }

        // 음주량 조절 및 렌더링
        function adjustDrinks(type, value) {
            state[type] = Math.max(0, state[type] + value);
            
            if (type === 'soju') {
                document.getElementById('valSoju').innerText = state.soju.toFixed(1);
            } else if (type === 'beer') {
                document.getElementById('valBeer').innerText = state.beer;
            } else if (type === 'wine') {
                document.getElementById('valWine').innerText = state.wine;
            }
            
            calculateAll();
        }

        // 시간 슬라이더 업데이트 및 자동 연산
        function updateHoursLabel(value) {
            state.hours = parseFloat(value);
            document.getElementById('lblHours').innerText = value;
            calculateAll();
        }

        // 음주 기록 리셋
        function resetIntake() {
            state.soju = 0.0;
            state.beer = 0;
            state.wine = 0;
            state.hours = 1.0;

            document.getElementById('valSoju').innerText = '0.0';
            document.getElementById('valBeer').innerText = '0';
            document.getElementById('valWine').innerText = '0';
            document.getElementById('rangeHours').value = 1;
            document.getElementById('lblHours').innerText = '1';

            calculateAll();
        }

        // 전체 핵심 알고리즘 계산 모듈 (혈중알코올농도, 음주 한도, 대사 지표, 심리 피드백 통합 연산)
        function calculateAll() {
            // 1. 값 수집
            const age = parseInt(document.getElementById('inputAge').value) || 20;
            const height = parseFloat(document.getElementById('inputHeight').value) || 178;
            const weight = parseFloat(document.getElementById('inputWeight').value) || 72;
            const isFlusher = document.getElementById('checkFlusher').checked;
            const mbti = document.getElementById('selectMBTI').value;
            const blackoutScore = parseInt(document.getElementById('selectBlackout').value) || 0;

            // 2. BMI 및 Watson 보정 r 상수 연산
            const heightM = height / 100.0;
            const bmi = weight / (heightM * heightM);
            let r = 0;
            if (state.gender === 'M') {
                r = 1.0181 - (0.01213 * bmi);
            } else {
                r = 0.9367 - (0.01240 * bmi);
            }

            // 3. 섭취 잔 수 및 순수 알코올 질량 연산 (표준 1잔 = 14g 기준)
            const drinks = (state.soju * 4.0) + (state.beer * 1.0) + (state.wine * 1.0);
            const alcoholG = drinks * 14.0;

            // 4. 위드마크 공식에 따른 혈중알코올농도(BAC) 연산 (보수적인 최저 대사율 0.010% 적용)
            let bac = 0;
            if (drinks > 0) {
                bac = ((alcoholG * 0.7) / (weight * r * 10.0)) - (0.010 * state.hours);
                bac = Math.max(0.0, bac);
            }

            // 5. 한국형 적정 음주량 가이드라인에 따른 1회 최대 권장량 도출
            const isSenior = age > 65;
            let rawLimit = 0;

            if (state.gender === 'M') {
                if (!isSenior) {
                    rawLimit = isFlusher ? 1.5 : 3.0;
                } else {
                    rawLimit = isFlusher ? 1.0 : 2.0;
                }
            } else {
                if (!isSenior) {
                    rawLimit = isFlusher ? 1.0 : 2.0;
                } else {
                    rawLimit = isFlusher ? 0.5 : 1.0;
                }
            }

            // 부작용 경험(블랙아웃)에 따른 음주량 감점
            const penalty = blackoutScore * 0.5;
            const adjustedLimit = Math.max(0.5, rawLimit - penalty);

            // 6. 진척도 비율 계산
            const ratio = (adjustedLimit > 0) ? (drinks / adjustedLimit) * 100.0 : 0;

            // 7. 위험 모니터링 단계 결정
            let risk = "안전";
            if (ratio >= 80.0 || drinks > adjustedLimit || bac >= 0.05) {
                risk = "위험";
            } else if (ratio >= 50.0) {
                risk = "주의";
            }

            // 8. MBTI의 T/F, J/P 속성에 맞춘 방어적 심리 멘탈케어 메시지 도출
            const isT = mbti.charAt(2) === 'T';
            const isJ = mbti.charAt(3) === 'J';
            let mentalMessage = "";
            let treatmentMethod = "자기 관찰 (Self-Monitoring)";

            if (risk === "안전") {
                mentalMessage = "현재 안전한 저위험 음주 구간을 유지하고 있습니다. 스스로 설정한 인생의 가치를 기억하며, 알코올 섭취 속도를 늦추고 중간에 충분한 물을 섭취해 보십시오.";
                treatmentMethod = "대처 계획 수립 (CBT)";
            } else if (risk === "주의") {
                if (isT) {
                    mentalMessage = "현재 알코올 섭취량이 계산된 1회 허용 임계치의 50%를 넘어섰습니다. 임상 데이터에 따르면 이 시점부터 간 대사 부하가 증가하고 인지 능력이 점진적으로 저하됩니다. 당신의 건강과 안전한 다음 날 아침을 위해 이제 잔을 내려놓고 탄산수로 가볍게 전환해 보는 것은 어떨까요?";
                    treatmentMethod = "객관적 피드백 제공 (MI / FRAMES)";
                } else {
                    mentalMessage = "오늘 하루 정말 수고 많으셨습니다. 지치고 복잡한 감정은 깊이 공감하지만, 내일 아침 더 가볍고 개운하게 눈을 뜰 당신을 위해 오늘 술자리는 여기서 따뜻하게 매듭지어 보는 것이 어떨까요? 술잔을 놓아두는 것만으로도 나를 지키는 좋은 첫걸음이 됩니다.";
                    treatmentMethod = "공감적 연민 지지 (MI)";
                }
            } else { // 위험 단계
                if (isT) {
                    mentalMessage = "경고: 현재 섭취량이 임상적 안전 임계치를 초과하였습니다. ALDH2(알데히드 대사효소) 한계를 넘어선 독성 물질 아세트알데히드의 비정상적 축적이 지속되어 다음 날 블랙아웃 및 간독성 발현 위험이 현격히 높습니다. 신체적 안전 보호를 위해 즉시 술자리 음주를 중단하십시오.";
                    treatmentMethod = "독성 인지적 재구성 (CBT)";
                } else {
                    mentalMessage = "당신이 느끼는 피로감과 술에 기대고 싶은 강박적 갈망은 지극히 인간적이지만, 과도한 알코올 섭취는 당신의 소중한 신체를 가혹하게 혹사시킵니다. 지친 당신의 오늘을 진심으로 안아주고 위로하지만, 절대적 안녕을 위해 여기서 부드럽게 멈추어야 할 때입니다. 나 자신을 아껴주는 용기를 내어주세요.";
                    treatmentMethod = "마음챙김 및 가치 행동 전념 (ACT)";
                }
            }

            // J / P 추가 심리 개입 행동 팁
            if (risk !== "안전") {
                if (isJ) {
                    mentalMessage += " [행동 처방] 술자리가 마무리되는 순간까지 미리 세워둔 절제 한계를 엄격히 유지하고, 주변의 권유를 극적으로 사양하는 '음주 거절 화법'을 실행하십시오.";
                } else {
                    mentalMessage += " [행동 처방] 충동과 갈망은 파도처럼 밀려왔다 사라집니다(파도타기 기법). 지금 즉시 깊은 호흡을 10회 수행하거나 마시는 잔을 시원한 냉수로 즉시 교체하십시오.";
                }
            }

            // 9. UI 대시보드 갱신
            document.getElementById('txtBAC').innerText = bac.toFixed(3);
            document.getElementById('txtProgressRatio').innerText = ratio.toFixed(1) + "%";
            document.getElementById('txtCurrentDrinks').innerText = drinks.toFixed(1);
            document.getElementById('txtMaxLimit').innerText = adjustedLimit.toFixed(1);
            document.getElementById('txtBMI').innerText = bmi.toFixed(1);
            document.getElementById('txtWidmarkR').innerText = r.toFixed(3);
            document.getElementById('txtAlcoholG').innerText = alcoholG.toFixed(1) + "g";
            document.getElementById('txtMentalCareMessage').innerText = mentalMessage;
            document.getElementById('txtCbtMethod').innerHTML = `<span class="w-1.5 h-1.5 rounded-full bg-rose-500/80 mr-1.5"></span>적용 모델: ${treatmentMethod}`;
            document.getElementById('txtTargetMBTI').innerText = `대상군: ${mbti}`;

            // 게이지 바 가로폭 제어
            const clippedRatio = Math.min(100, ratio);
            const bar = document.getElementById('barProgress');
            bar.style.width = clippedRatio + "%";

            // 위험 수준별 UI 컬러 전환 테마 로직
            const pnl = document.getElementById('pnlStatus');
            const glow = document.getElementById('radialGlow');
            const badge = document.getElementById('badgeRisk');
            const txtBAC = document.getElementById('txtBAC');

            if (risk === "안전") {
                pnl.className = "p-8 rounded-2xl border transition-all duration-300 relative overflow-hidden flex flex-col justify-between h-full min-h-[380px] bg-emerald-500/5 border-emerald-500/20 shadow-xl shadow-emerald-500/2";
                glow.className = "absolute -right-20 -top-20 w-60 h-60 rounded-full filter blur-3xl opacity-20 bg-emerald-500";
                badge.className = "px-4 py-1.5 rounded-full text-xs font-bold tracking-wide border bg-emerald-500/10 border-emerald-500/30 text-emerald-400";
                badge.innerText = "안전 및 유지";
                bar.className = "h-full rounded-full transition-all duration-500 ease-out bg-emerald-500 shadow-inner";
                txtBAC.className = "text-6xl font-black tracking-tight text-slate-100 transition-all duration-300";
            } else if (risk === "주의") {
                pnl.className = "p-8 rounded-2xl border transition-all duration-300 relative overflow-hidden flex flex-col justify-between h-full min-h-[380px] bg-amber-500/5 border-amber-500/20 shadow-xl shadow-amber-500/2";
                glow.className = "absolute -right-20 -top-20 w-60 h-60 rounded-full filter blur-3xl opacity-20 bg-amber-500";
                badge.className = "px-4 py-1.5 rounded-full text-xs font-bold tracking-wide border bg-amber-500/10 border-amber-500/30 text-amber-400";
                badge.innerText = "주의 단계";
                bar.className = "h-full rounded-full transition-all duration-500 ease-out bg-amber-500 shadow-inner";
                txtBAC.className = "text-6xl font-black tracking-tight text-amber-400 transition-all duration-300";
            } else { // 위험
                pnl.className = "p-8 rounded-2xl border transition-all duration-300 relative overflow-hidden flex flex-col justify-between h-full min-h-[380px] bg-rose-500/10 border-rose-500/20 shadow-xl shadow-rose-500/2";
                glow.className = "absolute -right-20 -top-20 w-60 h-60 rounded-full filter blur-3xl opacity-20 bg-rose-500";
                badge.className = "px-4 py-1.5 rounded-full text-xs font-bold tracking-wide border bg-rose-500/10 border-rose-500/30 text-rose-400 animate-pulse";
                badge.innerText = "절제 권고 (위험)";
                bar.className = "h-full rounded-full transition-all duration-500 ease-out bg-rose-500 shadow-inner";
                txtBAC.className = "text-6xl font-black tracking-tight text-rose-500 transition-all duration-300";
            }
        }
    </script>
</body>
</html>
