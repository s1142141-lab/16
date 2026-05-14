# 貪吃蛇遊戲 (Snake Game)

這是一個使用 HTML5 Canvas 實現的經典貪吃蛇遊戲。

## 檔案資訊

- **檔案名稱**: snake.html
- **類型**: 單一 HTML 檔案（包含內嵌 CSS 和 JavaScript）
- **語言**: 繁體中文

## 功能特點

- 使用方向鍵或 WASD 控制蛇的移動
- 按空白鍵暫停/繼續遊戲
- 計分系統（每吃一個食物 +10 分）
- 遊戲結束畫面顯示最終分數
- 重新開始功能

## 程式碼結構

### HTML 部分

```html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>貪吃蛇遊戲</title>
    ...
</head>
<body>
    <h1>🐍 貪吃蛇</h1>
    <div id="score">分數: 0</div>
    <div id="gameContainer">
        <canvas id="gameCanvas" width="400" height="400"></canvas>
        <div id="gameOver">
            <h2>遊戲結束!</h2>
            <p>最終分數: <span id="finalScore">0</span></p>
        </div>
    </div>
    <button id="startBtn">開始遊戲</button>
    <div id="controls">
        <p>使用 ↑ ↓ ← → 或 W A S D 控制移動</p>
        <p>按空白鍵暫停/繼續</p>
    </div>
    ...
</body>
</html>
```

### CSS 樣式

- **背景**: 深色漸變 (`linear-gradient(135deg, #1a1a2e 0%, #16213e 100%)`)
- **遊戲畫布**: 400x400 像素，帶有粉紅色邊框和光暈效果
- **配色方案**:
  - 主色: `#e94560` (粉紅色)
  - 次色: `#0f3460` (深藍色)
  - 食物: `#4ecca3` (綠色)
  - 蛇頭: `#ff6b6b` (淺粉紅)

### JavaScript 邏輯

| 函數 | 功能 |
|------|------|
| `initGame()` | 初始化遊戲狀態 |
| `placeFood()` | 放置食物（隨機位置，避免與蛇重疊）|
| `draw()` | 繪製遊戲畫面 |
| `update()` | 更新遊戲邏輯（移動、碰撞檢測）|
| `endGame()` | 結束遊戲並顯示結果 |
| `startGame()` | 開始新遊戲 |

### 遊戲參數

- **格子大小**: 20px
- **畫布大小**: 400x400 (20x20 格)
- **更新間隔**: 100ms
- **初始蛇長**: 3 格
- **分數增量**: 每次吃食物 +10 分

---

*此檔案目前無變更記錄*