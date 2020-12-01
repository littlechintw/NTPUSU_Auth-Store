<script>
const full_store_list = [
  {
    title: "食物",
    store: [
      {
        title: "johnny bro 健康廚房",
        subtitle: "營養滿點的美味健身餐",
        discount: "折抵 10 元",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "添財號碳烤土司",
        subtitle: "炭烤三明治 牛排",
        discount:
          "1. 限本人主餐+飲料折扣 5 元(添財套餐也可優惠 5 元) 2. 點排餐，贈薯條、雞塊一份(周末限定)",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "元崎麵包坊",
        subtitle: "麵包店",
        discount: "店內商品及餐盒餐點享 9 折優惠",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "來壺果飲",
        subtitle: "果昔、鮮果特調、蔬果汁",
        discount: "消費 60 元(以上)的飲品每滿百可折抵 10 元",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "西貢經典美食",
        subtitle: "豪華牛肉河粉、香茅雞肉飯",
        discount: "消費金額享 9 折優惠",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "steak boy",
        subtitle: "牛排、義大利麵",
        discount:
          "飲料(汽水類)無限暢飲或主餐類餐點享 9 折優惠(套餐部分不再此優惠內)",
        img: "",
        website: "https://www.walkerland.com.tw/article/view/221887",
        map: "",
      },
      {
        title: "橘村屋",
        subtitle: "蛋糕",
        discount: "全系列蛋糕 95 折(恕不與其他優惠合併使用)",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "oh sugar cafe",
        subtitle: "早午餐、鹹鬆餅、咖哩",
        discount: "消費金額享 9 折優惠",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "維羅納義大利麵",
        subtitle: "義大利麵",
        discount:
          "消費折 10 元且免費加大該餐點一次。打卡或 Google 評論送茶凍。",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "Elsa Cafe",
        subtitle: "貓咪、咖啡、鮮奶茶、鬆餅",
        discount: "店內飲品折價 20 元 (恕不與其他優惠合併使用)",
        img: "",
        website:
          "https://waitingangel0514.pixnet.net/blog/post/347050648-%E5%91%B7%E9%A3%BD%E7%A5%99%E3%80%90%E6%96%B0%E5%8C%97%E4%B8%89%E5%B3%BD%EF%BD%A5elsa-caf%C3%89%E3%80%91%E8%B2%93%E5%A5%B4%E5%8F%88%E5%A4%9A%E4%BA%86%E4%B8%80",
        map: "",
      },
      {
        title: "吉購吉",
        subtitle: "豬排丼、​炸物小菜",
        discount: "週一至五消費享 95 折 (恕不與其他優惠合併使用)",
        img: "",
        website:
          "https://dressingfrad.pixnet.net/blog/post/437377972-%E4%B8%89%E5%B3%BD-%E5%8C%97%E5%A4%A7%E7%89%B9%E5%8D%80-%E5%90%89%E8%B3%BC%E5%90%89%E6%97%A5%E5%BC%8F%E4%B8%BC%E9%A3%AF-%E8%B6%85%E4%BE%BF%E5%AE%9C%E8%B1%AC%E4%B8%BC-",
        map: "",
      },
      {
        title: "WaWa Land 三峽北大店",
        subtitle: "鬆餅、簡餐、義大利麵、千層麵",
        discount: "消費金額享 9 折優惠 (限平日)",
        img: "",
        website:
          "https://nixojov.pixnet.net/blog/post/296878936-%E3%80%90%E5%8F%B0%E5%8C%97%E9%A4%90%E5%BB%B3%E3%80%91wawa%E6%A8%82%E5%9C%92-%E5%A4%96%E9%85%A5%E5%85%A7%E8%BB%9F%E7%BE%8E%E5%91%B3%E9%AC%86%E9%A4%85-%E4%B8%89%E5%B3%BD",
        map: "",
      },
      {
        title: "比時地美式漢堡",
        subtitle: "美式漢堡、炸雞",
        discount: "消費金額享 95 折優惠",
        img: "",
        website:
          "https://faith9929.pixnet.net/blog/post/44098776-%5B%E5%8C%97%E5%A4%A7%5D%E7%B4%94%E6%AD%A3%E5%A5%BD%E6%96%99%E7%BE%8E%E5%BC%8F%E5%A4%A7%E6%BC%A2%E5%A0%A1-%E6%AF%94%E6%99%82%E5%9C%B0-big-steve%27s-",
        map: "",
      },
      {
        title: "台北永和豆漿大王",
        subtitle: "油條、蛋餅",
        discount: "消費滿百享 95 折優惠 (優惠商品不算在此滿百折扣中)",
        img: "",
        website: "",
        map: "",
      },
    ],
  },
  {
    title: "其他",
    store: [
      {
        title: "千堤髮妍(大德館)",
        subtitle: "美髮、沙龍​",
        discount:
          "免儲值即享頂級 VIP 折扣，洗.剪.補染.補燙享 9 折；燙.染.護.頭皮保養享 85 折 (採預約制.可指定設計師)",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "C and Y 時尚造型沙龍",
        subtitle: "美髮、沙龍",
        discount: "剪髮享7折(400元)、燙染護頭皮SPA享85折",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "neighbours 複合式自助洗衣",
        subtitle: "咖啡、洗衣店、甜點店",
        discount:
          "甜點、冷熱飲享 9 折(洗衣烘衣項目、特價組合商品不再優惠範圍內)",
        img: "",
        website: "https://jenis0529.pixnet.net/blog/post/403822508",
        map: "",
      },
      {
        title: "益銘藥師藥局",
        subtitle: "藥店",
        discount: "商品一律會員價",
        img: "",
        website: "https://www.facebook.com/Alina.86713268/",
        map: "",
      },
      {
        title: "ALICE愛創藝",
        subtitle: "手作課",
        discount: "滿額 100 元皆享有 9.5 折，任一課程皆現折 50 元",
        img: "",
        website: "",
        map: "",
      },
      {
        title: "陽光樂活 2 館",
        subtitle:
          "Skechers、Mizuno、Asics、Brooks、Hoka one one、Teva、運動服飾、泳裝與配件等其他商品",
        discount: "全品項 9 折",
        img: "",
        website: "https://www.facebook.com/SUNNYLOHASSTORE",
        map: "",
      },
      {
        title: "朵貓貓北大店",
        subtitle: "洗鞋、洗包​",
        discount: "全品項9折",
        img: "",
        website: "",
        map: "",
      },
    ],
  },
];

export default {
  full_store_list,
};
</script>