<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>나만의 링크 모음 & 랭킹</title>
  <style>
    :root {
      --bg-color: #f8f9fa;
      --card-bg: #ffffff;
      --text-color: #212529;
      --primary-color: #3b82f6;
      --border-color: #e5e7eb;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      padding: 20px;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
    }

    header {
      text-align: center;
      padding: 30px 0 20px;
    }

    header h1 {
      font-size: 2rem;
      color: #1e293b;
      margin-bottom: 8px;
    }

    header p {
      color: #64748b;
      font-size: 0.95rem;
    }

    /* 카테고리 필터 버튼 */
    .category-bar {
      display: flex;
      justify-content: center;
      gap: 8px;
      margin-bottom: 25px;
      flex-wrap: wrap;
    }

    .category-btn {
      background: #ffffff;
      border: 1px solid var(--border-color);
      padding: 8px 16px;
      border-radius: 20px;
      cursor: pointer;
      font-size: 0.9rem;
      font-weight: 600;
      color: #4b5563;
      transition: all 0.2s ease;
    }

    .category-btn:hover, .category-btn.active {
      background-color: var(--primary-color);
      color: white;
      border-color: var(--primary-color);
    }

    /* 링크 그리드 레이아웃 */
    .link-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 15px;
    }

    /* 링크 카드 디자인 */
    .link-card {
      background: var(--card-bg);
      border: 1px solid var(--border-color);
      border-radius: 12px;
      padding: 16px;
      display: flex;
      align-items: center;
      text-decoration: none;
      color: inherit;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .link-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05);
      border-color: #cbd5e1;
    }

    .rank-number {
      font-size: 1.1rem;
      font-weight: 800;
      color: #94a3b8;
      width: 30px;
      text-align: center;
    }

    .link-card:nth-child(1) .rank-number { color: #ef4444; } /* 1위 빨강 */
    .link-card:nth-child(2) .rank-number { color: #f97316; } /* 2위 주황 */
    .link-card:nth-child(3) .rank-number { color: #eab308; } /* 3위 노랑 */

    .link-icon {
      width: 40px;
      height: 40px;
      border-radius: 8px;
      background: #f1f5f9;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      margin: 0 12px;
      flex-shrink: 0;
    }

    .link-info {
      flex-grow: 1;
      overflow: hidden;
    }

    .link-title {
      font-weight: 700;
      font-size: 1rem;
      margin-bottom: 2px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .link-desc {
      font-size: 0.8rem;
      color: #64748b;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .badge {
      font-size: 0.7rem;
      background: #eff6ff;
      color: var(--primary-color);
      padding: 2px 6px;
      border-radius: 4px;
      margin-left: 6px;
    }
  </style>
</head>
<body>

  <div class="container">
    <header>
      <h1>📌 나만의 링크 랭킹 모음</h1>
      <p>원하는 카테고리별 사이트 모음 및 바로가기</p>
    </header>

    <!-- 카테고리 필터 -->
    <div class="category-bar" id="categoryBar"></div>

    <!-- 링크 목록 영역 -->
    <div class="link-grid" id="linkGrid"></div>
  </div>

  <script>
    /* =========================================================
       1. 카테고리 목록 설정
    ========================================================= */
    const categoryList = ["전체", "서비스", "알뜰정보", "토렌트", "포털/커뮤니티", "파일위키", "블로그", "무료웹툰", "AI tool"];

    /* =========================================================
       2. 전체 링크 데이터 (이미지 2장 내용 전체 수록)
    ========================================================= */
    const links = [
      // [서비스]
      { category: "서비스", name: "코버스", url: "https://www.kobus.co.kr/main.do", desc: "고속버스통합예매", icon: "🚌" },
      { category: "서비스", name: "구글지도", url: "https://www.google.co.kr/maps", desc: "지도맵", icon: "🗺️" },
      { category: "서비스", name: "지하철노선", url: "https://map.naver.com/p/subway/1000/-/-/", desc: "네이버노선표", icon: "🚇" },
      { category: "서비스", name: "우편번호", url: "https://www.epost.go.kr/search.RetrieveIntegrationNewZipCdList.comm", desc: "우편번호검색", icon: "📮" },
      { category: "서비스", name: "카카오맵", url: "https://map.kakao.com/?nil_profile=title&nil_src=local", desc: "교통정보", icon: "📍" },
      { category: "서비스", name: "코레일", url: "https://bt.korail.com/holiday/main", desc: "기차예매", icon: "🚆" },

      // [알뜰정보]
      { category: "알뜰정보", name: "로고카이", url: "https://mybrandnewlogo.com/ko/", desc: "자동로고메이커", icon: "🎨" },
      { category: "알뜰정보", name: "쓩패스", url: "https://www.sshoong.com/pass/", desc: "해외배송정보", icon: "✈️" },
      { category: "알뜰정보", name: "중고서치", url: "https://father.is-an.ai/Market/#/", desc: "중고검색", icon: "🔍" },
      { category: "알뜰정보", name: "데일리팝", url: "http://www.dailypop.kr/", desc: "1인가구미디어", icon: "📰" },
      { category: "알뜰정보", name: "공공서비스", url: "https://yeyak.seoul.go.kr/web/main.do/", desc: "서울시공공예약", icon: "🏛️" },
      { category: "알뜰정보", name: "알구몬", url: "https://www.algumon.com/n/deal/", desc: "핫딜", icon: "🔥" },
      { category: "알뜰정보", name: "정보통통", url: "https://www.jungbo114.com/", desc: "잡다한 모든 정보", icon: "💡" },
      { category: "알뜰정보", name: "이지티켓", url: "https://easyticket.co.kr/", desc: "여행정보 매거진", icon: "🎫" },
      { category: "알뜰정보", name: "펴늬", url: "https://pyony.com/", desc: "편의점할인", icon: "🏪" },
      { category: "알뜰정보", name: "알뜰폰 허브", url: "https://www.alnba.or.kr", desc: "알뜰폰 요금제 비교 검색", icon: "📲" },

      // [토렌트]
      { category: "토렌트", name: "이토렌트", url: "https://etoland.co.kr/", desc: "토렌트 커뮤", icon: "💬" },
      { category: "토렌트", name: "비트딕", url: "https://btdig.com/index.htm", desc: "파일 검색", icon: "🔎" },
      { category: "토렌트", name: "이지티비", url: "https://eztvx.to/", desc: "EZTV", icon: "📺" },
      { category: "토렌트", name: "1337", url: "https://1337x.to/home/", desc: "토렌트 커뮤", icon: "🧲" },
      { category: "토렌트", name: "섭디", url: "https://subdl.com/", desc: "Sub자막 검색", icon: "📝" },
      { category: "토렌트", name: "스키드로우", url: "https://www.skidrowreloaded.com/", desc: "복돌이", icon: "🎮" },
      { category: "토렌트", name: "도리리펙", url: "https://dodi-repacks.site/", desc: "복돌이", icon: "🕹️" },
      { category: "토렌트", name: "핏걸", url: "https://fitgirl-repacks.site/", desc: "복돌이", icon: "🎮" },
      { category: "토렌트", name: "리팩게임을", url: "https://repack-games.com/", desc: "복돌이", icon: "🕹️" },
      { category: "토렌트", name: "프로그탑넷", url: "https://prog-top.net/", desc: "소프트웨어", icon: "💾" },
      { category: "토렌트", name: "SmiDown", url: "https://subtitle.sunghwanyoo.com/", desc: "smi자막 검색", icon: "💬" },
      { category: "토렌트", name: "곰랩", url: "https://www.gomlab.com/subtitle-home/", desc: "곰랩자막 검색", icon: "🎬" },
      { category: "토렌트", name: "YTS", url: "https://www.yts.gg", desc: "영화 토렌트", icon: "🎬" },
      { category: "토렌트", name: "EXT", url: "https://ext.to/", desc: "토탈 토렌트", icon: "🌐" },

      // [포털/커뮤니티]
      { category: "포털/커뮤니티", name: "인벤", url: "https://www.inven.co.kr/", desc: "게임 커뮤니티", icon: "⚔️" },
      { category: "포털/커뮤니티", name: "뽐뿌", url: "https://www.ppomppu.co.kr/", desc: "함께하는곳", icon: "🛒" },
      { category: "포털/커뮤니티", name: "디시인사이드", url: "https://www.dcinside.com//", desc: "디시갤러리", icon: "💬" },
      { category: "포털/커뮤니티", name: "SLR클럽", url: "https://www.slrclub.com//", desc: "사진 커뮤니티", icon: "📷" },
      { category: "포털/커뮤니티", name: "인스티즈", url: "https://www.instiz.net/", desc: "팬덤", icon: "⭐" },
      { category: "포털/커뮤니티", name: "쿨엔조이", url: "https://coolenjoy.net/", desc: "PC 커뮤니티", icon: "🖥️" },
      { category: "포털/커뮤니티", name: "2CPU", url: "https://www.2cpu.co.kr/", desc: "듀얼메인보드사용자모임", icon: "⚙️" },
      { category: "포털/커뮤니티", name: "루리웹", url: "https://www.ruliweb.com/", desc: "비디오게이머 커뮤", icon: "🎮" },
      { category: "포털/커뮤니티", name: "보배드림", url: "https://www.bobaedream.co.kr/", desc: "자동차쇼핑몰", icon: "🚗" },
      { category: "포털/커뮤니티", name: "에펨코리아", url: "https://www.fmkorea.com/", desc: "종합커뮤니티", icon: "⚽" },
      { category: "포털/커뮤니티", name: "윈도우포럼", url: "https://windowsforum.kr/", desc: "윈도우커뮤니티", icon: "🪟" },

      // [파일위키]
      { category: "파일위키", name: "스매쉬", url: "https://fromsmash.com/", desc: "용량 2GB / 7일 / 자동삭제", icon: "💥" },
      { category: "파일위키", name: "파일키위", url: "https://file.kiwi/", desc: "용량 무제한 / 48시간 / 90시간 후 삭제", icon: "🥝" },
      { category: "파일위키", name: "워크업", url: "https://workupload.com/", desc: "용량 2GB / 90일간 공유 / 익명", icon: "📤" },
      { category: "파일위키", name: "고파일", url: "https://gofile.io/welcome/", desc: "용량 10GB / 10일 / 자동삭제", icon: "📁" },
      { category: "파일위키", name: "기가파일", url: "https://gigafile.nu/", desc: "용량 200GB / 100일 / 자동삭제", icon: "📦" },
      { category: "파일위키", name: "업로드EE", url: "https://www.upload.ee/", desc: "용량 100MB / 50일 / 자동삭제", icon: "☁️" },
      { category: "파일위키", name: "파일나우", url: "https://d.kuku.lu/", desc: "용량 300GB / 지속적 다운되는 파일 무삭제", icon: "🚀" },
      { category: "파일위키", name: "인피니", url: "https://infini-cloud.net/en/", desc: "용량 20GB / 무료 클라우드", icon: "☁️" },
      { category: "파일위키", name: "토피쉐어", url: "https://toffeeshare.com/", desc: "P2P 파일 공유", icon: "🍬" },
      { category: "파일위키", name: "샌드", url: "https://send.vis.ee/", desc: "용량 2GB / 다운횟수 10회 / 1일", icon: "🔒" },
      { category: "파일위키", name: "미디어파이어", url: "https://www.mediafire.com/", desc: "용량 4GB / 자동삭제", icon: "🔥" },
      { category: "파일위키", name: "소프트픽", url: "https://www.softpick.co.kr/", desc: "무료 소프트웨어", icon: "💻" },
      { category: "파일위키", name: "업투다운", url: "https://kr.uptodown.com/windows/", desc: "무료 PC 소프트웨어", icon: "⬇️" },
      { category: "파일위키", name: "니나이트", url: "https://ninite.com/", desc: "사용자 지정 설치 프로그램", icon: "🛠️" },
      { category: "파일위키", name: "소프트피디아", url: "https://www.softpedia.com/", desc: "다운로드 컬렉션", icon: "📂" },
      { category: "파일위키", name: "파일히포", url: "https://filehippo.com/", desc: "BEST & SAFE 소프트웨어", icon: "🦛" },
      { category: "파일위키", name: "다운크루", url: "https://www.downloadcrew.com/", desc: "엄선된 최고의 다운로드", icon: "⚓" },
      { category: "파일위키", name: "파일퓨마", url: "https://www.filepuma.com/", desc: "PC 소프트웨어", icon: "🐆" },
      { category: "파일위키", name: "파일씨알", url: "https://filecr.com//", desc: "최대규모 소프트웨어", icon: "🗄️" },
      { category: "파일위키", name: "보물닷컴", url: "https://software.dreamwiz.com/", desc: "(구)드림위즈 자료실", icon: "💎" },
      { category: "파일위키", name: "소프트다운타운", url: "https://www.softdowntown.com/", desc: "네이버자료실 대체", icon: "🏢" },
      { category: "파일위키", name: "케이벤치", url: "https://kbench.com/software/", desc: "필수 유틸리티", icon: "🔧" },
      { category: "파일위키", name: "포터블파즈", url: "https://portableappz.blogspot.com/", desc: "포터블 사이트", icon: "🎒" },
      { category: "파일위키", name: "포터블앱", url: "https://portableapps.com/", desc: "오픈 소프트웨어", icon: "📦" },
      { category: "파일위키", name: "판다헬퍼", url: "https://m.pandahelp.vip/", desc: "iOS 및 안드로이드 앱", icon: "🐼" },
      { category: "파일위키", name: "모드피드", url: "https://modfyp.com/", desc: "안드로이드 앱 스토어", icon: "📲" },
      { category: "파일위키", name: "APK키퍼", url: "https://apkkeeper.com/", desc: "APK 파일 다운로더", icon: "🤖" },

      // [블로그]
      { category: "블로그", name: "Retrospect", url: "https://kkull.blog.fc2.com/", desc: "개인블로그", icon: "📻" },
      { category: "블로그", name: "컴테크", url: "https://infohelpful.com/", desc: "IT 정보", icon: "💻" },
      { category: "블로그", name: "흥차의꿈", url: "https://jsb000.tistory.com/2429/", desc: "MS Office Preview", icon: "📊" },
      { category: "블로그", name: "열목이", url: "https://lenok-love.tistory.com/", desc: "자동화 방송", icon: "🤖" },

      // [무료웹툰]
      { category: "무료웹툰", name: "코사이트", url: "https://korsite.net/", desc: "최신 정보와 대체 사이트", icon: "🌐" },
      { category: "무료웹툰", name: "펀비", url: "https://t.me/s/funbe_next/", desc: "웹툰", icon: "📖" },
      { category: "무료웹툰", name: "늑대닷컴", url: "https://t.me/s/wfwf_com", desc: "늑대닷컴 공식채널", icon: "🐺" },
      { category: "무료웹툰", name: "뉴토끼", url: "https://t.me/s/newtokinews", desc: "뉴토끼&마나토끼", icon: "🐰" },
      { category: "무료웹툰", name: "뚜툰", url: "https://ddtoon21.com/mlist.php", desc: "최근 웹툰", icon: "🎨" },
      { category: "무료웹툰", name: "미미티비", url: "https://mimitv3.com/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "뷰티비", url: "https://vitv88.com/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "낭티비", url: "https://nortv91.com/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "콕콕티비", url: "https://xn--9w3b352aa608a.com/", desc: "무료 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "무비킹", url: "https://mvking17.org/", desc: "TV 다시보기", icon: "🎬" },
      { category: "무료웹툰", name: "티비착", url: "https://tvchak.org/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "후후티비", url: "https://telegra.ph/%ED%9B%84%ED%9B%84%ED%8B%B0%EB%B9%B0-09-03/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "애니어바웃", url: "https://www.aniabout2.com/", desc: "애니 다시보기", icon: "✨" },
      { category: "무료웹툰", name: "애니114", url: "https://jusobook1.com/bookmark_link/%ec%95%a0%eb%8b%88114/", desc: "애니 다시보기", icon: "✨" },
      { category: "무료웹툰", name: "고고티비", url: "https://gogotv.net/", desc: "TV 다시보기", icon: "📺" },
      { category: "무료웹툰", name: "온도티비", url: "https://xn--hq1b42rdlg8wn.com/", desc: "온도 커뮤니티", icon: "💬" },

      // [AI tool]
      { category: "AI tool", name: "ChatGPT", url: "https://chatgpt.com", desc: "OpenAI 대화형 AI 모델", icon: "🤖" },
      { category: "AI tool", name: "Claude", url: "https://claude.ai", desc: "Anthropic의 대화형 AI 서비스", icon: "🧠" },
      { category: "AI tool", name: "Midjourney", url: "https://www.midjourney.com", desc: "고성능 AI 이미지 생성 툴", icon: "🎨" }
    ];

    // DOM 요소 참조
    const linkGrid = document.getElementById('linkGrid');
    const categoryBar = document.getElementById('categoryBar');

    // 카테고리 버튼 생성
    categoryBar.innerHTML = categoryList.map((cat, idx) => `
      <button class="category-btn ${idx === 0 ? 'active' : ''}" onclick="filterCategory('${cat}')">${cat}</button>
    `).join('');

    // 링크 카드 렌더링 함수
    function renderLinks(data) {
      linkGrid.innerHTML = data.map((item, index) => `
        <a href="${item.url}" class="link-card" target="_blank" rel="noopener noreferrer">
          <div class="rank-number">${index + 1}</div>
          <div class="link-icon">${item.icon}</div>
          <div class="link-info">
            <div class="link-title">${item.name} <span class="badge">${item.category}</span></div>
            <div class="link-desc">${item.desc}</div>
          </div>
        </a>
      `).join('');
    }

    // 카테고리 필터링 함수
    function filterCategory(category) {
      document.querySelectorAll('.category-btn').forEach(btn => {
        btn.classList.toggle('active', btn.innerText === category);
      });

      if (category === '전체') {
        renderLinks(links);
      } else {
        const filtered = links.filter(item => item.category === category);
        renderLinks(filtered);
      }
    }

    // 초기 실행 (전체 목록 출력)
    renderLinks(links);
  </script>
</body>
</html>
