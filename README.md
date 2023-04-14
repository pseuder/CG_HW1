# 透過threejs打造可操控機器人

* Three.js  
    * WebGLRenderer: 基於webGL的渲染器
    * Scene: 容納所有threejs做出來的3D物件
    * PerspectiveCamera: 基於Perspective投影法的呈現方式
    * DirectionalLight: 直向光源, 用來呈現陰影, 反光等效果
    * Object3D: 為機器人建立一個3D系統, 後續的Mesh皆依此為基準
    * Geometry: 3D物件的形狀
    * TextureLoader: 加載3D物件的顏色, 材質等材質
    * Mesh: 將Geometry和Texture結合
    * OrbitControls: 讓使用者可以用滑鼠自由操控camara視角
* 心得&困難  
    第一次接觸jacascript, 相比於c++方便很多, 能做的事情也遠遠超乎我的想像

    在這個作業中, 第一次將以前學過的物理知識融入到程式中, 例如計算當前速度時用到: v＝v0＋at, 跳躍時的自由落體用到: y＝-1/2gt^2 

    為了監聽使用者的按鍵, 一開始是直接根據使用者的操作來驅動畫面更新, 但所呈現出來的效果很不順暢, 於是在參考別人的作品後發現requestAnimationFrame這個原生函數完美符合我的需求, 使用起來也很方便


# 操作&控制
* 機器人
    * WASD 控制移動方向
    * 上下左右鍵控制頭部轉向
    * 空格跳躍(最多兩次)
    * enter鍵 發射砲彈
* 相機視角
    * 滑鼠左鍵按住控制視角
    * 滾輪控制縮放
* GUI
     * Heading: 唯讀, 顯示當前面向角度
    * Velocity: 唯讀, 顯示當前速度
    * addSpeed: 控制移動時的加速度
    * rotSpeed: 控制轉動時的加速度
    * Stop: 停止移動
    * FollowMe: 將機器人鎖定至camara視角中心
# 畫面
<img width="1710" alt="截圖 2023-04-14 下午3 11 27" src="https://user-images.githubusercontent.com/51692158/231971539-1a7883d3-a038-4cae-9f14-ebb918e7e04b.png">

<img width="1698" alt="截圖 2023-04-14 下午3 10 20" src="https://user-images.githubusercontent.com/51692158/231971568-7bbf0428-9e87-4542-a413-89da44dba836.png">


# 線上demo: 
## [Github page](https://pseuder.github.io/Threejs_BB8/index.html)

