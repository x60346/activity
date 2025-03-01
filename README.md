藝文活動查找平台，串接文化部提供免費API。

使用 Vue3.js 搭建。

使用Bootstrap 5、axios套件。

----------------------------------------------------------

畫面有 5 個：首頁、藝文活動、節慶活動、查找周圍活動、活動詳情。

----------------------------------------------------------

＞ 資料夾內容：

  @/src/assets：reset.css

  @/src/router：路由規則文件

  @/src/views：路由元件

  @/src/store：pinia管理資料（全API）

----------------------------------------------------------

＞ API：

  活動詳細資料
  https://cloud.culture.tw/frontsite/opendata/activityOpenDataJsonAction.do?method=doFindActivityById&id=${props.uuid}

  經緯度查找資料
  https://cloud.culture.tw/frontsite/opendata/activityOpenDataJsonAction.do?method=doFindActivitiesNearBy&lat=${lat}&lon=${lon}&range=4

  類型查找資料
  https://cloud.culture.tw/frontsite/trans/SearchShowAction.do?method=doFindTypeJ&category=${type}

  節慶資料
  https://cloud.culture.tw/frontsite/trans/SearchShowAction.do?method=doFindFestivalTypeJ

  標語
  https://cloud.culture.tw/frontsite/trans/SearchShowAction.do?method=doFindIssueTypeJ

  所有活動
  https://cloud.culture.tw/frontsite/opendata/activityOpenDataJsonAction.do?method=doFindActivitiesByCategory&category=all

----------------------------------------------------------

＞ 網頁布局（路由交互）

  APP
  ｜－頂部
  ｜   ｜ 
  ｜   ｜ －網頁名稱（點擊返回首頁）（to：@/views/Home.vue）
  ｜   ｜ 
  ｜   ｜ －操作列表
  ｜          ｜
  ｜          ｜－舞動藝文（to：@/views/ArtActivity.vue）
  ｜          ｜
  ｜          ｜－節慶活動（to：@/views/Festival.vue）
  ｜          ｜
  ｜          ｜－查找周圍活動（to：@/views/AroundActivity.vue）  
  ｜   
  ｜－routerView 區（以路由切換 "@/router/index.ts"）
  ｜
  ｜－底部
      ｜
      ｜－說明文字

