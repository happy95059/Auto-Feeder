## 使用手冊 - 自動餵食器

### 餵食功能
- **A. 倒數計時**  
  - 當時間到達設定的倒數計時後，會自動進行餵食。
- **B. 設定時間**  
  - 每隔設定的時間，就會自動進行一次餵食。
- **C. 直接餵食**  
  - 手動觸發，立即執行餵食。
- **D. 清除模式**  
  - **A. 倒數計時清空**  
    - 清除倒數計時餵食設置（清除 A 功能）。
  - **B. 循環計時清空**  
    - 清除循環計時餵食設置（清除 B 功能）。
  - **C. 查看目前所有數值**  
    - 檢查所有目前的設定值。
  - **D. 開啟設定模式**  
    - 進入設定模式，對裝置進行調整。

### 設定模式
- **A. 初始化**  
  - 重置所有設定，恢復至預設狀態。
- **B. 設定餵食距離**  
  - 調整餵食的距離參數。
- **C. 設定食物量**  
  - 設定每次餵食的食物量。
- **D. 開關超音波感測器**  
  - 開啟或關閉超音波感測器。

### 鍵盤輸入方式
- 每次輸入十位數整數進行操作。
- 若輸入錯誤，請按 `*` 重新輸入。
- 當輸入正確後，請按 `#` 確認。

### 指示燈功能
- **第一顆燈 (C1) - 工作燈**  
  - 每秒閃爍一次，表示設備處於正常計時狀態。
- **第二顆燈 (A15) - 執行燈**  
  - 開始餵食時亮燈，餵食完成後熄燈。


## 硬體腳位說明

### LED 指示燈
| **功能**           | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| 工作燈              | `C1`     | 每秒閃爍一次，代表正常運行狀態。            |
| 執行燈              | `A15`    | 喂食過程中亮燈，喂食完成後熄滅。            |

### 按鍵矩陣
| **類型**           | **腳位** | **類型**           | **腳位** |
|---------------------|----------|---------------------|----------|
| 行 1               | `A0`     | 列 1               | `B0`     |
| 行 2               | `A1`     | 列 2               | `B1`     |
| 行 3               | `A2`     | 列 3               | `B2`     |
| 行 4               | `A3`     | 列 4               | `B3`     |

### 感測器
| **感測器**         | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| 水位感測器          | `A6`     | 讀取水位數據，用於監控水位。                |

### MCTM 計時與控制
| **功能**           | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| MCTM 輸出          | `C1`     | 輸出控制訊號，用於計時控制。                |
| MCTM 計時讀取      | `C10`    | 讀取 MCTM 計時並計數，適用於時間管理。      |

### 觸發中斷
| **功能**           | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| 觸發中斷 (EXTI)     | `B12`    | 觸發外部中斷，啟動餵食過程。                |

### 馬達控制
| **馬達部分**       | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| 步進馬達 1         | `C14`    | 控制步進馬達A信號。                         |
| 步進馬達 2         | `C15`    | 控制步進馬達A信號。                         |
| 步進馬達 3         | `D1`     | 控制步進馬達A信號。                         |
| 步進馬達 4         | `D2`     | 控制步進馬達A信號。                         |
| 步進馬達 5         | `B5`     | 控制步進馬達B信號。                         |
| 步進馬達 6         | `B6`     | 控制步進馬達B信號。                         |
| 步進馬達 7         | `B7`     | 控制步進馬達B信號。                         |
| 步進馬達 8         | `B8`     | 控制步進馬達B信號。                         |

### I2C 通訊
| **功能**           | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| I2C 時鐘 (SCL)     | `C4`     | I2C 通訊的時鐘線。                         |
| I2C 數據 (SDA)     | `C5`     | I2C 通訊的數據線。                         |

### 超音波感測器
| **功能**           | **腳位** | **描述**                                   |
|---------------------|----------|--------------------------------------------|
| 觸發 (Trig)         | `A5`     | 發送超音波信號。                           |
| 回波 (Echo)         | `A7`     | 接收超音波信號。                           |

