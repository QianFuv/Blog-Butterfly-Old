---
title: 说说
date: 2023-02-25 00:00:00
type: "talk"
aside: false
comments: false
---
<head>
  <!-- ... -->
  <script src="//cdn.jsdelivr.net/gh/Uyoahz26/daodao@main/dist/qexo-dao.min.js"></script>
  <!-- ... -->
</head>
<body>
  <!-- ... -->
  <div id="qexoDaoDao"></div>
  <script>
    qexoDaodao?.init({
      el: "#qexoDaoDao",
      avatar: "https://q1.qlogo.cn/g?b=qq&nk=2496091142&s=640",
      name: "UyoAhz",
      limit: 10,
      useLoadingImg: false,
      baseURL: "https://admin.qianf.fun",
    }).then(function (){
      console.log("qexoDaodao加载完成");
    })
  </script>
</body>