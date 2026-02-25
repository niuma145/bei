<!DOCTYPE html>
<html lang="zh-CN">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>系统维护中</title>
   <style>
       * {
           margin: 0;
           padding: 0;
           box-sizing: border-box;
       }

       body {
           height: 100vh;
           display: flex;
           justify-content: center;
           align-items: center;
           background: #0a0a0a;
           font-family: "Microsoft YaHei", "PingFang SC", sans-serif;
           overflow: hidden;
       }

       .maintenance-container {
           text-align: center;
           color: #fff;
           padding: 40px;
           position: relative;
           z-index: 10;
       }

       .status-icon {
           font-size: 80px;
           margin-bottom: 30px;
           animation: pulse 2s ease-in-out infinite;
           display: block;
       }

       @keyframes pulse {
           0%, 100% { opacity: 0.6; transform: scale(1); }
           50% { opacity: 1; transform: scale(1.1); }
       }

       .main-title {
           font-size: 28px;
           font-weight: 300;
           letter-spacing: 8px;
           margin-bottom: 20px;
           color: #e0e0e0;
       }

       .sub-title {
           font-size: 16px;
           color: #666;
           letter-spacing: 2px;
       }

       /* 背景装饰 */
       .bg-decoration {
           position: fixed;
           top: 0;
           left: 0;
           width: 100%;
           height: 100%;
           pointer-events: none;
       }

       .bg-decoration::before {
           content: '';
           position: absolute;
           top: 50%;
           left: 50%;
           width: 600px;
           height: 600px;
           transform: translate(-50%, -50%);
           background: radial-gradient(circle, rgba(255,255,255,0.03) 0%, transparent 70%);
           animation: breathe 4s ease-in-out infinite;
       }

       @keyframes breathe {
           0%, 100% { transform: translate(-50%, -50%) scale(1); opacity: 0.5; }
           50% { transform: translate(-50%, -50%) scale(1.2); opacity: 0.8; }
       }

       /* 网格背景 */
       .grid-bg {
           position: fixed;
           top: 0;
           left: 0;
           width: 100%;
           height: 100%;
           background-image: 
               linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
               linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
           background-size: 50px 50px;
           pointer-events: none;
       }
   </style>
</head>
<body>
   <div class="grid-bg"></div>
   <div class="bg-decoration"></div>
   
   <div class="maintenance-container">
       <span class="status-icon">⚡</span>
       <h1 class="main-title">维护期间暂不能领取</h1>
       <p class="sub-title">SYSTEM MAINTENANCE</p>
   </div>
</body>
</html>
