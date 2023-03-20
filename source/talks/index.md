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
      avatar: "https://vip2.loli.io/2023/02/24/78svlbO5q2KYIgc.jpg",
      name: "浅风",
      limit: 10,
      useLoadingImg: false,
      baseURL: "https://admin.qianf.fun",
      title: "",
      fromColor: "#696969",
      labelColor: "#696969",
    }).then(function (){
      console.log("qexoDaodao加载完成");
    })
  </script>
</body>