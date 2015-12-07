#前端工程師的設計流程 (for React) v0.1

keyword: Design Process, React

套上 BASIC 線性設計流程  
B: 定義問題 (Briefing the problem)  
A: 分析 (Analysis)  
S: 重構 (Synthesis)  
I: 實作 (Implementation)  
C: 傳達 (Communication)  
  
B1) 透過溝通和觀察，找出真正要解的「問題 / User Stories」是什麼  
  
A1) 研究「問題 / User Stories」的現有解法  
A2) 分析解法中問題的「階層架構/模組」和「資料表達 - data / state / 資料結構」  
A3) 分析解法中的「資料表達」的變化流程  
  
S1）對 A 重新提出各種更好的設計、包含 Prototype ( PS: 這步蘋果會有十種設計，之後會挑三種進入實作)  
  
I.函數化.1) 想有哪些 UI components 才能實現這個「資料表達」的變化流程  
I.函數化.2) 想每個 component 的 props (對外API & 元件要知道多少問題中自己的角色)  
I.render.1) 寫 Javascript 把 props 轉換成 HTML元件和埋 CSS Classes  
I.render.2) 寫 CSS in local scope 來控制元件外觀的變化 ( CSS 是元件 pure function 的一部份啊 )  
I.render.3) 幫 Pure and Shallow 元件都裝上 ReactComponentWithPureRenderMixin 加速  
I.資料流) 寫 Javascript 處理 Action 發生如何通知、更新 state  
  
C) 設計使用者第一次、第二次、第三次的使用經驗 or Magic Moment or Growth Hacking，讓使用者接受並上手你的新設計、解決他們的問題  
  
[It’s murmur time.]  
上面這個線性流程是為了說明而簡化的，實際上會是iterative、一直跳來跳去，會有很多的溝通、觀察和實驗，爛掉就要回去改原來的假設。修正各步驟的錯誤的損失是不同的，修正一個「傳達」的錯誤可能是幾個小時、修正一個「實作」的錯誤可能是一天、修正一個「新設計」的錯誤可能是一週、修正一個「分析」的錯誤可能是兩週、修正一個「定義問題」的錯誤可能是三個月。分配 BASIC 各步驟的時間會決定專案完成的時間，有點像馬拉松配速一樣，B + A + S 的時間最好超過 50%。如果 B or A or S 的步驟有問題，但你卻沒有辦法參與解決，請認真「溝通這參與的問題」或換個工作。總之每一步都要確定他是functional的，要問自己為什麼要這樣做?這樣做可以解決什麼?真的嗎?證據是?  
  
延伸閱讀：  
關於 B1：通常使用者要你解的問題都不是真正問題。詳見Donald A.Norman的「設計的心理學」第六章  
關於 蘋果設計流程: google “apple 10 3 1”   
關於 I.render.2： google「local scope css」，Webpack設定可以參考 React toolbox  
關於 I.render.3： [React的文件](https://github.com/facebook/react/blob/0b29035484f428cb56e7e1c04a88f66ac020d1d4/docs/docs/10.8-pure-render-mixin.md)  
關於 C：詳見一個 FB 設計師 Juile Zhuo 的「[Design the beginning](https://medium.com/the-year-of-the-looking-glass/design-the-beginning-b8e61081ce42)」一文。  
關於[設計流程的歷史](http://www.slideshare.net/divonis/design-process-8340952)  

—
對一個問題的好設計會在商業模式可行、技術可行、滿足使用者需求這三個部份重疊的地方，所以要有好的設計最好什麼都懂一點 XD 前端工程師 ＝ 設計師找問題 + 工程師解決問題。
