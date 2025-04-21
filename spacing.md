```scss
$spacers: (
    0: 0,
    1: $spacer * 0.25,   // 4px
    2: $spacer * 0.5,    // 8px
    2-1: $spacer * 0.625,// 10px
    2-2: $spacer * 0.75, // 12px
    2-3: $spacer * 0.875,// 14px
    3: $spacer,          // 16px
    3-5: $spacer * 1.25, // 20px  
    4: $spacer * 1.5,    // 24px
    4-5: $spacer * 2.25, // 36px
    4-7-5: $spacer * 2.5,// 40px
    5: $spacer * 3,      // 48px
);
```
```scss
$font-sizes: (
    1: 2.5rem,   // 40px
    2: 2rem,     // 32px
    3: 1.75rem,  // 28px
    4: 1.5rem,   // 24px
    5: 1.25rem,  // 20px
    5-5: 1.125rem, // 18px（客製）
    6: 1rem,     // 16px
    7: 0.875rem, // 14px（客製）
    8: 0.75rem   // 12px（客製）
)
```
```less
project/
├── index.html
├── assets/
│   ├── css/
│   │   └── main.css            ← 編譯後的 CSS
│   └── scss/
│       ├── bootstrap/          ← 來自官網下載的 Bootstrap scss 原始碼
│       │   ├── _functions.scss
│       │   ├── _variables.scss
│       │   ├── _maps.scss
│       │   ├── _utilities.scss
│       │   └── ...（其餘原生 SCSS）
│       ├── utilities/          ← 自訂 utility 擴充區
│       │   ├── _spacing.scss   ← 自訂 spacing（ex: m-2-1, m-4-5）
│       │   ├── _font-size.scss ← 自訂字級（ex: fs-5-5）
│       │   └── _colors.scss    ← 品牌色、語意色（ex: bg-brand, text-accent）
│       ├── _utilities.scss     ← 統整並輸出 utilities（@include utilities(...)）
│       └── main.scss           ← 主匯入點，編譯成 main.css

```