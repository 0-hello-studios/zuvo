<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Zuvo — Financial Toolkit</title>
  <meta name="description" content="Free financial calculator, market analysis, and education toolkit. Budget, invest, plan military finances, and learn — all in one app.">
  <meta name="theme-color" content="#1a1a1e">
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>💰</text></svg>">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; }
    #root { min-height: 100vh; }
  </style>
</head>
<body>
  <div id="root"></div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.9/babel.min.js"></script>
  <script type="text/babel">
    const { useState, useCallback, useEffect, useRef } = React;

// ===================== THEMES =====================
const THEMES = {
  graphite: { name:"Graphite", bg:"#1a1a1e", surface:"#232328", surfaceHover:"#2a2a30", border:"#333338", borderLight:"#2a2a2f", text:"#e4e4e7", textSecondary:"#a1a1aa", textMuted:"#71717a", accent:"#ca9a2e", accentBg:"rgba(202,154,46,0.08)", accentBorder:"rgba(202,154,46,0.2)", accentText:"#d4a843", resultHighlight:"rgba(202,154,46,0.06)", resultHighlightBorder:"rgba(202,154,46,0.15)", resultHighlightText:"#d4a843", inputBg:"#1a1a1e", inputBorder:"#3f3f46", tipBg:"rgba(202,154,46,0.04)", tipBorder:"rgba(202,154,46,0.12)", tipText:"#c4942a", sidebarActive:"rgba(202,154,46,0.08)", sidebarActiveText:"#d4a843", headerBg:"#18181b", green:"#6abf7b", red:"#e05555", blue:"#6b8afd", purple:"#a78bfa", orange:"#d48a4c" },
  midnight: { name:"Midnight", bg:"#0f1117", surface:"#181a22", surfaceHover:"#1e2130", border:"#262a38", borderLight:"#1f2333", text:"#e2e4eb", textSecondary:"#8b90a0", textMuted:"#5c6178", accent:"#6b8afd", accentBg:"rgba(107,138,253,0.08)", accentBorder:"rgba(107,138,253,0.2)", accentText:"#7d9aff", resultHighlight:"rgba(107,138,253,0.06)", resultHighlightBorder:"rgba(107,138,253,0.15)", resultHighlightText:"#7d9aff", inputBg:"#0f1117", inputBorder:"#2e3348", tipBg:"rgba(107,138,253,0.04)", tipBorder:"rgba(107,138,253,0.1)", tipText:"#6b8afd", sidebarActive:"rgba(107,138,253,0.08)", sidebarActiveText:"#7d9aff", headerBg:"#0c0e14", green:"#4ade80", red:"#f87171", blue:"#6b8afd", purple:"#a78bfa", orange:"#fb923c" },
  paper: { name:"Paper", bg:"#f5f4f0", surface:"#ffffff", surfaceHover:"#fafaf8", border:"#e2e0da", borderLight:"#eae8e3", text:"#1c1c1a", textSecondary:"#6b6b66", textMuted:"#9c9c96", accent:"#8b6914", accentBg:"rgba(139,105,20,0.06)", accentBorder:"rgba(139,105,20,0.15)", accentText:"#7a5c10", resultHighlight:"rgba(139,105,20,0.05)", resultHighlightBorder:"rgba(139,105,20,0.12)", resultHighlightText:"#7a5c10", inputBg:"#ffffff", inputBorder:"#d4d2cc", tipBg:"rgba(139,105,20,0.04)", tipBorder:"rgba(139,105,20,0.1)", tipText:"#8b6914", sidebarActive:"rgba(139,105,20,0.06)", sidebarActiveText:"#7a5c10", headerBg:"#ffffff", green:"#16a34a", red:"#dc2626", blue:"#2563eb", purple:"#7c3aed", orange:"#c2410c" },
  moss: { name:"Moss", bg:"#151a16", surface:"#1c221e", surfaceHover:"#232a25", border:"#2e362f", borderLight:"#262e27", text:"#d8e0da", textSecondary:"#8fa094", textMuted:"#647068", accent:"#6abf7b", accentBg:"rgba(106,191,123,0.07)", accentBorder:"rgba(106,191,123,0.18)", accentText:"#72cc84", resultHighlight:"rgba(106,191,123,0.06)", resultHighlightBorder:"rgba(106,191,123,0.14)", resultHighlightText:"#6abf7b", inputBg:"#151a16", inputBorder:"#354038", tipBg:"rgba(106,191,123,0.04)", tipBorder:"rgba(106,191,123,0.1)", tipText:"#6abf7b", sidebarActive:"rgba(106,191,123,0.07)", sidebarActiveText:"#72cc84", headerBg:"#131813", green:"#6abf7b", red:"#e05555", blue:"#6b9fff", purple:"#a78bfa", orange:"#d48a4c" },
  slate: { name:"Slate", bg:"#f8f9fa", surface:"#ffffff", surfaceHover:"#f1f3f5", border:"#dee2e6", borderLight:"#e9ecef", text:"#212529", textSecondary:"#6c757d", textMuted:"#adb5bd", accent:"#495057", accentBg:"rgba(73,80,87,0.05)", accentBorder:"rgba(73,80,87,0.15)", accentText:"#343a40", resultHighlight:"rgba(73,80,87,0.04)", resultHighlightBorder:"rgba(73,80,87,0.12)", resultHighlightText:"#212529", inputBg:"#ffffff", inputBorder:"#ced4da", tipBg:"rgba(73,80,87,0.03)", tipBorder:"rgba(73,80,87,0.1)", tipText:"#495057", sidebarActive:"rgba(73,80,87,0.06)", sidebarActiveText:"#212529", headerBg:"#ffffff", green:"#198754", red:"#dc3545", blue:"#0d6efd", purple:"#6f42c1", orange:"#fd7e14" },
  ember: { name:"Ember", bg:"#1a1614", surface:"#231f1c", surfaceHover:"#2c2724", border:"#3a3330", borderLight:"#302a27", text:"#e8e0da", textSecondary:"#a89888", textMuted:"#786858", accent:"#d48a4c", accentBg:"rgba(212,138,76,0.07)", accentBorder:"rgba(212,138,76,0.18)", accentText:"#dc9458", resultHighlight:"rgba(212,138,76,0.06)", resultHighlightBorder:"rgba(212,138,76,0.14)", resultHighlightText:"#d48a4c", inputBg:"#1a1614", inputBorder:"#443c38", tipBg:"rgba(212,138,76,0.04)", tipBorder:"rgba(212,138,76,0.1)", tipText:"#d48a4c", sidebarActive:"rgba(212,138,76,0.07)", sidebarActiveText:"#dc9458", headerBg:"#171412", green:"#6abf7b", red:"#e05555", blue:"#6b8afd", purple:"#c084fc", orange:"#d48a4c" },
};

// ===================== BUSINESS CALCULATORS =====================
const BIZ_CALCS = {
  profit_margin: { name:"Profit Margin", category:"Profitability", description:"Calculate profit margin from revenue and costs",
    fields:[{key:"revenue",label:"Revenue",prefix:"$",placeholder:"10000"},{key:"cost",label:"Cost of Goods / Expenses",prefix:"$",placeholder:"6000"}],
    calculate:(v)=>{const rev=parseFloat(v.revenue)||0,cost=parseFloat(v.cost)||0,profit=rev-cost,margin=rev>0?(profit/rev)*100:0,markup=cost>0?(profit/cost)*100:0;return[{label:"Gross Profit",value:`$${profit.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:profit>0},{label:"Profit Margin",value:`${margin.toFixed(1)}%`,highlight:margin>0},{label:"Markup",value:`${markup.toFixed(1)}%`}]},
    tip:"Margin is profit as % of revenue. Markup is profit as % of cost. 50% markup = 33.3% margin."
  },
  markup_margin: { name:"Markup / Margin", category:"Profitability", description:"Convert between markup and margin",
    fields:[{key:"value",label:"Enter Markup or Margin %",suffix:"%",placeholder:"50"}],
    calculate:(v)=>{const val=parseFloat(v.value)||0,p=val/100;return[{label:`If ${val}% is Markup → Margin`,value:`${(p/(1+p)*100).toFixed(2)}%`},{label:`If ${val}% is Margin → Markup`,value:`${isFinite(p/(1-p)*100)?(p/(1-p)*100).toFixed(2):"∞"}%`}]},
    tip:"50% markup ≠ 50% margin. Markup is based on cost, margin on selling price."
  },
  sales_tax: { name:"Sales Tax", category:"Tax", description:"Calculate sales tax forward and reverse",
    fields:[{key:"amount",label:"Amount",prefix:"$",placeholder:"99.99"},{key:"rate",label:"Tax Rate",suffix:"%",placeholder:"7.25"}],
    calculate:(v)=>{const a=parseFloat(v.amount)||0,r=(parseFloat(v.rate)||0)/100,tax=a*r;return[{label:"Tax Amount",value:`$${tax.toFixed(2)}`},{label:"Total with Tax",value:`$${(a+tax).toFixed(2)}`,highlight:true},{label:"If amount includes tax:",value:"",divider:true},{label:"Pre-tax Price",value:`$${(a/(1+r)).toFixed(2)}`},{label:"Tax Portion",value:`$${(a-a/(1+r)).toFixed(2)}`}]},
    tip:"Both directions shown. Enter pre-tax to see total, or tax-inclusive to see breakdown."
  },
  quarterly_tax: { name:"Quarterly Tax", category:"Tax", description:"Estimate quarterly tax payments",
    fields:[{key:"annual",label:"Annual Income",prefix:"$",placeholder:"75000"},{key:"expenses",label:"Deductible Expenses",prefix:"$",placeholder:"15000"},{key:"filing",label:"Effective Tax Rate",suffix:"%",placeholder:"22"},{key:"se_tax",label:"Self-Employment Tax (15.3%)",type:"toggle"}],
    calculate:(v)=>{const inc=parseFloat(v.annual)||0,exp=parseFloat(v.expenses)||0,taxable=Math.max(0,inc-exp),rate=(parseFloat(v.filing)||22)/100,se=v.se_tax?taxable*0.153:0,itax=taxable*rate,total=itax+se;return[{label:"Taxable Income",value:`$${taxable.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`},{label:"Income Tax",value:`$${itax.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`},...(v.se_tax?[{label:"SE Tax",value:`$${se.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`}]:[]),{label:"Annual Total",value:`$${total.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`},{label:"Quarterly Payment",value:`$${(total/4).toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true},{label:"Set Aside Monthly",value:`$${(total/12).toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true}]},
    tip:"Quarterly deadlines: Apr 15, Jun 15, Sep 15, Jan 15. Late = penalties."
  },
  breakeven: { name:"Break-Even", category:"Business", description:"Units and revenue needed to break even",
    fields:[{key:"fixed",label:"Fixed Costs",prefix:"$",placeholder:"3000"},{key:"price",label:"Price Per Unit",prefix:"$",placeholder:"50"},{key:"variable",label:"Variable Cost Per Unit",prefix:"$",placeholder:"20"}],
    calculate:(v)=>{const f=parseFloat(v.fixed)||0,p=parseFloat(v.price)||0,vc=parseFloat(v.variable)||0,c=p-vc,u=c>0?Math.ceil(f/c):0;return[{label:"Contribution Per Unit",value:`$${c.toFixed(2)}`},{label:"Contribution Margin",value:`${p>0?(c/p*100).toFixed(1):0}%`},{label:"Units to Break Even",value:u.toLocaleString(),highlight:true},{label:"Revenue to Break Even",value:`$${(u*p).toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true}]},
    tip:"Higher contribution margin = fewer sales needed to cover fixed costs."
  },
  payroll: { name:"Payroll", category:"Business", description:"Estimate net pay from gross",
    fields:[{key:"gross",label:"Gross Pay",prefix:"$",placeholder:"5000"},{key:"federal",label:"Federal Rate",suffix:"%",placeholder:"22"},{key:"state",label:"State Rate",suffix:"%",placeholder:"5"},{key:"period",label:"Pay Period",type:"select",options:["Monthly","Bi-weekly","Weekly"]}],
    calculate:(v)=>{const g=parseFloat(v.gross)||0,fed=g*(parseFloat(v.federal)||0)/100,st=g*(parseFloat(v.state)||0)/100,ss=g*0.062,med=g*0.0145,tot=fed+st+ss+med,net=g-tot,per=v.period==="Weekly"?52:v.period==="Bi-weekly"?26:12;return[{label:"Federal Tax",value:`-$${fed.toFixed(2)}`},{label:"State Tax",value:`-$${st.toFixed(2)}`},{label:"Social Security",value:`-$${ss.toFixed(2)}`},{label:"Medicare",value:`-$${med.toFixed(2)}`},{label:"Total Deductions",value:`-$${tot.toFixed(2)}`},{label:"Net Pay",value:`$${net.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true},{label:"Annual Net",value:`$${(net*per).toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`}]},
    tip:"Ballpark only. Real payroll includes 401k, health insurance, and other pre-tax deductions."
  },
  mileage: { name:"Mileage Deduction", category:"Tax", description:"IRS standard mileage deduction",
    fields:[{key:"miles",label:"Business Miles",placeholder:"12000"},{key:"rate",label:"Rate (cents/mi)",placeholder:"70",suffix:"¢"}],
    calculate:(v)=>{const m=parseFloat(v.miles)||0,r=(parseFloat(v.rate)||70)/100,d=m*r;return[{label:"Total Deduction",value:`$${d.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true},{label:"Tax Saved (22%)",value:`$${(d*0.22).toFixed(2)}`},{label:"Tax Saved (32%)",value:`$${(d*0.32).toFixed(2)}`}]},
    tip:"Keep a mileage log. IRS requires documentation."
  },
  depreciation: { name:"Depreciation", category:"Business", description:"Straight-line depreciation",
    fields:[{key:"cost",label:"Asset Cost",prefix:"$",placeholder:"25000"},{key:"salvage",label:"Salvage Value",prefix:"$",placeholder:"5000"},{key:"life",label:"Useful Life (years)",placeholder:"5"}],
    calculate:(v)=>{const c=parseFloat(v.cost)||0,s=parseFloat(v.salvage)||0,l=parseFloat(v.life)||1,d=c-s,a=d/l;return[{label:"Depreciable Amount",value:`$${d.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`},{label:"Annual",value:`$${a.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`,highlight:true},{label:"Monthly",value:`$${(a/12).toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`},{label:"Rate",value:`${c>0?(a/c*100).toFixed(1):0}%/yr`}]},
    tip:"Straight-line is simplest. MACRS may allow faster write-offs."
  },
  invoice: { name:"Invoice Builder", category:"Business", description:"Subtotal + discount + tax",
    fields:[{key:"subtotal",label:"Subtotal",prefix:"$",placeholder:"1500"},{key:"discount",label:"Discount",suffix:"%",placeholder:"10"},{key:"tax_rate",label:"Tax Rate",suffix:"%",placeholder:"7.25"}],
    calculate:(v)=>{const s=parseFloat(v.subtotal)||0,d=(parseFloat(v.discount)||0)/100,tx=(parseFloat(v.tax_rate)||0)/100,da=s*d,af=s-da,ta=af*tx;return[{label:"Subtotal",value:`$${s.toFixed(2)}`},...(d>0?[{label:`Discount (${(d*100).toFixed(0)}%)`,value:`-$${da.toFixed(2)}`},{label:"After Discount",value:`$${af.toFixed(2)}`}]:[]),{label:`Tax (${(tx*100).toFixed(2)}%)`,value:`$${ta.toFixed(2)}`},{label:"Total Due",value:`$${(af+ta).toFixed(2)}`,highlight:true}]},
    tip:"Discount applies before tax. Standard accounting practice."
  },
  hourly_rate: { name:"Hourly Rate Finder", category:"Profitability", description:"Find your rate from income goals",
    fields:[{key:"target",label:"Target Annual Income",prefix:"$",placeholder:"80000"},{key:"hours",label:"Billable Hrs/Week",placeholder:"30"},{key:"weeks",label:"Weeks/Year",placeholder:"48"},{key:"expenses",label:"Annual Expenses",prefix:"$",placeholder:"12000"}],
    calculate:(v)=>{const t=parseFloat(v.target)||0,h=parseFloat(v.hours)||1,w=parseFloat(v.weeks)||1,e=parseFloat(v.expenses)||0,tax=t*0.3,need=t+tax+e,th=h*w;return[{label:"Gross Needed (inc. ~30% tax)",value:`$${(t+tax).toLocaleString("en-US",{maximumFractionDigits:0})}`},{label:"Plus Expenses",value:`$${e.toLocaleString("en-US",{maximumFractionDigits:0})}`},{label:"Revenue Needed",value:`$${need.toLocaleString("en-US",{maximumFractionDigits:0})}`},{label:"Billable Hours/Year",value:`${th.toLocaleString()} hrs`},{label:"Minimum Rate",value:`$${(need/th).toFixed(2)}/hr`,highlight:true}]},
    tip:"Most freelancers only bill 60-70% of working hours. Factor that in."
  },
};

const BIZ_CATEGORIES = ["All","Profitability","Tax","Business"];

// ===================== STRATEGIES =====================
const STRATEGIES = [
  { id:"macd",name:"MACD",fullName:"Moving Average Convergence Divergence",difficulty:"Intermediate",timeframe:"Swing / Position",
    description:"Measures the relationship between two EMAs to identify momentum shifts and trend direction.",
    signals:["MACD crosses above Signal → Bullish","MACD crosses below Signal → Bearish","Histogram growing → Momentum increasing","Histogram shrinking → Momentum fading","Divergence with price → Trend weakening"],
    settings:"12-period EMA, 26-period EMA, 9-period Signal",bestFor:"Trend changes and momentum in trending markets.",
    proTip:"Combine with support/resistance or RSI for confirmation. False signals common in ranging markets." },
  { id:"rsi",name:"RSI",fullName:"Relative Strength Index",difficulty:"Beginner",timeframe:"Day / Swing",
    description:"Measures speed and magnitude of price changes on a 0-100 scale to identify overbought/oversold conditions.",
    signals:["Above 70 → Overbought, may pull back","Below 30 → Oversold, may bounce","Crossing 50 upward → Bullish shift","Crossing 50 downward → Bearish shift","Divergence with price → Reversal warning"],
    settings:"14-period default. 9 for sensitive, 21 for smooth.",bestFor:"Spotting reversals and confirming trend strength.",
    proTip:"In strong uptrends RSI can stay above 70 for extended periods. Context matters." },
  { id:"bollinger",name:"Bollinger Bands",fullName:"Bollinger Bands",difficulty:"Intermediate",timeframe:"Day / Swing",
    description:"Plots a moving average with upper/lower bands based on standard deviation. Expands in high volatility, contracts in low.",
    signals:["Price at upper band → Potentially overbought","Price at lower band → Potentially oversold","Squeeze (narrow bands) → Big move coming","Riding upper band → Strong uptrend","W-bottom at lower band → Buy signal"],
    settings:"20-period SMA, 2 standard deviations.",bestFor:"Measuring volatility and identifying breakouts.",
    proTip:"Squeeze is the most powerful signal but won't tell you direction. Use volume to confirm." },
  { id:"sma",name:"Moving Averages",fullName:"Simple & Exponential Moving Averages",difficulty:"Beginner",timeframe:"All",
    description:"Smooth price data to show underlying trend. SMA weights equally, EMA weights recent prices more.",
    signals:["Price above MA → Bullish","Price below MA → Bearish","Golden Cross (50 above 200) → Major bullish","Death Cross (50 below 200) → Major bearish","MA as support/resistance → Trend confirmation"],
    settings:"Common: 10, 20, 50, 100, 200 period.",bestFor:"Foundation of technical analysis. Learn this first.",
    proTip:"The 200-day MA is watched by institutions globally. Price near it always gets a reaction." },
  { id:"volume",name:"Volume Analysis",fullName:"Volume & On-Balance Volume",difficulty:"Beginner",timeframe:"All",
    description:"Shows trading conviction behind price moves. OBV tracks cumulative volume flow.",
    signals:["Price up + Volume up → Strong continuation","Price up + Volume down → Weak, possible reversal","Volume spike on breakout → Confirms breakout","OBV rising, price flat → Accumulation","OBV falling, price flat → Distribution"],
    settings:"No settings. Overlay volume bars on chart.",bestFor:"Confirming every other signal. The truth detector.",
    proTip:"Never trust a breakout on low volume. Best breakouts come with 2-3x average volume." },
  { id:"fibonacci",name:"Fibonacci",fullName:"Fibonacci Retracement Levels",difficulty:"Advanced",timeframe:"Swing / Position",
    description:"Uses mathematical ratios (23.6%, 38.2%, 50%, 61.8%) to identify support/resistance during pullbacks.",
    signals:["38.2% retracement → Shallow pullback, strong trend","50% → Healthy correction","61.8% (Golden Ratio) → Last defense for trend","Bounce at Fib + confirmation → High-probability entry","Break through 61.8% → Trend likely over"],
    settings:"Levels: 23.6%, 38.2%, 50%, 61.8%, 78.6%. Extensions: 127.2%, 161.8%.",bestFor:"Precise entries during pullbacks in trending markets.",
    proTip:"61.8% is the most important level. Use it as your line in the sand." },
  { id:"vwap",name:"VWAP",fullName:"Volume Weighted Average Price",difficulty:"Intermediate",timeframe:"Day",
    description:"The average price weighted by volume throughout the day. Institutional traders use it as a benchmark — if they buy below VWAP, they got a good deal.",
    signals:["Price above VWAP → Bullish intraday bias","Price below VWAP → Bearish intraday bias","Price bouncing off VWAP → Support/resistance confirmation","Crossing VWAP with volume → Trend shift","Far from VWAP → Stretched, may revert"],
    settings:"Resets daily. Some use anchored VWAP from specific dates.",bestFor:"Day trading entries and exits. Knowing if you're buying cheap or expensive relative to the day.",
    proTip:"VWAP is most useful in the first and last hours of trading. Mid-day it flattens out and loses power." },
  { id:"stochastic",name:"Stochastic",fullName:"Stochastic Oscillator",difficulty:"Intermediate",timeframe:"Day / Swing",
    description:"Compares closing price to the price range over a period. Shows momentum on a 0-100 scale, similar to RSI but more sensitive to price action.",
    signals:["Above 80 → Overbought zone","Below 20 → Oversold zone","%K crosses above %D from below 20 → Buy signal","%K crosses below %D from above 80 → Sell signal","Divergence with price → Reversal coming"],
    settings:"Default: %K=14, %D=3, slowing=3. Fast stochastic uses raw values.",bestFor:"Short-term momentum and timing entries in ranging markets.",
    proTip:"Stochastic gives many false signals in trending markets. Best used in sideways/range-bound conditions." },
  { id:"atr",name:"ATR",fullName:"Average True Range",difficulty:"Beginner",timeframe:"All",
    description:"Measures volatility by averaging the true range (high-low including gaps) over a period. Doesn't indicate direction — just how much price is moving.",
    signals:["Rising ATR → Volatility increasing, bigger moves","Falling ATR → Volatility decreasing, consolidation","High ATR after trend → Possible exhaustion","Low ATR before breakout → Explosive move building","Use ATR for stop-loss placement → 1.5-2x ATR below entry"],
    settings:"Default: 14 periods. Lower for short-term, higher for long-term.",bestFor:"Setting stop-losses and position sizing. Knowing when to expect big vs small moves.",
    proTip:"ATR is the best tool for stop-loss placement. A stop at 2x ATR gives your trade room to breathe without getting stopped out by normal noise." },
  { id:"ichimoku",name:"Ichimoku Cloud",fullName:"Ichimoku Kinko Hyo",difficulty:"Advanced",timeframe:"Swing / Position",
    description:"A comprehensive indicator system that shows support/resistance, trend direction, momentum, and future levels all in one view. The cloud (kumo) is the key feature.",
    signals:["Price above cloud → Bullish","Price below cloud → Bearish","Cloud color change → Trend reversal","Tenkan crosses Kijun above cloud → Strong buy","Price in cloud → Consolidation, no clear trend"],
    settings:"Default: Tenkan=9, Kijun=26, Senkou B=52, displacement=26.",bestFor:"Full picture analysis. One indicator that replaces several others.",
    proTip:"Ichimoku was designed for weekly charts. On daily or lower timeframes, consider adjusting to 7/22/44 for faster signals." },
  { id:"support_resistance",name:"Support / Resistance",fullName:"Support & Resistance Levels",difficulty:"Beginner",timeframe:"All",
    description:"Horizontal price levels where buying (support) or selling (resistance) consistently occurs. The most fundamental concept in technical analysis — price has memory.",
    signals:["Price bounces off support → Buy opportunity","Price rejects at resistance → Sell/short opportunity","Support breaks → Becomes new resistance","Resistance breaks → Becomes new support","Multiple tests of a level → Stronger level"],
    settings:"Draw horizontal lines at swing highs/lows. Look for areas with multiple touches.",bestFor:"Every trading style. These are the levels where the most important decisions happen.",
    proTip:"Round numbers ($50, $100, $500) are natural support/resistance because humans think in round numbers. Institutions place orders there." },
  { id:"candlestick",name:"Candlestick Patterns",fullName:"Japanese Candlestick Patterns",difficulty:"Intermediate",timeframe:"All",
    description:"Price action patterns formed by one or more candles that suggest continuation or reversal. Each candle shows open, high, low, and close.",
    signals:["Hammer at support → Bullish reversal","Shooting star at resistance → Bearish reversal","Engulfing pattern → Strong reversal signal","Doji → Indecision, look for next candle","Three white soldiers / black crows → Strong trend"],
    settings:"No indicator settings. Read price action directly from the chart.",bestFor:"Timing entries and exits without any indicators. Pure price reading.",
    proTip:"Never trade a candlestick pattern in isolation. A hammer at a key support level with rising volume is 10x more reliable than a random hammer." },
  { id:"dca",name:"DCA Strategy",fullName:"Dollar-Cost Averaging",difficulty:"Beginner",timeframe:"Long-Term",
    description:"Investing a fixed amount at regular intervals regardless of price. You buy more shares when price is low, fewer when high. Removes emotion and timing from investing.",
    signals:["Set a schedule (weekly/monthly) and stick to it","Market dips → You naturally buy more shares","Market highs → You buy fewer shares, reduces risk","Consistency beats timing → Data proves this repeatedly","Works best with index funds and ETFs"],
    settings:"Choose your amount, frequency (weekly/bi-weekly/monthly), and asset. Automate it.",bestFor:"Long-term wealth building. The strategy that requires the least skill and beats most active traders.",
    proTip:"DCA into an S&P 500 index fund has historically returned ~10% annually. Over 20 years, $500/mo becomes $380k+. Start early, stay consistent." },
];

const LEARN_TOPICS = [
  // === Market / Technical (reuse STRATEGIES ids) ===
  ...STRATEGIES.map(s=>({...s,category:"Market"})),
  // === Budgeting ===
  {id:"50_30_20",name:"50/30/20 Rule",fullName:"The 50/30/20 Budget Framework",difficulty:"Beginner",category:"Budgeting",timeframe:"Monthly",
    description:"Split your after-tax income into three buckets: 50% needs (rent, food, insurance), 30% wants (dining, entertainment, subscriptions), and 20% savings & debt payoff.",
    signals:["Calculate take-home pay first","List all fixed needs → should be ≤50%","Wants are negotiable → cap at 30%","Savings includes investments + extra debt payments","If needs exceed 50% → reduce or earn more"],
    settings:"Works with any income level. Adjust percentages based on goals — FIRE savers might do 50/20/30.",bestFor:"People starting their first budget. Simple enough to stick with.",
    proTip:"The 20% savings is the minimum. Every percent above 20% accelerates your timeline to financial independence exponentially."},
  {id:"emergency_fund",name:"Emergency Fund",fullName:"Building Your Emergency Fund",difficulty:"Beginner",category:"Budgeting",timeframe:"3-6 Months",
    description:"Cash reserve covering 3-6 months of expenses in a high-yield savings account. This is the foundation — without it, one car repair or medical bill can spiral into debt.",
    signals:["Start with $1,000 mini emergency fund","Then build to 1 month expenses","Target 3 months (stable job) or 6 months (variable income)","Keep in HYSA earning 4-5% APY","Never invest your emergency fund"],
    settings:"Monthly expenses × target months. $2,000/mo expenses × 6 months = $12,000 target.",bestFor:"Everyone. This is step one before investing, before debt payoff, before everything.",
    proTip:"Automate $50-200/paycheck into a separate HYSA. Don't touch it. When you need it, you'll be thankful it's boring and liquid."},
  {id:"pay_yourself_first",name:"Pay Yourself First",fullName:"Automated Savings Strategy",difficulty:"Beginner",category:"Budgeting",timeframe:"Per Paycheck",
    description:"On payday, automatically move money to savings and investments before spending on anything. What's left is what you live on. Reverses the typical spend-then-save pattern.",
    signals:["Set up auto-transfer on payday","Savings/investments leave your account immediately","Live on what remains","Increase the amount by 1% every raise","Separate accounts for separate goals"],
    settings:"Start with 10-15% of gross income. Increase 1% every 6 months until it hurts.",bestFor:"People who 'never have money left to save.' This fixes that by removing the choice.",
    proTip:"Open a separate bank for savings. Out of sight, out of mind. The friction of transferring money back prevents impulse spending."},
  // === Debt ===
  {id:"avalanche",name:"Avalanche Method",fullName:"Debt Avalanche (Highest Interest First)",difficulty:"Intermediate",category:"Debt",timeframe:"Varies",
    description:"Pay minimums on all debts, then throw every extra dollar at the highest-interest debt. Mathematically optimal — saves the most money and time.",
    signals:["List all debts by interest rate (highest first)","Pay minimums on everything","All extra money → highest rate debt","When it's paid off → roll payment to next highest","Repeat until debt-free"],
    settings:"Need: all balances, interest rates, minimum payments, and your total monthly debt budget.",bestFor:"People motivated by math and saving money. Best for high-interest debt like credit cards.",
    proTip:"Credit card debt at 20%+ APR is a financial emergency. No investment reliably returns 20%. Pay this off before investing beyond employer match."},
  {id:"snowball",name:"Snowball Method",fullName:"Debt Snowball (Smallest Balance First)",difficulty:"Beginner",category:"Debt",timeframe:"Varies",
    description:"Pay minimums on all debts, throw extra at the smallest balance. Quick wins build momentum. Costs slightly more than avalanche but the psychological boost keeps people going.",
    signals:["List all debts by balance (smallest first)","Pay minimums on everything","All extra money → smallest balance","Celebrate each payoff → momentum builds","Roll freed payment into next debt"],
    settings:"Same info as avalanche. The difference is sort order — balance vs interest rate.",bestFor:"People with many small debts who need motivation. The quick wins are real.",
    proTip:"Dave Ramsey popularized this. It works because personal finance is 80% behavior. A mathematically inferior plan you stick with beats a perfect plan you quit."},
  {id:"good_vs_bad_debt",name:"Good vs Bad Debt",fullName:"Understanding Debt Quality",difficulty:"Beginner",category:"Debt",timeframe:"Concept",
    description:"Not all debt is equal. Good debt builds wealth (mortgage, education, business loans at low rates). Bad debt destroys it (credit cards, car loans on depreciating assets, payday loans).",
    signals:["Under 5% interest + builds equity → Generally good","Over 10% interest → Almost always bad","Appreciating asset backing → Good sign","Depreciating asset → Bad sign","If it makes you money → Potentially good leverage"],
    settings:"Rule of thumb: if the interest rate is lower than expected investment returns (~7-10%), the debt may be worth keeping.",bestFor:"Everyone making debt decisions. Helps prioritize what to pay off vs keep.",
    proTip:"A 3% mortgage while investing at 10% is smart leverage. A 24% credit card balance while investing is insanity. Rate comparison is everything."},
  // === Tax ===
  {id:"tax_brackets",name:"Tax Brackets",fullName:"How Marginal Tax Brackets Work",difficulty:"Beginner",category:"Tax",timeframe:"Annual",
    description:"You don't pay one rate on all income. Each bracket only applies to the income within that range. Being 'in the 22% bracket' means only income above $44,725 is taxed at 22%.",
    signals:["First $11,600 → 10% ($1,160 tax)","$11,601-$47,150 → 12%","$47,151-$100,525 → 22%","$100,526-$191,950 → 24%","Your effective rate is always lower than your bracket"],
    settings:"2024 single filer brackets. Married filing jointly gets wider brackets (roughly 2x).",bestFor:"Everyone who pays taxes. Most people misunderstand this and overpay as a result.",
    proTip:"Earning $1 more never costs you money. A raise that pushes you into a higher bracket only taxes the extra income at the new rate, not all of it."},
  {id:"self_employment_tax",name:"Self-Employment Tax",fullName:"SE Tax for Freelancers & Side Hustles",difficulty:"Intermediate",category:"Tax",timeframe:"Quarterly",
    description:"When you're your own boss, you pay both the employee AND employer share of Social Security + Medicare: 15.3% on top of income tax. This is the tax that surprises new freelancers.",
    signals:["15.3% on first $168,600 of SE income (2024)","2.9% Medicare above that (no cap)","Deduct half of SE tax from gross income","Pay quarterly estimates or face penalties","Track ALL business expenses to reduce SE income"],
    settings:"SE tax = net SE income × 0.9235 × 0.153. The 0.9235 factor simulates the employer deduction.",bestFor:"Freelancers, Roblox devs, anyone with 1099 income or side hustle revenue.",
    proTip:"An S-Corp election can save thousands in SE tax if you earn $50k+ from self-employment. Pay yourself a 'reasonable salary' and take the rest as distributions (no SE tax on distributions)."},
  // === Military ===
  {id:"bah_arbitrage",name:"BAH Arbitrage",fullName:"Profiting from Housing Allowance",difficulty:"Beginner",category:"Military",timeframe:"Monthly",
    description:"BAH is based on average housing costs in your area, but you can pocket the difference by living below that average. Live in barracks, with roommates, or in cheaper housing and keep the tax-free surplus.",
    signals:["BAH is tax-free → $2,000 BAH = $2,600+ pre-tax value","Barracks = $0 housing → keep 100% of implicit BAH savings","Roommate splits → keep 40-60% of BAH","Stealth camping → keep nearly all BAH","Difference goes straight to investments"],
    settings:"Check BAH rates at militarybenefits.info for your rank and duty station.",bestFor:"Single E-1 through E-6 who can tolerate basic living. The savings compound dramatically.",
    proTip:"An E-5 in San Diego getting $2,350 BAH who lives with a roommate for $900 pockets $1,450/mo tax-free. That's $17,400/year straight to TSP."},
  {id:"tsp_strategy",name:"TSP Strategy",fullName:"Thrift Savings Plan Optimization",difficulty:"Beginner",category:"Military",timeframe:"Career-Long",
    description:"The TSP is the military 401k with the lowest fees in existence (0.043%). DoD matches up to 5% of base pay. The C Fund tracks the S&P 500, the S Fund tracks small caps, the I Fund tracks international.",
    signals:["Always contribute at least 5% → Get the full match","Roth TSP if in low tax bracket → Tax-free growth","C Fund = S&P 500 → Default good choice","80/20 C/S split → Aggressive growth strategy","Increase contribution 1% every promotion"],
    settings:"Max contribution: $23,000/year (2024). Match: 1% auto + up to 4% matching = 5% free money.",bestFor:"Every service member. This is the #1 wealth-building tool in the military.",
    proTip:"An E-3 contributing 15% to Roth TSP from age 18 will have $1M+ by 40 assuming 10% returns. The earlier you start, the less you need to contribute."},
  {id:"gi_bill_mha",name:"GI Bill + MHA",fullName:"Maximizing Education Benefits",difficulty:"Intermediate",category:"Military",timeframe:"36 Months",
    description:"Post-9/11 GI Bill covers tuition + a Monthly Housing Allowance (MHA) equal to E-5 BAH at the school's zip code. This means you get paid to go to school — and the zip code matters enormously.",
    signals:["Full tuition covered at public universities","MHA = E-5 BAH rate at school zip code","San Francisco MHA ≈ $4,500/mo vs rural ≈ $1,200/mo","Online-only = 50% of national average MHA","Yellow Ribbon covers private school gaps"],
    settings:"36 months of benefits. Can be used part-time (extends duration). Must be enrolled more than half-time for MHA.",bestFor:"Veterans planning education. Location choice alone can mean $100k+ difference in total benefits.",
    proTip:"Attend school in an expensive zip code, live somewhere cheap nearby. A school in SF paying $4,500 MHA while you rent a room for $1,200 nets you $3,300/mo tax-free."},
  // === Retirement ===
  {id:"fire_movement",name:"FIRE",fullName:"Financial Independence, Retire Early",difficulty:"Intermediate",category:"Retirement",timeframe:"10-20 Years",
    description:"Save 50-70% of income aggressively, invest in index funds, and retire when your portfolio hits 25x annual expenses (the 4% rule). Not about being frugal forever — about buying your freedom.",
    signals:["Calculate annual expenses → multiply by 25 = your FIRE number","Save 50%+ of income → accelerates timeline","Invest in low-cost index funds → keep it simple","Track savings rate monthly → most important metric","Coast FIRE = enough invested that compounding handles retirement"],
    settings:"$40k/year expenses × 25 = $1M FIRE number. $60k × 25 = $1.5M.",bestFor:"Anyone who values time freedom over lifestyle inflation. Military members have a huge advantage here.",
    proTip:"Barista FIRE: save enough that you only need part-time income to cover expenses while investments grow. Much more achievable than full FIRE for most people."},
  {id:"roth_vs_traditional",name:"Roth vs Traditional",fullName:"Roth vs Traditional Retirement Accounts",difficulty:"Intermediate",category:"Retirement",timeframe:"Career-Long",
    description:"Traditional: tax deduction now, pay taxes in retirement. Roth: pay taxes now, never again. The core question: will you be in a higher tax bracket now or in retirement?",
    signals:["Low income now → Roth (pay low taxes now, withdraw tax-free later)","High income now → Traditional (deduction worth more now)","Military enlisted → Almost always Roth (low taxable income)","Roth contributions withdraw penalty-free anytime","Traditional forces withdrawals at 73 (RMDs)"],
    settings:"2024 IRA limit: $7,000. 401k/TSP limit: $23,000. Can split between Roth and Traditional.",bestFor:"Everyone choosing between account types. Getting this right over a career saves six figures.",
    proTip:"Military members in combat zones pay ZERO income tax. Max out Roth TSP during deployments — you're putting in tax-free money that grows and withdraws tax-free. Triple tax benefit."},
  // === Real Estate ===
  {id:"house_hacking",name:"House Hacking",fullName:"Live-In Real Estate Investing",difficulty:"Beginner",category:"Real Estate",timeframe:"2-5 Years",
    description:"Buy a duplex/triplex/fourplex, live in one unit, rent the others. Tenants cover your mortgage while you build equity. The single best first move in real estate investing.",
    signals:["FHA loan → 3.5% down on up to 4 units","VA loan → 0% down on up to 4 units","Rental income covers 50-100% of mortgage","Live there 1 year → then rent your unit too","Repeat → buy another property every 1-2 years"],
    settings:"Target: rental income ≥ mortgage payment. Even 80% coverage means drastically reduced housing costs.",bestFor:"First-time investors, military members with VA loans. Lowest barrier to entry in real estate.",
    proTip:"A VA loan on a fourplex with 0% down where tenants cover the mortgage is the most powerful wealth-building move available to military members. Period."},
  {id:"rental_math",name:"Rental Math",fullName:"Analyzing Rental Property Returns",difficulty:"Intermediate",category:"Real Estate",timeframe:"Per Property",
    description:"The 1% rule, cap rate, and cash-on-cash return are the three numbers that matter. If a $200k property rents for $2,000/mo (1%), has a 6% cap rate, and returns 10% cash-on-cash, it's solid.",
    signals:["1% Rule → Monthly rent ≥ 1% of purchase price","Cap Rate → NOI ÷ price (aim for 5-8%)","Cash-on-Cash → Annual cash flow ÷ cash invested","50% Rule → Expect 50% of rent goes to expenses","DSCR → Rental income ÷ debt payments (want >1.25)"],
    settings:"NOI = gross rent - vacancy (8%) - management (10%) - repairs (10%) - insurance - taxes.",bestFor:"Evaluating whether a rental property is actually profitable or just looks good on paper.",
    proTip:"Most new investors underestimate expenses. Budget 50% of gross rent for vacancies, repairs, management, taxes, and insurance. If it still cash flows, it's a deal."},
  // === Crypto ===
  {id:"crypto_security",name:"Crypto Security",fullName:"Protecting Your Crypto Assets",difficulty:"Beginner",category:"Crypto",timeframe:"Ongoing",
    description:"Not your keys, not your coins. Exchanges get hacked, freeze withdrawals, and go bankrupt. A hardware wallet (cold storage) is the only way to truly own your crypto.",
    signals:["Exchange = convenience, not security","Hardware wallet for anything over $1,000","Never share seed phrase with anyone, ever","Use 2FA (authenticator app, not SMS)","Diversify across wallets for large holdings"],
    settings:"Top hardware wallets: Ledger Nano X, Trezor Model T. $70-200. Cheap insurance.",bestFor:"Anyone holding crypto they don't plan to trade daily. If you're HODLing, get it off the exchange.",
    proTip:"Write your seed phrase on metal (not paper) and store it in a fireproof safe. Paper burns. If you lose your seed phrase and your device breaks, your crypto is gone forever."},
  {id:"crypto_dca_strategy",name:"Crypto DCA",fullName:"Dollar-Cost Averaging into Crypto",difficulty:"Beginner",category:"Crypto",timeframe:"Weekly/Monthly",
    description:"Same as stock DCA but even more important for crypto due to extreme volatility. A fixed amount on a fixed schedule means you buy more when prices crash and less at peaks.",
    signals:["Set a fixed amount ($25-500/week)","Choose 1-3 assets (BTC + ETH is the default)","Automate through exchange recurring buys","Ignore daily price swings entirely","Review allocation quarterly, not daily"],
    settings:"Suggested allocation: 60% BTC, 30% ETH, 10% other. Adjust to your risk tolerance.",bestFor:"Long-term crypto believers who don't want to time the market. Statistically beats lump-sum in volatile assets.",
    proTip:"BTC DCA from any point in history, held for 4+ years, has never lost money. Time in market beats timing the market, especially in crypto."},
  // === Investing ===
  {id:"asset_allocation",name:"Asset Allocation",fullName:"Portfolio Diversification Strategy",difficulty:"Intermediate",category:"Investing",timeframe:"Career-Long",
    description:"How you split money between stocks, bonds, real estate, and cash. The single biggest factor in investment returns — more important than picking individual stocks.",
    signals:["Age in bonds rule → 120 minus age = stock %","Young + aggressive → 90-100% stocks is fine","Diversify across US, international, and bonds","Rebalance annually → sell winners, buy losers","Target-date funds do this automatically"],
    settings:"Aggressive: 80% stock / 20% bond. Moderate: 60/40. Conservative: 40/60.",bestFor:"Everyone with investment accounts. Get this right and individual stock picks barely matter.",
    proTip:"A three-fund portfolio (US total market + international + bonds) in the right ratio beats 90% of professional fund managers. Simplicity wins."},
  {id:"compound_power",name:"Compounding",fullName:"The Power of Compound Growth",difficulty:"Beginner",category:"Investing",timeframe:"Decades",
    description:"Interest earning interest. The 8th wonder of the world. $500/month at 10% annual return becomes $1.1M in 30 years — but only $200k of that is your money. The other $900k is pure compounding.",
    signals:["Start early → time is the #1 factor","$500/mo from 18-28 (10 yrs) beats $500/mo from 28-58 (30 yrs)","Rule of 72 → divide 72 by return rate = years to double","10% return → money doubles every 7.2 years","Never withdraw → let compounding work uninterrupted"],
    settings:"Rule of 72: 72 ÷ 10% = 7.2 years to double. 72 ÷ 7% = 10.3 years.",bestFor:"Young investors who think they don't have enough to start. Even $50/mo matters enormously over decades.",
    proTip:"An 18-year-old investing $200/mo into the S&P 500 will have more at 65 than a 30-year-old investing $500/mo. The 12-year head start is worth more than 2.5x the monthly contribution."},
  // === More Budgeting ===
  {id:"zero_based",name:"Zero-Based Budget",fullName:"Every Dollar Gets a Job",difficulty:"Intermediate",category:"Budgeting",timeframe:"Monthly",
    description:"Assign every dollar of income to a specific category until you hit $0 remaining. Income minus all allocations (bills, savings, fun) = zero. Nothing is unaccounted for.",
    signals:["List all income sources for the month","Assign every dollar to a category","Savings and investing are categories too","Adjust categories mid-month if needed","$0 remaining means the budget is complete"],
    settings:"Use the budget tab in this app or a simple spreadsheet. The key is accounting for literally every dollar.",bestFor:"People who leak money on 'I don't know where it went.' Forces intentionality with every dollar.",
    proTip:"Do this the weekend before each month. It takes 20 minutes and saves hundreds. The first month feels restrictive, by month 3 it feels like a raise."},
  {id:"lifestyle_creep",name:"Fighting Lifestyle Creep",fullName:"Keeping Expenses Flat as Income Grows",difficulty:"Beginner",category:"Budgeting",timeframe:"Ongoing",
    description:"The tendency to spend more as you earn more. Get a $5k raise, suddenly your car payment and dining budget grow by $5k. The #1 reason high earners are still broke.",
    signals:["Bank raises before you feel them → auto-invest","Keep housing costs flat through promotions","Drive the same car for 10+ years","One lifestyle upgrade per raise, invest the rest","Track spending quarterly to catch drift"],
    settings:"Rule: invest 50%+ of every raise. Live on last year's salary, save the difference.",bestFor:"Anyone getting promotions or pay increases. The gap between earning and spending is where wealth lives.",
    proTip:"A person earning $60k who saves 40% will be wealthier than someone earning $150k who saves 5%. Income doesn't build wealth — the gap does."},
  // === More Debt ===
  {id:"credit_utilization",name:"Credit Utilization",fullName:"Managing Credit Card Usage Ratio",difficulty:"Beginner",category:"Debt",timeframe:"Monthly",
    description:"The percentage of available credit you're using. Using $3,000 of a $10,000 limit = 30% utilization. This is the second biggest factor in your credit score after payment history.",
    signals:["Under 10% utilization → Excellent for score","Under 30% → Acceptable","Over 30% → Hurting your score","Per-card utilization matters too","Pay before statement date to lower reported balance"],
    settings:"Check each card's limit and balance. Total balance ÷ total limits = overall utilization.",bestFor:"Anyone building or repairing credit. Quick wins here — pay down a card and score jumps within 30 days.",
    proTip:"Pay your balance twice a month — once mid-cycle, once before due date. This keeps reported utilization near 0% even if you use the card heavily."},
  {id:"debt_to_income",name:"Debt-to-Income Ratio",fullName:"DTI and Why Lenders Care",difficulty:"Intermediate",category:"Debt",timeframe:"Ongoing",
    description:"Monthly debt payments divided by gross monthly income. Lenders use this to determine if you can handle more debt. Under 36% is healthy, under 20% is excellent, over 43% and most lenders say no.",
    signals:["Front-end DTI → Housing costs only (target <28%)","Back-end DTI → All debt payments (target <36%)","Include: mortgage, car, student loans, minimums","Exclude: utilities, food, insurance","Lower DTI = better rates and approval odds"],
    settings:"(Total monthly debt payments ÷ gross monthly income) × 100 = DTI%.",bestFor:"Anyone planning to buy a home or take on major financing. Know your DTI before applying.",
    proTip:"To improve DTI fast: pay off smallest debts to eliminate their minimum payments, or increase income. Both move the ratio. Getting a side hustle before applying for a mortgage is a legitimate strategy."},
  // === More Tax ===
  {id:"tax_loss_harvesting",name:"Tax-Loss Harvesting",fullName:"Turning Investment Losses into Tax Savings",difficulty:"Advanced",category:"Tax",timeframe:"Annual",
    description:"Selling investments at a loss to offset capital gains taxes. Lost $5k on one stock but gained $8k on another? Sell the loser, reduce taxable gains to $3k. Can also offset up to $3k of regular income per year.",
    signals:["Sell losing positions before year-end","Offset gains dollar-for-dollar","Excess losses offset $3k of income/year","Remaining losses carry forward indefinitely","Wash sale rule: can't rebuy same stock within 30 days"],
    settings:"Review portfolio in November-December. Identify positions with unrealized losses.",bestFor:"Taxable brokerage accounts. Doesn't apply to Roth IRA or 401k (those are already tax-advantaged).",
    proTip:"Sell the loser, immediately buy a similar (not identical) fund. Sell S&P 500 fund at a loss, buy a total market fund. You stay invested, get the tax benefit, and avoid the wash sale rule."},
  {id:"tax_advantaged",name:"Tax-Advantaged Accounts",fullName:"The Order of Operations for Tax-Efficient Investing",difficulty:"Intermediate",category:"Tax",timeframe:"Career-Long",
    description:"Not all accounts are created equal. The order you fill them matters enormously. Getting this wrong over a career can cost six figures in unnecessary taxes.",
    signals:["1. Employer match (401k/TSP) → Free money first","2. Roth IRA → $7,000/year, tax-free growth","3. Max out 401k/TSP → $23,000/year","4. HSA if eligible → Triple tax advantage","5. Taxable brokerage → After all tax-advantaged full"],
    settings:"2024 limits: 401k $23,000, IRA $7,000, HSA $4,150 single / $8,300 family.",bestFor:"Everyone investing. Following this order optimizes every dollar's tax treatment.",
    proTip:"The HSA is the most tax-advantaged account in existence. Deductible contributions, tax-free growth, tax-free withdrawals for medical. After 65 it works like a traditional IRA for non-medical expenses."},
  // === More Military ===
  {id:"military_pay",name:"Military Pay Breakdown",fullName:"Understanding Your Total Compensation",difficulty:"Beginner",category:"Military",timeframe:"Monthly",
    description:"Base pay is only part of the picture. BAH, BAS, and special pays are often tax-free, making military compensation worth 20-30% more than the equivalent civilian salary.",
    signals:["Base pay → Taxable, based on rank + time in service","BAH → Tax-free housing allowance","BAS → Tax-free food allowance (~$400/mo)","Special pays → Flight, hazard, sea, etc.","Tax-free = effectively 20-30% more than face value"],
    settings:"Use the Military tab calculator. An E-5 with 4 years in San Diego: $3,050 base + $2,350 BAH + $400 BAS = $5,800/mo, but tax-equivalent of ~$7,200.",bestFor:"New enlistees and anyone comparing military vs civilian pay. The tax-free benefits change the math completely.",
    proTip:"In a combat zone, ALL pay becomes tax-free. Max out Roth TSP during deployments. You're contributing tax-free money that grows and withdraws tax-free. It's the ultimate triple tax benefit."},
  {id:"military_transition",name:"Transition Planning",fullName:"Preparing for Post-Military Life",difficulty:"Intermediate",category:"Military",timeframe:"12-24 Months Before ETS",
    description:"Start planning 12-24 months before separation. Use SkillBridge for civilian job experience, apply for VA disability, line up GI Bill school, and have 6+ months expenses saved.",
    signals:["Start TAP/TAPS classes 12+ months out","Apply for VA disability before separation","Research SkillBridge programs (last 6 months)","Save 6-month emergency fund before ETS","Use GI Bill MHA to replace BAH income"],
    settings:"Timeline: 24mo = plan, 18mo = save aggressively, 12mo = TAP + VA claims, 6mo = SkillBridge, 0 = separate.",bestFor:"Anyone within 2 years of ETS. The transition from guaranteed paycheck to civilian life is the riskiest financial period.",
    proTip:"File your VA disability claim 180 days before separation using the Benefits Delivery at Discharge (BDD) program. Claims filed while still in are processed faster and have higher approval rates."},
  // === More Retirement ===
  {id:"coast_fire",name:"Coast FIRE",fullName:"Coasting to Retirement",difficulty:"Intermediate",category:"Retirement",timeframe:"10-15 Years",
    description:"Save aggressively early until your investments will grow to a full retirement number on their own through compounding — even with zero additional contributions. Then 'coast' with lower-stress work.",
    signals:["Calculate your FIRE number (expenses × 25)","Determine how much you need invested TODAY","Factor: current age, retirement age, expected return","Once you hit Coast number → optional to save more","Work for enjoyment/insurance, not survival"],
    settings:"Coast FIRE formula: FIRE number ÷ (1 + return)^(years to retirement). E.g., $1M needed at 60, 7% return, age 30 → need $131k now.",bestFor:"People who want freedom sooner without the extreme frugality of full FIRE. Work becomes optional, not mandatory.",
    proTip:"A military member who maxes TSP for 8 years (E-1 to E-5) could hit Coast FIRE by 26. Even if they never invest another dollar, compounding handles the rest by 55."},
  {id:"withdrawal_strategy",name:"Withdrawal Strategy",fullName:"How to Draw Down Your Portfolio in Retirement",difficulty:"Advanced",category:"Retirement",timeframe:"Retirement",
    description:"Which accounts to withdraw from and in what order matters for tax efficiency. Generally: taxable first, then traditional, then Roth last (it grows tax-free longest).",
    signals:["Taxable accounts first → Capital gains rates are lower","Traditional 401k/IRA second → Pay ordinary income tax","Roth last → Tax-free, let it grow longest","Stay within lower tax brackets each year","Roth conversions in low-income years"],
    settings:"Withdrawal order: taxable brokerage → traditional IRA/401k → Roth IRA. Adjust annually based on tax situation.",bestFor:"Anyone within 5-10 years of retirement. Getting the order right saves tens of thousands in taxes.",
    proTip:"The years between retirement and Social Security/RMDs are the 'golden years' for Roth conversions. Your income is low, so you can convert traditional to Roth at rock-bottom tax rates."},
  // === More Real Estate ===
  {id:"rent_vs_buy",name:"Rent vs Buy",fullName:"The Real Math Behind Renting vs Buying",difficulty:"Intermediate",category:"Real Estate",timeframe:"5+ Years",
    description:"Buying isn't always better. The real comparison: total cost of ownership (mortgage + taxes + insurance + maintenance + opportunity cost) vs rent + investing the difference. Location and timeline matter enormously.",
    signals:["Staying 5+ years → Buying usually wins","Under 3 years → Renting almost always wins","Price-to-rent ratio > 20 → Renting is better","Factor in ALL costs: taxes, insurance, HOA, repairs","Compare: invest down payment at 10% vs home appreciation at 3-5%"],
    settings:"Use the Real Estate tab calculator. Input local prices, rent, rates, and timeline.",bestFor:"Anyone deciding whether to buy. Removes emotion from one of the biggest financial decisions.",
    proTip:"The 5% rule: multiply home price by 5%, divide by 12. If rent is less than that number, renting is financially better. $400k home × 5% = $20k/year = $1,667/mo break-even rent."},
  {id:"va_loan",name:"VA Loan Power",fullName:"Maximizing the VA Home Loan Benefit",difficulty:"Beginner",category:"Real Estate",timeframe:"Lifetime Benefit",
    description:"0% down, no PMI, competitive rates, and reusable. The VA loan is arguably the single most valuable financial benefit of military service. Can be used on 1-4 unit properties.",
    signals:["0% down payment → Keep cash invested","No PMI ever → Saves $200-400/month vs conventional","Reusable → Pay off one, use it again","Rates often lower than conventional","Works on duplexes/triplexes/fourplexes"],
    settings:"No loan limit in most areas (with full entitlement). Funding fee: 2.15% first use, 3.3% subsequent (waived with VA disability).",bestFor:"Any eligible veteran or active duty member buying a home. There's almost no reason to use a conventional loan instead.",
    proTip:"Buy a fourplex with VA loan at 0% down, live in one unit, rent three. If the rent covers the mortgage, you're living for free while building equity. Repeat every 1-2 years."},
  // === More Crypto ===
  {id:"crypto_taxes",name:"Crypto Taxes",fullName:"How Cryptocurrency is Taxed",difficulty:"Intermediate",category:"Crypto",timeframe:"Annual",
    description:"The IRS treats crypto as property, not currency. Every trade, swap, or purchase is a taxable event. Yes, even swapping BTC for ETH triggers capital gains tax. Many people learn this the hard way.",
    signals:["Selling crypto → Capital gains/loss event","Swapping crypto-to-crypto → Taxable event","Buying with crypto → Taxable (disposed of property)","Mining/staking rewards → Ordinary income at receipt","HODLing → Not taxable until you sell"],
    settings:"Short-term (<1 year): taxed as ordinary income (10-37%). Long-term (>1 year): 0%, 15%, or 20%.",bestFor:"Anyone trading or earning crypto. One year of untracked trades can create a tax nightmare.",
    proTip:"Use a crypto tax tool (Koinly, CoinTracker) to auto-track your cost basis. Do this throughout the year, not in April. And HODL for 12+ months when possible — long-term rates save 10-20% vs short-term."},
  {id:"crypto_risk",name:"Crypto Risk Management",fullName:"Position Sizing and Risk Control",difficulty:"Intermediate",category:"Crypto",timeframe:"Ongoing",
    description:"Crypto can drop 50-80% in months. Position sizing is everything. The standard advice: only invest what you can afford to lose completely. For most people, 5-15% of portfolio max.",
    signals:["5-15% of total portfolio max in crypto","BTC + ETH = 70%+ of crypto allocation","Altcoins = high risk, small positions only","Never use leverage in crypto","Set maximum loss threshold and stick to it"],
    settings:"Portfolio allocation: 60% stocks, 25% bonds/cash, 15% crypto max. Within crypto: 50% BTC, 30% ETH, 20% other.",bestFor:"Anyone adding crypto to a diversified portfolio. Prevents the classic mistake of going all-in on a moonshot.",
    proTip:"If crypto going to zero would meaningfully damage your financial life, you own too much. It should be the hot sauce, not the main dish."},
  // === More Investing ===
  {id:"index_vs_active",name:"Index vs Active",fullName:"Why Index Funds Beat Stock Pickers",difficulty:"Beginner",category:"Investing",timeframe:"Long-Term",
    description:"Over 15 years, 90%+ of actively managed funds underperform their benchmark index. After fees, the number is even worse. A $10k investment in the S&P 500 index in 1990 is worth $200k+ today.",
    signals:["S&P 500 index returns ~10% annually long-term","Active funds charge 0.5-1.5% fees → drag on returns","1% fee difference = $100k+ over 30 years","Warren Buffett bet $1M that index beats hedge funds → won","Three-fund portfolio beats most advisors"],
    settings:"Core index funds: VTI/VTSAX (US total market), VXUS (international), BND (bonds). Expense ratios under 0.10%.",bestFor:"Everyone. This is the boring, proven, mathematically optimal approach that most professionals can't beat.",
    proTip:"If someone tells you they can consistently beat the market, ask them why they're selling advice instead of managing their own billions. The data is overwhelming: index and chill."},
  {id:"dollar_cost_avg",name:"DCA vs Lump Sum",fullName:"Dollar-Cost Averaging vs Investing All at Once",difficulty:"Intermediate",category:"Investing",timeframe:"Ongoing",
    description:"Historically, lump sum investing beats DCA about 66% of the time because markets trend upward. But DCA reduces regret risk and is psychologically easier. Both crush sitting in cash.",
    signals:["Lump sum wins ~66% of the time mathematically","DCA wins on behavioral consistency","Both massively beat timing the market","DCA removes 'what if it drops tomorrow' anxiety","Regular paychecks = forced DCA anyway"],
    settings:"If you have a lump sum: invest 50% immediately, DCA the rest over 3-6 months. Best of both worlds.",bestFor:"Anyone with a windfall (bonus, inheritance, tax refund) wondering whether to invest all at once.",
    proTip:"The best time to invest was yesterday. The second best time is today. Arguments about DCA vs lump sum are irrelevant if the alternative is sitting in cash losing to inflation."},
  {id:"rebalancing",name:"Portfolio Rebalancing",fullName:"Maintaining Target Allocations",difficulty:"Intermediate",category:"Investing",timeframe:"Annual",
    description:"Over time, winning investments grow to dominate your portfolio. If your target is 80/20 stocks/bonds but stocks crushed it and you're now 92/8, sell stocks and buy bonds to rebalance. Forces buy low, sell high.",
    signals:["Check allocations quarterly or annually","Rebalance when >5% off target","Sell what's overweight → Buy what's underweight","Use new contributions to rebalance first (tax-free)","Tax-loss harvest during rebalancing"],
    settings:"Rebalance annually or when any asset class drifts 5%+ from target. Preferably in tax-advantaged accounts.",bestFor:"Anyone with a multi-asset portfolio. Maintains your chosen risk level and forces disciplined selling of winners.",
    proTip:"The lazy way: direct all new contributions to the underweight asset class. This rebalances naturally without selling anything (and without triggering taxes in taxable accounts)."},
];
const GLOSSARY = [
  // Business
  {term:"Revenue",def:"Total money coming in before any costs. Also called sales or top-line income.",cat:"Business"},
  {term:"Gross Profit",def:"Revenue minus direct costs. Doesn't include rent, salaries, or overhead.",cat:"Business"},
  {term:"Net Profit",def:"What's left after all expenses. The actual money you keep.",cat:"Business"},
  {term:"Margin",def:"Profit as a percentage of revenue. 40% margin = 40 cents profit per dollar sold.",cat:"Business"},
  {term:"Markup",def:"Amount added on top of cost. $10 item at $15 is 50% markup but 33% margin.",cat:"Business"},
  {term:"COGS",def:"Cost of Goods Sold. Direct costs to produce what you sell.",cat:"Business"},
  {term:"Overhead",def:"Ongoing costs not tied to specific sales. Rent, utilities, software.",cat:"Business"},
  {term:"Accounts Receivable",def:"Money customers owe you. An asset on your balance sheet.",cat:"Business"},
  {term:"Accounts Payable",def:"Money you owe suppliers. Your unpaid bills.",cat:"Business"},
  {term:"Cash Flow",def:"Actual money moving in and out. Profitable businesses can still fail here.",cat:"Business"},
  {term:"Break-Even",def:"Where revenue equals total costs. Below: losing money. Above: profitable.",cat:"Business"},
  {term:"Balance Sheet",def:"Snapshot of what a business owns (assets), owes (liabilities), and is worth (equity) at a point in time.",cat:"Business"},
  {term:"Income Statement",def:"Shows revenue, expenses, and profit over a period. Also called a P&L (Profit & Loss).",cat:"Business"},
  {term:"ROI",def:"Return on Investment. Profit divided by cost, expressed as %. 100% ROI = you doubled your money.",cat:"Business"},
  // Investing
  {term:"ETF",def:"Exchange-Traded Fund. A basket of stocks/bonds you buy as one ticker. SPY holds all S&P 500 companies.",cat:"Investing"},
  {term:"Index Fund",def:"A fund that tracks a market index like the S&P 500. Low fees, broad diversification, the default smart investment.",cat:"Investing"},
  {term:"Dividend",def:"Cash payment from a company to shareholders. Usually quarterly. Reinvesting dividends accelerates growth.",cat:"Investing"},
  {term:"Capital Gains",def:"Profit from selling an asset for more than you paid. Short-term (under 1yr) taxed higher than long-term.",cat:"Investing"},
  {term:"Dollar-Cost Averaging",def:"Investing a fixed amount regularly regardless of price. Removes emotion and timing risk from investing.",cat:"Investing"},
  {term:"Compound Interest",def:"Interest earned on interest. The reason $100/mo at 10% becomes $200k+ over 20 years, not $24k.",cat:"Investing"},
  {term:"Bull Market",def:"Extended period of rising prices. Generally defined as a 20%+ gain from recent lows.",cat:"Investing"},
  {term:"Bear Market",def:"Extended period of falling prices. A 20%+ decline from recent highs. Historically, they end.",cat:"Investing"},
  {term:"Volatility",def:"How much and how fast prices swing. High volatility = bigger swings. Measured by standard deviation of returns.",cat:"Investing"},
  {term:"Liquidity",def:"How easily something converts to cash. Stocks are liquid. Real estate is not. Cash is perfectly liquid.",cat:"Investing"},
  {term:"P/E Ratio",def:"Price-to-Earnings ratio. Stock price divided by earnings per share. Lower = cheaper relative to profits.",cat:"Investing"},
  {term:"Market Cap",def:"Total value of a company's shares. Share price × total shares. Mega-cap = $200B+, large = $10B+.",cat:"Investing"},
  {term:"Expense Ratio",def:"Annual fee charged by a fund, taken from returns. 0.03% is great, 1%+ is robbery. Always check this.",cat:"Investing"},
  {term:"Diversification",def:"Spreading money across different investments to reduce risk. Don't put all eggs in one basket.",cat:"Investing"},
  {term:"Rebalancing",def:"Adjusting your portfolio back to target allocations. If stocks grew to 80% but target is 60%, sell some.",cat:"Investing"},
  // Market / Technical
  {term:"MACD",def:"Moving Average Convergence Divergence. Shows momentum by comparing two moving averages. Crossovers signal trend changes.",cat:"Market"},
  {term:"RSI",def:"Relative Strength Index. Oscillator from 0-100. Above 70 = overbought, below 30 = oversold.",cat:"Market"},
  {term:"Bollinger Bands",def:"Price channel based on standard deviations from a moving average. Squeeze = low volatility, big move coming.",cat:"Market"},
  {term:"Support",def:"Price level where buying pressure tends to prevent further decline. A floor.",cat:"Market"},
  {term:"Resistance",def:"Price level where selling pressure tends to prevent further rise. A ceiling.",cat:"Market"},
  {term:"EMA",def:"Exponential Moving Average. Weighted average that reacts faster to recent prices than a simple MA.",cat:"Market"},
  {term:"SMA",def:"Simple Moving Average. Unweighted average of closing prices over a period. Smoother but slower.",cat:"Market"},
  {term:"Golden Cross",def:"When 50-day MA crosses above 200-day MA. Historically bullish long-term signal.",cat:"Market"},
  {term:"Death Cross",def:"When 50-day MA crosses below 200-day MA. Bearish signal, but often a lagging indicator.",cat:"Market"},
  {term:"Candlestick",def:"Chart bar showing open, high, low, close for a period. Green/hollow = up, red/filled = down.",cat:"Market"},
  {term:"Volume",def:"Number of shares or contracts traded. Confirms price moves — high volume = conviction.",cat:"Market"},
  // Budgeting
  {term:"Net Worth",def:"Everything you own minus everything you owe. The single number that measures your financial health.",cat:"Budgeting"},
  {term:"Emergency Fund",def:"3-6 months of expenses in a savings account. The foundation of financial stability. Build this first.",cat:"Budgeting"},
  {term:"Savings Rate",def:"Percentage of income you save/invest. 20% is solid, 50%+ is FIRE territory.",cat:"Budgeting"},
  {term:"50/30/20 Rule",def:"Budget framework: 50% needs, 30% wants, 20% savings. Simple starting point, adjust to your situation.",cat:"Budgeting"},
  {term:"Sinking Fund",def:"Money set aside monthly for a known future expense. Car repair fund, vacation fund, etc.",cat:"Budgeting"},
  {term:"Pay Yourself First",def:"Automatically save/invest before spending on anything else. Treat savings like a bill.",cat:"Budgeting"},
  {term:"Lifestyle Creep",def:"Spending more as you earn more. The silent killer of wealth building. Fight it.",cat:"Budgeting"},
  // Debt
  {term:"APR",def:"Annual Percentage Rate. The true yearly cost of a loan including fees. Always higher than the base interest rate.",cat:"Debt"},
  {term:"Principal",def:"The original amount borrowed or invested, before interest. On a $200k mortgage, $200k is the principal.",cat:"Debt"},
  {term:"Interest Rate",def:"The cost of borrowing money or the reward for lending it, expressed as annual %. Lower is better when you're borrowing.",cat:"Debt"},
  {term:"Amortization",def:"Spreading loan payments over time so each payment covers both interest and principal. Standard for mortgages.",cat:"Debt"},
  {term:"Avalanche Method",def:"Pay minimum on all debts, throw extra at highest-interest first. Mathematically optimal, saves the most money.",cat:"Debt"},
  {term:"Snowball Method",def:"Pay minimum on all debts, throw extra at smallest balance first. Psychologically motivating — quick wins.",cat:"Debt"},
  {term:"Debt-to-Income",def:"Monthly debt payments divided by gross monthly income. Lenders want this under 36%. Under 20% is strong.",cat:"Debt"},
  {term:"Credit Score",def:"A number (300-850) representing your creditworthiness. 750+ is excellent. Affects loan rates, rental apps, even jobs.",cat:"Debt"},
  {term:"Refinancing",def:"Replacing an existing loan with a new one at better terms. Only worth it if you save enough to cover closing costs.",cat:"Debt"},
  // Tax
  {term:"1099",def:"Tax form for freelance/contract income over $600. Triggers SE tax.",cat:"Tax"},
  {term:"W-2",def:"Tax form for employee wages. Employer withholds taxes.",cat:"Tax"},
  {term:"Write-Off",def:"Business expense deducted from taxable income. Reduces tax, not free.",cat:"Tax"},
  {term:"Quarterly Estimates",def:"Tax payments 4x/year for self-employed. No one withholds for them.",cat:"Tax"},
  {term:"Depreciation",def:"Spreading an asset's cost over its useful life instead of all at once.",cat:"Tax"},
  {term:"Standard Deduction",def:"Fixed amount subtracted from income before tax. $14,600 single in 2024. Most people take this over itemizing.",cat:"Tax"},
  {term:"Marginal Tax Rate",def:"Tax rate on your next dollar earned. Being in the 22% bracket doesn't mean all income is taxed at 22%.",cat:"Tax"},
  {term:"Effective Tax Rate",def:"Total tax paid divided by total income. Your actual average rate. Always lower than your marginal rate.",cat:"Tax"},
  {term:"Tax-Advantaged",def:"Accounts where you get a tax break — 401k, IRA, HSA, TSP. Use these before taxable brokerage accounts.",cat:"Tax"},
  {term:"Self-Employment Tax",def:"15.3% tax on freelance income covering Social Security + Medicare. On top of income tax. Plan for it.",cat:"Tax"},
  // Military
  {term:"BAH",def:"Basic Allowance for Housing. Tax-free military payment for off-base housing. Amount varies by rank and location.",cat:"Military"},
  {term:"BAS",def:"Basic Allowance for Subsistence. Monthly food allowance for military members. About $400/mo for enlisted.",cat:"Military"},
  {term:"GI Bill",def:"Covers 36 months of college tuition plus a monthly housing allowance. One of the most valuable military benefits.",cat:"Military"},
  {term:"TSP",def:"Thrift Savings Plan. The military/federal 401k. Low fees, employer match up to 5%. Use it.",cat:"Military"},
  {term:"MHA",def:"Monthly Housing Allowance under GI Bill. Paid while attending school, based on zip code. Equivalent to E-5 BAH.",cat:"Military"},
  {term:"TRICARE",def:"Military health insurance. Essentially free while active duty. Covers family too.",cat:"Military"},
  {term:"SCRA",def:"Servicemembers Civil Relief Act. Caps interest rates at 6% on pre-service debt. Powerful protection.",cat:"Military"},
  {term:"SBP",def:"Survivor Benefit Plan. Provides up to 55% of retirement pay to spouse/dependents if you die. Costs 6.5% of pay.",cat:"Military"},
  {term:"TDY/TAD",def:"Temporary Duty. Travel for military work with per diem (daily pay for food/lodging). Can be profitable.",cat:"Military"},
  // Retirement
  {term:"Roth IRA",def:"Retirement account where you pay taxes now, never again. Contributions can be withdrawn anytime penalty-free.",cat:"Retirement"},
  {term:"401(k)",def:"Employer-sponsored retirement account. Often comes with employer match — free money you should always take.",cat:"Retirement"},
  {term:"FIRE",def:"Financial Independence, Retire Early. Save aggressively (50-70% of income) to retire in your 30s-40s.",cat:"Retirement"},
  {term:"4% Rule",def:"Withdraw 4% of your portfolio per year in retirement. $1M portfolio = $40k/year. The standard retirement math.",cat:"Retirement"},
  {term:"Vesting",def:"How long before employer contributions are fully yours. 3-year cliff = nothing until year 3, then 100%.",cat:"Retirement"},
  {term:"Required Minimum Distribution",def:"Forced withdrawals from retirement accounts starting at age 73. Government wants its tax money eventually.",cat:"Retirement"},
  {term:"Roth Conversion",def:"Moving money from traditional (pre-tax) to Roth (post-tax) account. Pay taxes now, grow tax-free forever.",cat:"Retirement"},
  {term:"HSA",def:"Health Savings Account. Triple tax advantage: deduct contributions, grow tax-free, withdraw tax-free for medical. Best retirement hack.",cat:"Retirement"},
  // Real Estate
  {term:"Equity",def:"Your ownership stake. Home value minus what you owe. $300k home with $200k mortgage = $100k equity.",cat:"Real Estate"},
  {term:"LTV",def:"Loan-to-Value ratio. Mortgage balance divided by home value. Under 80% = no PMI required.",cat:"Real Estate"},
  {term:"PMI",def:"Private Mortgage Insurance. Extra fee when your down payment is under 20%. Adds $100-300/mo. Drops off at 80% LTV.",cat:"Real Estate"},
  {term:"DTI",def:"Debt-to-Income ratio for mortgage qualification. Front-end (housing only) should be under 28%, back-end (all debt) under 36%.",cat:"Real Estate"},
  {term:"Cap Rate",def:"Capitalization Rate. Net operating income ÷ property value. A 6% cap rate means 6% annual return before financing.",cat:"Real Estate"},
  {term:"Cash-on-Cash Return",def:"Annual cash flow divided by total cash invested. The real return metric for leveraged real estate.",cat:"Real Estate"},
  {term:"House Hacking",def:"Buy a multi-unit, live in one unit, rent the others. Your tenants pay your mortgage. Best first real estate move.",cat:"Real Estate"},
  {term:"VA Loan",def:"0% down mortgage for military. No PMI ever. One of the most powerful financial tools available to service members.",cat:"Real Estate"},
  // Crypto
  {term:"DCA (Crypto)",def:"Dollar-cost averaging into crypto. Same concept as stocks — fixed amount on a schedule. Reduces volatility risk.",cat:"Crypto"},
  {term:"HODL",def:"Hold On for Dear Life. Crypto slang for holding through volatility instead of panic selling.",cat:"Crypto"},
  {term:"Staking",def:"Locking crypto to help validate transactions. Earn rewards (like interest) while holding. Rates vary by chain.",cat:"Crypto"},
  {term:"Gas Fee",def:"Transaction fee on blockchains like Ethereum. Varies with network congestion. Can be $1 or $100+.",cat:"Crypto"},
  {term:"Cold Wallet",def:"Offline crypto storage (hardware device). Most secure way to hold crypto. Not connected to internet = unhackable.",cat:"Crypto"},
  {term:"Hot Wallet",def:"Online crypto wallet (app/exchange). Convenient but vulnerable. Keep only what you actively trade here.",cat:"Crypto"},
  {term:"Market Cap (Crypto)",def:"Total value of a cryptocurrency. Price × circulating supply. Bitcoin dominance = BTC market cap ÷ total crypto market cap.",cat:"Crypto"},
];

// ===================== MILITARY DATA =====================
const BRANCHES = ["Army","Navy","Air Force","Marine Corps","Coast Guard","Space Force"];
const PAY_TABLE = {
  "E-1":[1949,1949,1949],
  "E-2":[2185,2185,2185],
  "E-3":[2298,2298,2418],
  "E-4":[2450,2598,2738],
  "E-5":[2900,3050,3200],
  "E-6":[3200,3400,3600],
  "E-7":[3700,3900,4100],
  "E-8":[4600,4800,5000],
  "E-9":[5500,5700,5900],
};
const BAH_SAMPLES = {
  "San Diego, CA":2350,"Fort Liberty, NC":1450,"Fort Hood, TX":1250,"Joint Base Lewis-McChord, WA":1950,
  "Fort Bragg, NC":1450,"Norfolk, VA":1600,"Colorado Springs, CO":1750,"Honolulu, HI":2800,
  "Fort Campbell, KY":1200,"Jacksonville, FL":1500,"San Antonio, TX":1400,"El Paso, TX":1200,
  "Fort Carson, CO":1750,"Pensacola, FL":1350,"Killeen, TX":1250,"Tacoma, WA":1950,
  "Virginia Beach, VA":1600,"Fayetteville, NC":1350,"Oceanside, CA":2200,"Custom Amount":0,
};


function MilitaryCalculator({t}) {
  const [branch, setBranch] = useState("Army");
  const [age, setAge] = useState("18");
  const [startRank, setStartRank] = useState("E-1");
  const [enlistYears, setEnlistYears] = useState(4);
  const [dutyStation, setDutyStation] = useState("Fort Liberty, NC");
  const [customBAH, setCustomBAH] = useState("1500");
  const [monthlyExpenses, setMonthlyExpenses] = useState("300");
  const [sideHustle, setSideHustle] = useState("");
  const [investRate, setInvestRate] = useState("10");
  const [showAdvanced, setShowAdvanced] = useState(false);
  const [postMilContrib, setPostMilContrib] = useState("1500");
  const [tspMatch, setTspMatch] = useState(true);
  const [tspContribPct, setTspContribPct] = useState("5");
  const [showProgression, setShowProgression] = useState(false);
  const [customRanks, setCustomRanks] = useState(null);
  const [yearBonuses, setYearBonuses] = useState(null);
  const canvasRef = useRef(null);

  const num = (v) => parseFloat(v) || 0;
  const startAge = Math.max(17, Math.min(42, Math.round(num(age)))) || 18;
  const bah = dutyStation === "Custom Amount" ? num(customBAH) : BAH_SAMPLES[dutyStation];
  const ALL_RANKS = ["E-1","E-2","E-3","E-4","E-5","E-6","E-7","E-8","E-9"];
  const startIdx = ALL_RANKS.indexOf(startRank);

  const buildDefaultRanks = () => {
    const rr = []; let idx = startIdx;
    for (let yr = 0; yr < 20; yr++) {
      rr.push(ALL_RANKS[Math.min(idx, ALL_RANKS.length - 1)]);
      if (idx < 4 && yr > 0) idx++;
      else if (idx >= 4 && idx < 6 && yr > 0 && yr % 2 === 0) idx++;
      else if (idx >= 6 && yr > 0 && yr % 3 === 0) idx++;
    }
    return rr.slice(0, enlistYears);
  };

  useEffect(() => {
    setCustomRanks(buildDefaultRanks());
    const b = new Array(enlistYears).fill("");
    if (enlistYears > 4) b[3] = "20000";
    setYearBonuses(b);
  }, [enlistYears, startRank]);

  const ranks = (customRanks && customRanks.length === enlistYears) ? customRanks : buildDefaultRanks();
  const bonusList = (yearBonuses && yearBonuses.length === enlistYears) ? yearBonuses : new Array(enlistYears).fill("");

  const setRankForYear = (yr, rank) => { const n = [...ranks]; n[yr] = rank; setCustomRanks(n); };
  const setBonusForYear = (yr, val) => { const n = [...bonusList]; n[yr] = val; setYearBonuses(n); };

  // Calculate
  const yearlyData = [];
  let totalInvested = 0, portfolio = 0;
  const r = num(investRate) / 100;
  const tspPct = Math.min(num(tspContribPct), 100) / 100;

  for (let yr = 0; yr < enlistYears; yr++) {
    const rank = ranks[yr] || "E-1";
    const yrsInRank = yr < 2 ? 0 : yr < 4 ? 1 : 2;
    const basePay = PAY_TABLE[rank]?.[yrsInRank] || PAY_TABLE[rank]?.[0] || 2000;
    const bahActive = yr >= 3 ? bah : 0;
    const housingExp = yr >= 3 ? Math.min(bah * 0.4, 700) : 0;

    const yourTSP = tspMatch ? basePay * tspPct : 0;
    const autoOne = tspMatch ? basePay * 0.01 : 0;
    const matchAmt = tspMatch ? (Math.min(tspPct, 0.03) * basePay + Math.max(0, Math.min(tspPct - 0.03, 0.02)) * basePay * 0.5) : 0;
    const govTSP = autoOne + matchAmt;

    const totalIncome = basePay + bahActive + num(sideHustle);
    const totalExp = yr >= 3 ? (num(monthlyExpenses) + housingExp) : num(monthlyExpenses);
    const monthlyInvest = Math.max(0, totalIncome - yourTSP - totalExp);
    const totalMonthly = monthlyInvest + yourTSP + govTSP;
    const annualInvest = totalMonthly * 12;
    const bonusThisYear = num(bonusList[yr]);

    portfolio = (portfolio + bonusThisYear) * (1 + r) + annualInvest * ((1 + r/12) ** 6);
    totalInvested += annualInvest + bonusThisYear;

    yearlyData.push({ year: yr + 1, age: startAge + yr, rank, basePay, bah: bahActive,
      sideHustle: num(sideHustle), tspContrib: Math.round(yourTSP), govMatch: Math.round(govTSP),
      monthlyInvest, totalMonthly: Math.round(totalMonthly), bonus: bonusThisYear,
      portfolio: Math.round(portfolio), totalInvested: Math.round(totalInvested) });
  }

  const postYears = [];
  let postPort = portfolio;
  for (let yr = 1; yr <= 20; yr++) {
    postPort = postPort * (1 + r) + num(postMilContrib) * 12;
    postYears.push({ age: startAge + enlistYears + yr, portfolio: Math.round(postPort) });
  }
  // Chart
  useEffect(() => {
    const canvas = canvasRef.current;
    if (!canvas || yearlyData.length === 0) return;
    const ctx = canvas.getContext("2d");
    const dpr = window.devicePixelRatio || 1;
    const rect = canvas.getBoundingClientRect();
    canvas.width = rect.width * dpr; canvas.height = rect.height * dpr;
    ctx.scale(dpr, dpr);
    const W = rect.width, H = rect.height;
    ctx.clearRect(0, 0, W, H);

    const allPts = [...yearlyData.map(d => d.portfolio), ...postYears.slice(0, 12).map(d => d.portfolio)];
    const allInv = yearlyData.map(d => d.totalInvested);
    const maxV = Math.max(...allPts, 1);
    const totalPts = yearlyData.length + Math.min(12, postYears.length);
    const pT = 20, pB = 35, pL = 65, pR = 15, cW = W - pL - pR, cH = H - pT - pB;
    const toX = i => pL + (i / (totalPts - 1)) * cW;
    const toY = v => pT + cH - (v / maxV) * cH;

    // Grid
    ctx.strokeStyle = t.border; ctx.lineWidth = 1;
    for (let i = 0; i <= 4; i++) {
      const y = pT + (cH / 4) * i;
      ctx.beginPath(); ctx.moveTo(pL, y); ctx.lineTo(W - pR, y); ctx.stroke();
      ctx.fillStyle = t.textMuted; ctx.font = "10px Inter,sans-serif"; ctx.textAlign = "right";
      const val = maxV * (1 - i / 4);
      ctx.fillText("$" + (val >= 1e6 ? (val / 1e6).toFixed(1) + "M" : val >= 1e3 ? (val / 1e3).toFixed(0) + "k" : val.toFixed(0)), pL - 6, y + 3);
    }

    // Divider
    const divX = toX(yearlyData.length - 1);
    ctx.strokeStyle = t.textMuted + "30"; ctx.setLineDash([4, 4]);
    ctx.beginPath(); ctx.moveTo(divX, pT); ctx.lineTo(divX, pT + cH); ctx.stroke(); ctx.setLineDash([]);
    ctx.fillStyle = t.textMuted + "60"; ctx.font = "9px Inter,sans-serif"; ctx.textAlign = "center";
    ctx.fillText("Enlistment | Post-Military", divX, pT + cH + 12);

    // Invested area (enlistment only)
    ctx.beginPath(); ctx.moveTo(toX(0), pT + cH);
    for (let i = 0; i < allInv.length; i++) ctx.lineTo(toX(i), toY(allInv[i]));
    ctx.lineTo(toX(allInv.length - 1), pT + cH); ctx.closePath();
    ctx.fillStyle = t.blue + "15"; ctx.fill();

    // Portfolio line
    ctx.beginPath(); ctx.strokeStyle = t.accent; ctx.lineWidth = 2;
    for (let i = 0; i < yearlyData.length; i++) { const x = toX(i), y = toY(yearlyData[i].portfolio); i === 0 ? ctx.moveTo(x, y) : ctx.lineTo(x, y); }
    ctx.stroke();

    // Post-military line
    ctx.beginPath(); ctx.strokeStyle = t.green; ctx.lineWidth = 2;
    ctx.moveTo(toX(yearlyData.length - 1), toY(yearlyData[yearlyData.length - 1].portfolio));
    for (let i = 0; i < Math.min(12, postYears.length); i++) {
      ctx.lineTo(toX(yearlyData.length + i), toY(postYears[i].portfolio));
    }
    ctx.stroke();

    // Fill under portfolio
    ctx.beginPath();
    ctx.moveTo(toX(0), toY(yearlyData[0].portfolio));
    for (let i = 1; i < yearlyData.length; i++) ctx.lineTo(toX(i), toY(yearlyData[i].portfolio));
    for (let i = 0; i < Math.min(12, postYears.length); i++) ctx.lineTo(toX(yearlyData.length + i), toY(postYears[i].portfolio));
    ctx.lineTo(toX(yearlyData.length + Math.min(12, postYears.length) - 1), pT + cH);
    ctx.lineTo(toX(0), pT + cH); ctx.closePath();
    const grd = ctx.createLinearGradient(0, pT, 0, pT + cH);
    grd.addColorStop(0, t.accent + "20"); grd.addColorStop(1, t.accent + "00");
    ctx.fillStyle = grd; ctx.fill();

    // Age labels
    ctx.fillStyle = t.textMuted; ctx.font = "9px Inter,sans-serif"; ctx.textAlign = "center";
    for (let i = 0; i < yearlyData.length; i++) {
      if (i === 0 || i === yearlyData.length - 1 || i % 2 === 0)
        ctx.fillText("" + yearlyData[i].age, toX(i), H - pB + 20);
    }
    for (let i = 0; i < Math.min(12, postYears.length); i++) {
      if (i % 3 === 0) ctx.fillText("" + postYears[i].age, toX(yearlyData.length + i), H - pB + 20);
    }
  }, [yearlyData, postYears, t, enlistYears]);

  const fmt = n => n >= 1e6 ? "$" + (n / 1e6).toFixed(2) + "M" : "$" + n.toLocaleString("en-US", { maximumFractionDigits: 0 });
  const lastYr = yearlyData[yearlyData.length - 1];
  const milestone1M = postYears.find(p => p.portfolio >= 1000000);
  const inputStyle = { width: "100%", padding: "9px 12px", fontSize: "14px", fontFamily: "inherit", border: `1px solid ${t.inputBorder}`, borderRadius: "6px", background: t.inputBg, color: t.text, outline: "none" };

  const totalGovMatchAll = yearlyData.reduce((s, d) => s + d.govMatch * 12, 0);

  return (
    <div style={{ maxWidth: "800px", margin: "0 auto" }}>
      {/* Intro */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "18px 20px", marginBottom: "16px" }}>
        <h2 style={{ fontSize: "16px", fontWeight: "700", margin: "0 0 6px" }}>Military Wealth Projection</h2>
        <p style={{ fontSize: "12px", color: t.textSecondary, lineHeight: "1.6", margin: 0 }}>
          See how much wealth you can build during and after military service. Enter your details below — the calculator auto-fills your pay based on rank and estimates how your investments grow over time.
        </p>
      </div>

      {/* About You */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "20px", marginBottom: "12px" }}>
        <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, marginBottom: "12px", textTransform: "uppercase", letterSpacing: "0.5px" }}>About You</div>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr 1fr", gap: "12px" }}>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Branch</label>
            <select value={branch} onChange={e => setBranch(e.target.value)} style={{ ...inputStyle, cursor: "pointer" }}>
              {BRANCHES.map(b => <option key={b} value={b}>{b}</option>)}
            </select>
          </div>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Your Current Age</label>
            <input type="number" value={age} onChange={e => setAge(e.target.value)} placeholder="18" style={inputStyle} />
          </div>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Starting Rank</label>
            <select value={startRank} onChange={e => setStartRank(e.target.value)} style={{ ...inputStyle, cursor: "pointer" }}>
              {ALL_RANKS.map(rk => <option key={rk} value={rk}>{rk}</option>)}
            </select>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>Most new enlistees start at E-1. Prior service or college credits may start higher.</div>
          </div>
        </div>
      </div>

      {/* Service Details */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "20px", marginBottom: "12px" }}>
        <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, marginBottom: "12px", textTransform: "uppercase", letterSpacing: "0.5px" }}>Service Details</div>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: "12px" }}>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Enlistment Length</label>
            <select value={enlistYears} onChange={e => setEnlistYears(+e.target.value)} style={{ ...inputStyle, cursor: "pointer" }}>
              {[4, 6, 8, 10, 12, 15, 20].map(y => <option key={y} value={y}>{y + " years" + (y >= 20 ? " (full career)" : "")}</option>)}
            </select>
          </div>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Duty Station</label>
            <select value={dutyStation} onChange={e => setDutyStation(e.target.value)} style={{ ...inputStyle, cursor: "pointer" }}>
              {Object.keys(BAH_SAMPLES).map(s => <option key={s} value={s}>{s + (s !== "Custom Amount" ? " \u2014 $" + BAH_SAMPLES[s] + "/mo" : "")}</option>)}
            </select>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>
              {"Sets your BAH (housing allowance) \u2014 tax-free payment for off-base housing."}
              {dutyStation !== "Custom Amount" && <span style={{ color: t.accentText }}>{" $" + bah.toLocaleString() + "/mo"}</span>}
            </div>
          </div>
        </div>
        {dutyStation === "Custom Amount" && (
          <div style={{ maxWidth: "250px", marginTop: "12px" }}>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Custom BAH Amount</label>
            <div style={{ position: "relative" }}>
              <span style={{ position: "absolute", left: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "13px", pointerEvents: "none" }}>$</span>
              <input type="number" value={customBAH} onChange={e => setCustomBAH(e.target.value)} placeholder="1500" style={{ ...inputStyle, paddingLeft: "26px" }} />
            </div>
          </div>
        )}
      </div>

      {/* Rank Progression & Bonuses */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "20px", marginBottom: "12px" }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: "6px" }}>
          <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, textTransform: "uppercase", letterSpacing: "0.5px" }}>Rank Progression & Bonuses</div>
          <button onClick={() => setShowProgression(!showProgression)} style={{ background: showProgression ? t.accentBg : "transparent", border: "1px solid " + (showProgression ? t.accentBorder : t.border), borderRadius: "5px", padding: "4px 10px", cursor: "pointer", color: showProgression ? t.accentText : t.textMuted, fontSize: "10px", fontFamily: "inherit" }}>
            {showProgression ? "Hide" : "Customize"}
          </button>
        </div>
        <p style={{ fontSize: "11px", color: t.textMuted, lineHeight: "1.5", marginBottom: showProgression ? "12px" : "0" }}>
          Ranks auto-promote based on typical timelines. Click Customize to adjust ranks or add bonuses for specific years (re-enlistment, special duty pay, sign-on, etc).
        </p>
        {showProgression && (
          <div style={{ overflowX: "auto" }}>
            <div style={{ display: "grid", gridTemplateColumns: "repeat(" + Math.min(enlistYears, 10) + ", 1fr)", gap: "6px", minWidth: enlistYears > 6 ? "600px" : "auto" }}>
              {ranks.map(function(rk, i) { return (
                <div key={i} style={{ background: t.bg, borderRadius: "6px", padding: "8px", border: "1px solid " + t.border }}>
                  <div style={{ fontSize: "9px", color: t.textMuted, textTransform: "uppercase", marginBottom: "4px" }}>{"Yr " + (i + 1) + " (age " + (startAge + i) + ")"}</div>
                  <select value={rk} onChange={function(e) { setRankForYear(i, e.target.value) }} style={{ width: "100%", padding: "4px", fontSize: "12px", fontFamily: "inherit", border: "1px solid " + t.inputBorder, borderRadius: "4px", background: t.inputBg, color: t.text, cursor: "pointer", outline: "none", marginBottom: "4px" }}>
                    {ALL_RANKS.map(r2 => <option key={r2} value={r2}>{r2}</option>)}
                  </select>
                  <div style={{ position: "relative" }}>
                    <span style={{ position: "absolute", left: "6px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "10px", pointerEvents: "none" }}>$</span>
                    <input type="number" value={bonusList[i]} onChange={function(e) { setBonusForYear(i, e.target.value) }} placeholder="0" style={{ width: "100%", padding: "4px 4px 4px 18px", fontSize: "11px", fontFamily: "inherit", border: "1px solid " + t.inputBorder, borderRadius: "4px", background: t.inputBg, color: t.text, outline: "none" }} />
                  </div>
                  <div style={{ fontSize: "8px", color: t.textMuted, marginTop: "2px" }}>bonus</div>
                </div>
              )})}
            </div>
            {enlistYears > 10 && (
              <div style={{ display: "grid", gridTemplateColumns: "repeat(10, 1fr)", gap: "6px", marginTop: "6px", minWidth: "600px" }}>
                {ranks.slice(10).map(function(rk, i) { var idx = i + 10; return (
                  <div key={idx} style={{ background: t.bg, borderRadius: "6px", padding: "8px", border: "1px solid " + t.border }}>
                    <div style={{ fontSize: "9px", color: t.textMuted, textTransform: "uppercase", marginBottom: "4px" }}>{"Yr " + (idx + 1)}</div>
                    <select value={rk} onChange={function(e) { setRankForYear(idx, e.target.value) }} style={{ width: "100%", padding: "4px", fontSize: "12px", fontFamily: "inherit", border: "1px solid " + t.inputBorder, borderRadius: "4px", background: t.inputBg, color: t.text, cursor: "pointer", outline: "none", marginBottom: "4px" }}>
                      {ALL_RANKS.map(r2 => <option key={r2} value={r2}>{r2}</option>)}
                    </select>
                    <div style={{ position: "relative" }}>
                      <span style={{ position: "absolute", left: "6px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "10px", pointerEvents: "none" }}>$</span>
                      <input type="number" value={bonusList[idx]} onChange={function(e) { setBonusForYear(idx, e.target.value) }} placeholder="0" style={{ width: "100%", padding: "4px 4px 4px 18px", fontSize: "11px", fontFamily: "inherit", border: "1px solid " + t.inputBorder, borderRadius: "4px", background: t.inputBg, color: t.text, outline: "none" }} />
                    </div>
                    <div style={{ fontSize: "8px", color: t.textMuted, marginTop: "2px" }}>bonus</div>
                  </div>
                )})}
              </div>
            )}
          </div>
        )}
      </div>

      {/* TSP Match */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "20px", marginBottom: "12px" }}>
        <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, marginBottom: "6px", textTransform: "uppercase", letterSpacing: "0.5px" }}>TSP (Military 401k)</div>
        <p style={{ fontSize: "11px", color: t.textMuted, lineHeight: "1.5", marginBottom: "12px" }}>
          The Thrift Savings Plan is the military retirement account. The government automatically contributes 1% of your base pay, then matches your contributions up to 5%. This is free money.
        </p>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: "12px" }}>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>TSP Matching</label>
            <button onClick={function() { setTspMatch(!tspMatch) }} style={{ ...inputStyle, cursor: "pointer", textAlign: "center", fontSize: "12px", fontWeight: "500", background: tspMatch ? t.accentBg : t.inputBg, color: tspMatch ? t.accentText : t.textMuted, borderColor: tspMatch ? t.accentBorder : t.inputBorder }}>
              {tspMatch ? "On \u2014 Government matching enabled" : "Off \u2014 No TSP contributions"}
            </button>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>Auto-enrolled after 60 days of service. Turn this on (you should).</div>
          </div>
          {tspMatch && (
            <div>
              <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Your TSP Contribution</label>
              <div style={{ position: "relative" }}>
                <input type="number" value={tspContribPct} onChange={function(e) { setTspContribPct(e.target.value) }} placeholder="5" style={{ ...inputStyle, paddingRight: "48px" }} />
                <span style={{ position: "absolute", right: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "12px", pointerEvents: "none" }}>% pay</span>
              </div>
              <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>{"Contribute at least 5% to get full match. Gov adds ~$" + (yearlyData[0] ? yearlyData[0].govMatch : 0) + "/mo free."}</div>
            </div>
          )}
        </div>
        {tspMatch && totalGovMatchAll > 0 && (
          <div style={{ marginTop: "10px", padding: "8px 12px", background: t.accentBg, border: "1px solid " + t.accentBorder, borderRadius: "6px" }}>
            <span style={{ fontSize: "12px", color: t.accentText, fontWeight: "600" }}>{"Free money from TSP match: $" + totalGovMatchAll.toLocaleString() + " over " + enlistYears + " years"}</span>
          </div>
        )}
      </div>

      {/* Budget */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "20px", marginBottom: "12px" }}>
        <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, marginBottom: "4px", textTransform: "uppercase", letterSpacing: "0.5px" }}>Your Budget</div>
        <p style={{ fontSize: "11px", color: t.textMuted, marginBottom: "12px", lineHeight: "1.5" }}>
          In barracks (first ~3 years), housing and food are covered. Everything else can be invested.
        </p>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr 1fr", gap: "12px" }}>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Monthly Personal Spending</label>
            <div style={{ position: "relative" }}>
              <span style={{ position: "absolute", left: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "13px", pointerEvents: "none" }}>$</span>
              <input type="number" value={monthlyExpenses} onChange={e => setMonthlyExpenses(e.target.value)} placeholder="300" style={{ ...inputStyle, paddingLeft: "26px" }} />
            </div>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>Phone, gas, subscriptions, eating out</div>
          </div>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Side Income (optional)</label>
            <div style={{ position: "relative" }}>
              <span style={{ position: "absolute", left: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "13px", pointerEvents: "none" }}>$</span>
              <input type="number" value={sideHustle} onChange={e => setSideHustle(e.target.value)} placeholder="0" style={{ ...inputStyle, paddingLeft: "26px" }} />
            </div>
          </div>
          <div>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Expected Investment Return</label>
            <div style={{ position: "relative" }}>
              <input type="number" value={investRate} step={0.5} onChange={e => setInvestRate(e.target.value)} placeholder="10" style={{ ...inputStyle, paddingRight: "28px" }} />
              <span style={{ position: "absolute", right: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "13px", pointerEvents: "none" }}>%</span>
            </div>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>S&P 500 averages ~10%/yr</div>
          </div>
        </div>
        <button onClick={function() { setShowAdvanced(!showAdvanced) }} style={{ marginTop: "14px", background: "transparent", border: "none", color: t.textMuted, fontSize: "11px", cursor: "pointer", fontFamily: "inherit", display: "flex", alignItems: "center", gap: "4px" }}>
          <span style={{ transform: showAdvanced ? "rotate(90deg)" : "rotate(0)", transition: "transform 0.2s", display: "inline-block" }}>{"\u25B8"}</span>
          {showAdvanced ? "Hide" : "Show"}{" Advanced Options"}
        </button>
        {showAdvanced && (
          <div style={{ marginTop: "10px" }}>
            <label style={{ display: "block", fontSize: "11px", fontWeight: "500", color: t.textSecondary, marginBottom: "4px" }}>Post-Military Monthly Investment</label>
            <div style={{ position: "relative", maxWidth: "250px" }}>
              <span style={{ position: "absolute", left: "11px", top: "50%", transform: "translateY(-50%)", color: t.textMuted, fontSize: "13px", pointerEvents: "none" }}>$</span>
              <input type="number" value={postMilContrib} onChange={e => setPostMilContrib(e.target.value)} placeholder="1500" style={{ ...inputStyle, paddingLeft: "26px" }} />
            </div>
            <div style={{ fontSize: "10px", color: t.textMuted, marginTop: "3px" }}>How much you invest monthly after service. Used for long-term projections.</div>
          </div>
        )}
      </div>

      {/* RESULTS */}
      <div style={{ fontSize: "12px", fontWeight: "600", color: t.accentText, marginBottom: "8px", marginTop: "20px", textTransform: "uppercase", letterSpacing: "0.5px" }}>Your Projection</div>

      <div style={{ background: t.surface, borderRadius: "8px", border: "1px solid " + t.border, padding: "14px 16px", marginBottom: "12px" }}>
        <p style={{ fontSize: "11px", color: t.textSecondary, lineHeight: "1.6", margin: 0 }}>
          <span style={{ fontWeight: "600", color: t.text }}>How this works:</span>{" Base pay is set by rank. First ~3 years: barracks (housing + food covered). After: BAH kicks in, we assume ~40% spent on rent. TSP contributions and government match are included. Everything you don\u2019t spend gets invested."}
        </p>
      </div>

      <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr 1fr", gap: "8px", marginBottom: "12px" }}>
        {[
          ["Portfolio at Separation", "Age " + (lastYr ? lastYr.age : "--"), fmt(lastYr ? lastYr.portfolio : 0), t.accent],
          ["You Invested", "Including TSP + match", fmt(lastYr ? lastYr.totalInvested : 0), t.blue],
          ["Investment Growth", "Compound returns", fmt((lastYr ? lastYr.portfolio : 0) - (lastYr ? lastYr.totalInvested : 0)), t.green],
        ].map(function(item) { var title=item[0], sub=item[1], v=item[2], c=item[3]; return (
          <div key={title} style={{ background: t.surface, border: "1px solid " + t.border, borderRadius: "8px", padding: "12px", textAlign: "center" }}>
            <div style={{ fontSize: "10px", color: t.textMuted, textTransform: "uppercase", letterSpacing: "0.5px", marginBottom: "2px" }}>{title}</div>
            <div style={{ fontSize: "20px", fontWeight: "700", color: c, marginBottom: "2px" }}>{v}</div>
            <div style={{ fontSize: "10px", color: t.textMuted }}>{sub}</div>
          </div>
        )})}
      </div>

      {milestone1M && (
        <div style={{ background: t.accentBg, border: "1px solid " + t.accentBorder, borderRadius: "8px", padding: "12px 16px", marginBottom: "16px", textAlign: "center" }}>
          <span style={{ fontSize: "14px", color: t.accentText, fontWeight: "700" }}>{"Millionaire by age " + milestone1M.age}</span>
          <span style={{ fontSize: "12px", color: t.textMuted, marginLeft: "8px" }}>{"at " + num(investRate) + "% annual returns"}</span>
        </div>
      )}

      <canvas ref={canvasRef} style={{ width: "100%", height: "280px", borderRadius: "8px", background: t.bg, border: "1px solid " + t.border, marginBottom: "8px" }} />
      <div style={{ display: "flex", gap: "16px", justifyContent: "center", marginBottom: "20px" }}>
        {[[t.accent, "During Service"], [t.green, "After Service"], [t.blue + "40", "Contributions"]].map(function(item) { return (
          <div key={item[1]} style={{ display: "flex", alignItems: "center", gap: "5px" }}>
            <div style={{ width: "14px", height: "3px", background: item[0], borderRadius: "2px" }}></div>
            <span style={{ fontSize: "10px", color: t.textMuted }}>{item[1]}</span>
          </div>
        )})}
      </div>

      {/* Table */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, overflow: "hidden", marginBottom: "12px" }}>
        <div style={{ padding: "12px 16px", borderBottom: "1px solid " + t.borderLight }}>
          <h3 style={{ fontSize: "13px", fontWeight: "600", margin: 0 }}>Year-by-Year Breakdown</h3>
        </div>
        <div style={{ overflowX: "auto" }}>
          <table style={{ width: "100%", borderCollapse: "collapse", fontSize: "11px" }}>
            <thead>
              <tr style={{ borderBottom: "1px solid " + t.border }}>
                {["Yr","Age","Rank","Base Pay","BAH","TSP","Match","Invest/mo","Bonus","Portfolio"].map(function(h) { return (
                  <th key={h} style={{ padding: "7px 8px", textAlign: "right", color: t.textMuted, fontWeight: "500", fontSize: "9px", textTransform: "uppercase", letterSpacing: "0.5px", whiteSpace: "nowrap" }}>{h}</th>
                )})}
              </tr>
            </thead>
            <tbody>
              {yearlyData.map(function(d, i) { return (
                <tr key={i} style={{ borderBottom: "1px solid " + t.borderLight }}>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: t.textMuted }}>{d.year}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right" }}>{d.age}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: t.accentText, fontWeight: "500" }}>{d.rank}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right" }}>{"$" + d.basePay.toLocaleString()}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: d.bah > 0 ? t.green : t.textMuted }}>{d.bah > 0 ? "$" + d.bah.toLocaleString() : "Barracks"}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: d.tspContrib > 0 ? t.text : t.textMuted }}>{d.tspContrib > 0 ? "$" + d.tspContrib : "\u2014"}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: d.govMatch > 0 ? t.green : t.textMuted }}>{d.govMatch > 0 ? "+$" + d.govMatch : "\u2014"}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", fontWeight: "500" }}>{"$" + d.totalMonthly.toLocaleString()}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", color: d.bonus > 0 ? t.accent : t.textMuted }}>{d.bonus > 0 ? "$" + d.bonus.toLocaleString() : "\u2014"}</td>
                  <td style={{ padding: "7px 8px", textAlign: "right", fontWeight: "700", color: t.accentText }}>{fmt(d.portfolio)}</td>
                </tr>
              )})}
            </tbody>
          </table>
        </div>
      </div>

      {/* Post-military */}
      {postYears.length > 0 && (
        <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, overflow: "hidden", marginBottom: "12px" }}>
          <div style={{ padding: "12px 16px", borderBottom: "1px solid " + t.borderLight }}>
            <h3 style={{ fontSize: "13px", fontWeight: "600", margin: 0 }}>After You Separate</h3>
            <p style={{ fontSize: "10px", color: t.textMuted, margin: "3px 0 0" }}>
              {"Assumes $" + num(postMilContrib).toLocaleString() + "/mo continued investment at " + num(investRate) + "% returns."}
            </p>
          </div>
          <div style={{ padding: "4px 0" }}>
            {postYears.filter(function(_, i) { return [0, 2, 4, 7, 9, 14, 19].includes(i) }).map(function(d, i) { return (
              <div key={i} style={{ display: "flex", justifyContent: "space-between", alignItems: "center", padding: "8px 16px", borderBottom: "1px solid " + t.borderLight }}>
                <div>
                  <span style={{ fontSize: "12px", color: t.textSecondary }}>{"Age " + d.age}</span>
                  <span style={{ fontSize: "10px", color: t.textMuted, marginLeft: "8px" }}>{(d.age - startAge - enlistYears) + " yr" + ((d.age - startAge - enlistYears) !== 1 ? "s" : "") + " after"}</span>
                </div>
                <span style={{ fontSize: "14px", fontWeight: "700", color: d.portfolio >= 1000000 ? t.green : t.text }}>{fmt(d.portfolio)}</span>
              </div>
            )})}
          </div>
        </div>
      )}

      {/* What military covers */}
      <div style={{ background: t.surface, borderRadius: "9px", border: "1px solid " + t.border, padding: "16px 18px", marginBottom: "12px" }}>
        <div style={{ fontSize: "12px", fontWeight: "600", color: t.text, marginBottom: "10px" }}>What the military covers (not shown above)</div>
        <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: "8px" }}>
          {[
            ["Housing", "Barracks or BAH covers rent"],
            ["Food", "Meal halls or BAS (~$400/mo allowance)"],
            ["Healthcare", "Full medical, dental, vision \u2014 $0 cost"],
            ["Education", "GI Bill: full tuition + ~$2k/mo housing"],
            ["Tax Benefits", "BAH/BAS tax-free. Combat = all tax-free"],
            ["TSP Match", "Gov matches up to 5% of base pay"],
          ].map(function(item) { return (
            <div key={item[0]} style={{ padding: "10px", borderRadius: "6px", background: t.bg, border: "1px solid " + t.border }}>
              <div style={{ fontSize: "11px", fontWeight: "600", color: t.accentText, marginBottom: "2px" }}>{item[0]}</div>
              <div style={{ fontSize: "10px", color: t.textMuted, lineHeight: "1.4" }}>{item[1]}</div>
            </div>
          )})}
        </div>
      </div>

      <div style={{ padding: "10px 12px", background: t.tipBg, border: "1px solid " + t.tipBorder, borderRadius: "6px" }}>
        <div style={{ fontSize: "10px", fontWeight: "600", color: t.tipText, marginBottom: "2px" }}>The Strategy</div>
        <p style={{ fontSize: "11px", color: t.tipText, lineHeight: "1.6", margin: 0, opacity: 0.9 }}>
          {"Keep spending low. Always contribute at least 5% to TSP for full match \u2014 it\u2019s free money. When you get BAH, rent a room for 30-40% and invest the rest. Combined with free healthcare, food, and compound interest, you have an advantage most civilians never will."}
        </p>
      </div>
    </div>
  );
}

// ===================== DEBT PAYOFF =====================
function DebtPayoff({t}) {
  const [debts, setDebts] = useState([{name:"Credit Card",balance:"5000",rate:"22",minPay:"150"},{name:"Car Loan",balance:"12000",rate:"6.5",minPay:"300"}]);
  const [method, setMethod] = useState("avalanche");
  const [extraPay, setExtraPay] = useState("200");
  const num = v => parseFloat(v) || 0;
  const addDebt = () => setDebts([...debts, {name:"Debt "+(debts.length+1),balance:"",rate:"",minPay:""}]);
  const removeDebt = i => setDebts(debts.filter((_,j)=>j!==i));
  const updateDebt = (i,k,v) => { const n=[...debts]; n[i]={...n[i],[k]:v}; setDebts(n); };
  const is = {width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};

  const calculate = () => {
    let active = debts.map((d,i)=>({i,name:d.name,bal:num(d.balance),rate:num(d.rate)/100/12,min:num(d.minPay),paid:0,months:0})).filter(d=>d.bal>0);
    if(active.length===0) return {months:0,totalPaid:0,totalInterest:0,timeline:[]};
    const sorted = method==="avalanche" ? [...active].sort((a,b)=>b.rate-a.rate) : [...active].sort((a,b)=>a.bal-b.bal);
    let months=0, totalPaid=0, totalInterest=0, timeline=[], extra=num(extraPay);
    while(sorted.some(d=>d.bal>0) && months<600) {
      months++;
      let extraLeft=extra;
      for(const d of sorted) {
        if(d.bal<=0) continue;
        const interest=d.bal*d.rate;
        totalInterest+=interest;
        d.bal+=interest;
        const pay=Math.min(d.bal,d.min);
        d.bal-=pay; totalPaid+=pay;
      }
      for(const d of sorted) {
        if(d.bal<=0||extraLeft<=0) continue;
        const pay=Math.min(d.bal,extraLeft);
        d.bal-=pay; extraLeft-=pay; totalPaid+=pay;
      }
      if(months%3===0||sorted.every(d=>d.bal<=0)) timeline.push({month:months,remaining:sorted.reduce((s,d)=>s+Math.max(0,d.bal),0)});
    }
    return {months,totalPaid:Math.round(totalPaid),totalInterest:Math.round(totalInterest),timeline};
  };
  const result = calculate();
  const noExtra = (() => { let a=debts.map(d=>({bal:num(d.balance),rate:num(d.rate)/100/12,min:num(d.minPay)})).filter(d=>d.bal>0),m=0,ti=0;
    while(a.some(d=>d.bal>0)&&m<600){m++;for(const d of a){if(d.bal<=0)continue;const i=d.bal*d.rate;ti+=i;d.bal=Math.max(0,d.bal+i-d.min)}} return{months:m,interest:Math.round(ti)}})();
  const fmt=n=>"$"+n.toLocaleString();
  const saved=noExtra.interest-result.totalInterest;
  return (
    <div style={{maxWidth:"750px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Debt Payoff Calculator</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>Add your debts below. Choose snowball (smallest balance first) or avalanche (highest interest first) and see how fast you can be debt-free.</p>
      </div>
      <div style={{display:"flex",gap:"6px",marginBottom:"14px"}}>
        {["avalanche","snowball"].map(m=><button key={m} onClick={()=>setMethod(m)} style={{padding:"6px 14px",fontSize:"12px",fontWeight:"500",border:"1px solid "+(method===m?t.accentBorder:t.border),borderRadius:"6px",cursor:"pointer",fontFamily:"inherit",background:method===m?t.accentBg:"transparent",color:method===m?t.accentText:t.textMuted}}>
          {m==="avalanche"?"Avalanche (highest interest first)":"Snowball (smallest balance first)"}
        </button>)}
      </div>
      {debts.map((d,i)=>(
        <div key={i} style={{background:t.surface,borderRadius:"8px",border:"1px solid "+t.border,padding:"14px",marginBottom:"8px"}}>
          <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:"8px"}}>
            <input value={d.name} onChange={e=>updateDebt(i,"name",e.target.value)} style={{...is,maxWidth:"200px",fontWeight:"600"}} />
            {debts.length>1&&<button onClick={()=>removeDebt(i)} style={{background:"transparent",border:"none",color:t.textMuted,cursor:"pointer",fontSize:"14px"}}>&#10005;</button>}
          </div>
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"10px"}}>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Balance</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={d.balance} onChange={e=>updateDebt(i,"balance",e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Interest Rate</label><div style={{position:"relative"}}><input type="number" value={d.rate} onChange={e=>updateDebt(i,"rate",e.target.value)} style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Min Payment</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={d.minPay} onChange={e=>updateDebt(i,"minPay",e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          </div>
        </div>
      ))}
      <div style={{display:"flex",gap:"10px",alignItems:"center",marginBottom:"16px"}}>
        <button onClick={addDebt} style={{padding:"7px 14px",fontSize:"12px",background:t.surface,border:"1px solid "+t.border,borderRadius:"6px",cursor:"pointer",color:t.textSecondary,fontFamily:"inherit"}}>+ Add Debt</button>
        <div style={{flex:1}}></div>
        <label style={{fontSize:"11px",color:t.textSecondary}}>Extra monthly payment:</label>
        <div style={{position:"relative",width:"120px"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={extraPay} onChange={e=>setExtraPay(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Debt Free In",result.months<600?Math.floor(result.months/12)+"yr "+result.months%12+"mo":"Never",t.accent],["Total Interest",fmt(result.totalInterest),t.red],["Interest Saved",fmt(Math.max(0,saved)),t.green],["Months Saved",(noExtra.months-result.months)+" months",t.blue]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"16px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>Avalanche saves the most money. Snowball gives faster wins to stay motivated. Both beat minimum payments. The extra payment is the real weapon.</p>
      </div>
    </div>
  );
}

// ===================== BUDGET BUILDER =====================
function BudgetBuilder({t}) {
  const [income, setIncome] = useState("4000");
  const [cats, setCats] = useState([{name:"Rent/Housing",amount:"1200"},{name:"Food/Groceries",amount:"400"},{name:"Transportation",amount:"300"},{name:"Utilities",amount:"150"},{name:"Insurance",amount:"200"},{name:"Subscriptions",amount:"50"},{name:"Personal",amount:"200"},{name:"Savings/Investing",amount:"500"}]);
  const num=v=>parseFloat(v)||0;
  const addCat=()=>setCats([...cats,{name:"Category",amount:""}]);
  const removeCat=i=>setCats(cats.filter((_,j)=>j!==i));
  const updateCat=(i,k,v)=>{const n=[...cats];n[i]={...n[i],[k]:v};setCats(n)};
  const totalExp=cats.reduce((s,c)=>s+num(c.amount),0);
  const remaining=num(income)-totalExp;
  const savingsRate=num(income)>0?((num(income)-totalExp)/num(income)*100):0;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const colors=[t.accent,t.blue,t.green,t.red,t.purple,t.orange,"#e879a0","#67d4c0","#a3a3a3"];
  return (
    <div style={{maxWidth:"700px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Budget Builder</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>See where your money goes. Enter your monthly income and expenses to find your savings rate and leftover cash flow.</p>
      </div>
      <div style={{marginBottom:"14px"}}>
        <label style={{fontSize:"11px",fontWeight:"500",color:t.textSecondary,display:"block",marginBottom:"4px"}}>Monthly Take-Home Income</label>
        <div style={{position:"relative",maxWidth:"250px"}}><span style={{position:"absolute",left:"10px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"13px"}}>$</span><input type="number" value={income} onChange={e=>setIncome(e.target.value)} style={{...is,paddingLeft:"24px"}} /></div>
      </div>
      <div style={{display:"flex",flexDirection:"column",gap:"6px",marginBottom:"14px"}}>
        {cats.map((c,i)=>(
          <div key={i} style={{display:"flex",gap:"8px",alignItems:"center"}}>
            <div style={{width:"8px",height:"8px",borderRadius:"50%",background:colors[i%colors.length],flexShrink:0}}></div>
            <input value={c.name} onChange={e=>updateCat(i,"name",e.target.value)} style={{...is,flex:1,maxWidth:"200px"}} />
            <div style={{position:"relative",width:"130px"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={c.amount} onChange={e=>updateCat(i,"amount",e.target.value)} placeholder="0" style={{...is,paddingLeft:"22px"}} /></div>
            <div style={{fontSize:"11px",color:t.textMuted,width:"40px",textAlign:"right"}}>{num(income)>0?(num(c.amount)/num(income)*100).toFixed(0)+"%":""}</div>
            {cats.length>1&&<button onClick={()=>removeCat(i)} style={{background:"transparent",border:"none",color:t.textMuted,cursor:"pointer",fontSize:"13px"}}>&#10005;</button>}
          </div>
        ))}
        <button onClick={addCat} style={{padding:"6px 12px",fontSize:"11px",background:t.surface,border:"1px solid "+t.border,borderRadius:"5px",cursor:"pointer",color:t.textSecondary,fontFamily:"inherit",alignSelf:"flex-start",marginTop:"4px"}}>+ Add Category</button>
      </div>
      {/* Bar */}
      {num(income)>0&&<div style={{background:t.bg,borderRadius:"8px",border:"1px solid "+t.border,overflow:"hidden",height:"32px",display:"flex",marginBottom:"14px"}}>
        {cats.map((c,i)=>{const pct=num(c.amount)/num(income)*100;return pct>0?<div key={i} title={c.name+": "+pct.toFixed(1)+"%"} style={{width:pct+"%",height:"100%",background:colors[i%colors.length],minWidth:"2px"}}></div>:null})}
        {remaining>0&&<div style={{flex:1,height:"100%",background:t.green+"30"}}></div>}
      </div>}
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Total Expenses","$"+totalExp.toLocaleString(),t.text],["Remaining","$"+remaining.toLocaleString(),remaining>=0?t.green:t.red],["Savings Rate",savingsRate.toFixed(1)+"%",savingsRate>=20?t.green:savingsRate>=10?t.accent:t.red]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"18px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>Aim for 20%+ savings rate. 50/30/20 rule: 50% needs, 30% wants, 20% savings. Track this monthly and your net worth compounds fast.</p>
      </div>
    </div>
  );
}

// ===================== NET WORTH TRACKER =====================
function NetWorthTracker({t}) {
  const [assets, setAssets] = useState([{name:"Checking Account",value:"3000"},{name:"Savings",value:"8000"},{name:"Investments/TSP",value:"15000"},{name:"Car Value",value:"12000"}]);
  const [liabilities, setLiabilities] = useState([{name:"Car Loan",value:"8000"},{name:"Credit Card",value:"2000"}]);
  const num=v=>parseFloat(v)||0;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const totalA=assets.reduce((s,a)=>s+num(a.value),0);
  const totalL=liabilities.reduce((s,l)=>s+num(l.value),0);
  const netWorth=totalA-totalL;
  const fmt=n=>(n<0?"-$"+Math.abs(n).toLocaleString():"$"+n.toLocaleString());
  const updateA=(i,k,v)=>{const n=[...assets];n[i]={...n[i],[k]:v};setAssets(n)};
  const updateL=(i,k,v)=>{const n=[...liabilities];n[i]={...n[i],[k]:v};setLiabilities(n)};
  return (
    <div style={{maxWidth:"700px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Net Worth Tracker</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>Everything you own minus everything you owe. This single number is the best measure of your financial health.</p>
      </div>
      <div style={{background:netWorth>=0?t.accentBg:"rgba(224,85,85,0.08)",border:"1px solid "+(netWorth>=0?t.accentBorder:"rgba(224,85,85,0.2)"),borderRadius:"10px",padding:"20px",textAlign:"center",marginBottom:"16px"}}>
        <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"1px",marginBottom:"4px"}}>Your Net Worth</div>
        <div style={{fontSize:"32px",fontWeight:"700",color:netWorth>=0?t.green:t.red}}>{fmt(netWorth)}</div>
        <div style={{display:"flex",justifyContent:"center",gap:"24px",marginTop:"8px"}}>
          <span style={{fontSize:"12px",color:t.textSecondary}}>{"Assets: "+fmt(totalA)}</span>
          <span style={{fontSize:"12px",color:t.textSecondary}}>{"Debts: "+fmt(totalL)}</span>
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"12px",marginBottom:"14px"}}>
        <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"16px"}}>
          <div style={{fontSize:"12px",fontWeight:"600",color:t.green,marginBottom:"10px"}}>Assets (what you own)</div>
          {assets.map((a,i)=>(
            <div key={i} style={{display:"flex",gap:"6px",marginBottom:"6px",alignItems:"center"}}>
              <input value={a.name} onChange={e=>updateA(i,"name",e.target.value)} style={{...is,flex:1,fontSize:"12px"}} />
              <div style={{position:"relative",width:"110px"}}><span style={{position:"absolute",left:"7px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"11px"}}>$</span><input type="number" value={a.value} onChange={e=>updateA(i,"value",e.target.value)} style={{...is,paddingLeft:"20px",fontSize:"12px"}} /></div>
              {assets.length>1&&<button onClick={()=>setAssets(assets.filter((_,j)=>j!==i))} style={{background:"transparent",border:"none",color:t.textMuted,cursor:"pointer",fontSize:"12px"}}>&#10005;</button>}
            </div>
          ))}
          <button onClick={()=>setAssets([...assets,{name:"Asset",value:""}])} style={{fontSize:"11px",background:"transparent",border:"1px solid "+t.border,borderRadius:"4px",padding:"4px 10px",cursor:"pointer",color:t.textMuted,fontFamily:"inherit",marginTop:"4px"}}>+ Add</button>
        </div>
        <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"16px"}}>
          <div style={{fontSize:"12px",fontWeight:"600",color:t.red,marginBottom:"10px"}}>Liabilities (what you owe)</div>
          {liabilities.map((l,i)=>(
            <div key={i} style={{display:"flex",gap:"6px",marginBottom:"6px",alignItems:"center"}}>
              <input value={l.name} onChange={e=>updateL(i,"name",e.target.value)} style={{...is,flex:1,fontSize:"12px"}} />
              <div style={{position:"relative",width:"110px"}}><span style={{position:"absolute",left:"7px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"11px"}}>$</span><input type="number" value={l.value} onChange={e=>updateL(i,"value",e.target.value)} style={{...is,paddingLeft:"20px",fontSize:"12px"}} /></div>
              {liabilities.length>1&&<button onClick={()=>setLiabilities(liabilities.filter((_,j)=>j!==i))} style={{background:"transparent",border:"none",color:t.textMuted,cursor:"pointer",fontSize:"12px"}}>&#10005;</button>}
            </div>
          ))}
          <button onClick={()=>setLiabilities([...liabilities,{name:"Debt",value:""}])} style={{fontSize:"11px",background:"transparent",border:"1px solid "+t.border,borderRadius:"4px",padding:"4px 10px",cursor:"pointer",color:t.textMuted,fontFamily:"inherit",marginTop:"4px"}}>+ Add</button>
        </div>
      </div>
      {/* Milestones */}
      <div style={{background:t.surface,borderRadius:"8px",border:"1px solid "+t.border,padding:"14px 16px"}}>
        <div style={{fontSize:"11px",fontWeight:"600",color:t.text,marginBottom:"8px"}}>Milestones</div>
        <div style={{display:"flex",gap:"6px",flexWrap:"wrap"}}>
          {[0,10000,25000,50000,100000,250000,500000,1000000].map(function(m){const hit=netWorth>=m;return(
            <div key={m} style={{padding:"5px 10px",borderRadius:"5px",fontSize:"11px",fontWeight:"500",background:hit?t.accentBg:t.bg,border:"1px solid "+(hit?t.accentBorder:t.border),color:hit?t.accentText:t.textMuted}}>
              {m===0?"Positive NW":m>=1e6?"$1M":"$"+m.toLocaleString()}{hit?" \u2713":""}
            </div>
          )})}
        </div>
      </div>
    </div>
  );
}

// ===================== REAL ESTATE =====================
function RealEstateCalc({t}) {
  const [tab, setTab] = useState("mortgage");
  const num=v=>parseFloat(v)||0;
  const [price,setPrice]=useState("300000");const[down,setDown]=useState("20");const[mRate,setMRate]=useState("6.5");const[term,setTerm]=useState("30");const[propTax,setPropTax]=useState("1.2");const[insurance,setInsurance]=useState("150");
  const [rent,setRent]=useState("1500");const[rentInc,setRentInc]=useState("3");const[investReturn,setInvestReturn]=useState("10");const[stayYears,setStayYears]=useState("7");
  const downAmt=num(price)*num(down)/100;const loan=num(price)-downAmt;const mr=num(mRate)/100/12;const n=num(term)*12;
  const monthlyPI=mr>0?loan*(mr*Math.pow(1+mr,n))/(Math.pow(1+mr,n)-1):loan/n;
  const monthlyTax=num(price)*num(propTax)/100/12;const totalMonthly=monthlyPI+monthlyTax+num(insurance);
  const totalPaid=monthlyPI*n;const totalInterest=totalPaid-loan;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const fmt=n2=>"$"+Math.round(n2).toLocaleString();
  // Rent vs buy
  const yrs=num(stayYears);const buyMonthly=totalMonthly;const rentMonthly=num(rent);
  let rentCost=0,buyCost=0,investGain=0;const ri=num(investReturn)/100/12;const rInc=num(rentInc)/100;
  let curRent=rentMonthly;
  for(let y=0;y<yrs;y++){for(let m=0;m<12;m++){rentCost+=curRent;buyCost+=buyMonthly;const diff=buyMonthly>curRent?0:curRent-buyMonthly;investGain=investGain*(1+ri)+diff}curRent*=(1+rInc)}
  const equity=num(price)*0.03*yrs; // rough appreciation
  const builtEquity=loan>0?monthlyPI*yrs*12*0.3:0;
  return (
    <div style={{maxWidth:"750px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Real Estate Calculator</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>Calculate mortgage payments, compare renting vs buying, and model house-hack scenarios.</p>
      </div>
      <div style={{display:"flex",gap:"4px",marginBottom:"14px"}}>
        {[["mortgage","Mortgage"],["rentvbuy","Rent vs Buy"]].map(function(x){return <button key={x[0]} onClick={function(){setTab(x[0])}} style={{padding:"6px 14px",fontSize:"12px",fontWeight:"500",border:"1px solid "+(tab===x[0]?t.accentBorder:t.border),borderRadius:"6px",cursor:"pointer",fontFamily:"inherit",background:tab===x[0]?t.accentBg:"transparent",color:tab===x[0]?t.accentText:t.textMuted}}>{x[1]}</button>})}
      </div>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"20px",marginBottom:"14px"}}>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Home Price</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={price} onChange={e=>setPrice(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Down Payment</label><div style={{position:"relative"}}><input type="number" value={down} onChange={e=>setDown(e.target.value)} style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div><div style={{fontSize:"10px",color:t.textMuted,marginTop:"2px"}}>{fmt(downAmt)}</div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Interest Rate</label><div style={{position:"relative"}}><input type="number" value={mRate} onChange={e=>setMRate(e.target.value)} step="0.1" style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px",marginTop:"10px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Loan Term</label><select value={term} onChange={e=>setTerm(e.target.value)} style={{...is,cursor:"pointer"}}><option value="15">15 years</option><option value="20">20 years</option><option value="30">30 years</option></select></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Property Tax Rate</label><div style={{position:"relative"}}><input type="number" value={propTax} onChange={e=>setPropTax(e.target.value)} step="0.1" style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Monthly Insurance</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={insurance} onChange={e=>setInsurance(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
        </div>
      </div>
      {tab==="mortgage"&&<div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Monthly Payment",fmt(totalMonthly),t.accent],["Principal+Interest",fmt(monthlyPI),t.text],["Total Interest",fmt(totalInterest),t.red],["Loan Amount",fmt(loan),t.blue]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"9px",color:t.textMuted,textTransform:"uppercase",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"16px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>}
      {tab==="rentvbuy"&&<>
        <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"16px",marginBottom:"14px"}}>
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px"}}>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Current Rent</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={rent} onChange={e=>setRent(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Annual Rent Increase</label><div style={{position:"relative"}}><input type="number" value={rentInc} onChange={e=>setRentInc(e.target.value)} style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
            <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>How Long Staying</label><select value={stayYears} onChange={e=>setStayYears(e.target.value)} style={{...is,cursor:"pointer"}}>{[3,5,7,10,15,20].map(y=><option key={y} value={y}>{y+" years"}</option>)}</select></div>
          </div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"8px",marginBottom:"14px"}}>
          <div style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"14px"}}>
            <div style={{fontSize:"11px",fontWeight:"600",color:t.accent,marginBottom:"6px"}}>Buying</div>
            <div style={{fontSize:"12px",color:t.textSecondary,marginBottom:"3px"}}>{"Monthly: "+fmt(buyMonthly)}</div>
            <div style={{fontSize:"12px",color:t.textSecondary}}>{"Total cost over "+yrs+"yr: "+fmt(buyCost)}</div>
            <div style={{fontSize:"12px",color:t.green,marginTop:"3px"}}>{"Equity built: ~"+fmt(builtEquity+equity)}</div>
          </div>
          <div style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"14px"}}>
            <div style={{fontSize:"11px",fontWeight:"600",color:t.blue,marginBottom:"6px"}}>Renting</div>
            <div style={{fontSize:"12px",color:t.textSecondary,marginBottom:"3px"}}>{"Starting: "+fmt(rentMonthly)+"/mo"}</div>
            <div style={{fontSize:"12px",color:t.textSecondary}}>{"Total cost over "+yrs+"yr: "+fmt(rentCost)}</div>
            <div style={{fontSize:"12px",color:t.textMuted,marginTop:"3px"}}>{"No equity built"}</div>
          </div>
        </div>
      </>}
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>House hacking: buy a duplex/triplex, live in one unit, rent the others. BAH can cover the mortgage while tenants build your equity. The best real estate strategy for military members.</p>
      </div>
    </div>
  );
}

// ===================== TAX ESTIMATOR =====================
function TaxEstimator({t}) {
  const [filing, setFiling] = useState("single");
  const [incomeType, setIncomeType] = useState("w2");
  const [gross, setGross] = useState("55000");
  const [deduction, setDeduction] = useState("standard");
  const [itemized, setItemized] = useState("14600");
  const num=v=>parseFloat(v)||0;
  const stdDed = filing==="single"?14600:filing==="married"?29200:21900;
  const ded = deduction==="standard"?stdDed:num(itemized);
  const gi = num(gross);
  const se = incomeType==="1099" ? gi * 0.9235 * 0.153 : 0;
  const taxableIncome = Math.max(0, gi - ded - (incomeType==="1099" ? se/2 : 0));
  const brackets = filing==="single"?[[11600,0.10],[47150,0.12],[100525,0.22],[191950,0.24],[243725,0.32],[609350,0.35],[Infinity,0.37]]:filing==="married"?[[23200,0.10],[94300,0.12],[201050,0.22],[383900,0.24],[487450,0.32],[731200,0.35],[Infinity,0.37]]:[[16550,0.10],[63100,0.12],[100500,0.22],[191950,0.24],[243725,0.32],[609350,0.35],[Infinity,0.37]];
  let tax=0, prev=0, breakdown=[];
  for(const [cap,rate] of brackets) {
    if(taxableIncome<=prev) break;
    const taxable=Math.min(taxableIncome,cap)-prev;
    const t2=taxable*rate;
    tax+=t2;
    if(taxable>0) breakdown.push({bracket:Math.round(rate*100)+"%",taxable:Math.round(taxable),tax:Math.round(t2)});
    prev=cap;
  }
  const totalTax=Math.round(tax+se);
  const effectiveRate=gi>0?(totalTax/gi*100).toFixed(1):0;
  const takeHome=Math.round(gi-totalTax);
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const fmt=n=>"$"+n.toLocaleString();
  return (
    <div style={{maxWidth:"700px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Tax Estimator</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>Estimate your federal income tax for 2024. Covers W-2 employees and 1099 self-employed including self-employment tax.</p>
      </div>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"20px",marginBottom:"14px"}}>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px",marginBottom:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Filing Status</label><select value={filing} onChange={e=>setFiling(e.target.value)} style={{...is,cursor:"pointer"}}><option value="single">Single</option><option value="married">Married Filing Jointly</option><option value="hoh">Head of Household</option></select></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Income Type</label><select value={incomeType} onChange={e=>setIncomeType(e.target.value)} style={{...is,cursor:"pointer"}}><option value="w2">W-2 Employee</option><option value="1099">1099 Self-Employed</option></select></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Annual Gross Income</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={gross} onChange={e=>setGross(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Deduction</label><select value={deduction} onChange={e=>setDeduction(e.target.value)} style={{...is,cursor:"pointer"}}><option value="standard">{"Standard ($"+stdDed.toLocaleString()+")"}</option><option value="itemized">Itemized</option></select></div>
          {deduction==="itemized"&&<div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Itemized Amount</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={itemized} onChange={e=>setItemized(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>}
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Take Home",fmt(takeHome),t.green],["Federal Tax",fmt(Math.round(tax)),t.red],["Effective Rate",effectiveRate+"%",t.accent],incomeType==="1099"?["SE Tax",fmt(Math.round(se)),t.orange]:["Taxable Income",fmt(Math.round(taxableIncome)),t.text]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"9px",color:t.textMuted,textTransform:"uppercase",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"16px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      {breakdown.length>0&&<div style={{background:t.surface,borderRadius:"8px",border:"1px solid "+t.border,overflow:"hidden",marginBottom:"14px"}}>
        <div style={{padding:"10px 14px",borderBottom:"1px solid "+t.borderLight,fontSize:"12px",fontWeight:"600"}}>Tax Bracket Breakdown</div>
        {breakdown.map(function(b,i){return <div key={i} style={{display:"flex",justifyContent:"space-between",padding:"7px 14px",borderBottom:"1px solid "+t.borderLight}}>
          <span style={{fontSize:"12px",color:t.textSecondary}}>{b.bracket+" bracket"}</span>
          <span style={{fontSize:"12px",color:t.textMuted}}>{"on "+fmt(b.taxable)}</span>
          <span style={{fontSize:"12px",fontWeight:"600",color:t.red}}>{fmt(b.tax)}</span>
        </div>})}
      </div>}
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>Your effective rate is always lower than your bracket. A $55k salary in the 22% bracket actually pays ~12% effective. Self-employed? Set aside 25-30% of every dollar for taxes.</p>
      </div>
    </div>
  );
}

// ===================== SIDE HUSTLE =====================
function SideHustleCalc({t}) {
  const [revenue,setRevenue]=useState("3000");const[expenses,setExpenses]=useState("800");const[hours,setHours]=useState("60");const[taxRate,setTaxRate]=useState("25");
  const num=v=>parseFloat(v)||0;
  const profit=num(revenue)-num(expenses);const seTax=profit*0.9235*0.153;const incomeTax=profit*num(taxRate)/100;const net=profit-seTax-incomeTax;const hourly=num(hours)>0?net/num(hours):0;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const fmt=n=>"$"+Math.round(n).toLocaleString();
  return (
    <div style={{maxWidth:"650px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Side Hustle Profitability</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>See what your side hustle actually pays after expenses, self-employment tax, and income tax. Your real hourly rate might surprise you.</p>
      </div>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"20px",marginBottom:"14px"}}>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"12px",marginBottom:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Monthly Revenue</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={revenue} onChange={e=>setRevenue(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Monthly Expenses</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={expenses} onChange={e=>setExpenses(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Hours Worked / Month</label><input type="number" value={hours} onChange={e=>setHours(e.target.value)} style={is} /></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Est. Income Tax Bracket</label><div style={{position:"relative"}}><input type="number" value={taxRate} onChange={e=>setTaxRate(e.target.value)} style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Profit",fmt(profit),t.text],["After Taxes",fmt(net),net>0?t.green:t.red],["Real Hourly",fmt(hourly)+"/hr",t.accent],["SE Tax",fmt(seTax),t.orange]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"9px",color:t.textMuted,textTransform:"uppercase",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"16px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>If your real hourly rate is lower than a regular job would pay, the hustle only makes sense if it scales. Track your hours honestly.</p>
      </div>
    </div>
  );
}

// ===================== RETIREMENT / FIRE =====================
function RetirementCalc({t}) {
  const [age,setAge]=useState("25");const[retireAge,setRetireAge]=useState("55");const[annualSpend,setAnnualSpend]=useState("40000");const[portfolio2,setPortfolio2]=useState("50000");const[monthlyAdd,setMonthlyAdd]=useState("1500");const[retRate,setRetRate]=useState("10");const[withdrawRate,setWithdrawRate]=useState("4");
  const num=v=>parseFloat(v)||0;
  const fireNumber=num(annualSpend)/(num(withdrawRate)/100);
  const yrs=Math.max(0,num(retireAge)-num(age));
  const r=num(retRate)/100;
  let projected=num(portfolio2);for(let i=0;i<yrs;i++)projected=projected*(1+r)+num(monthlyAdd)*12;
  const funded=projected>=fireNumber;
  // How many years to FIRE from now
  let yrsToFire=0,p=num(portfolio2);while(p<fireNumber&&yrsToFire<100){p=p*(1+r)+num(monthlyAdd)*12;yrsToFire++}
  const fireAge=num(age)+yrsToFire;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const fmt=n=>n>=1e6?"$"+(n/1e6).toFixed(2)+"M":"$"+Math.round(n).toLocaleString();
  return (
    <div style={{maxWidth:"700px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Retirement / FIRE Calculator</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>FIRE = Financial Independence, Retire Early. Calculate your FIRE number and how long until you can live off your investments forever.</p>
      </div>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"20px",marginBottom:"14px"}}>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px",marginBottom:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Current Age</label><input type="number" value={age} onChange={e=>setAge(e.target.value)} style={is} /></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Current Portfolio</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={portfolio2} onChange={e=>setPortfolio2(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Monthly Investment</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={monthlyAdd} onChange={e=>setMonthlyAdd(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Annual Spending in Retirement</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={annualSpend} onChange={e=>setAnnualSpend(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Expected Return</label><div style={{position:"relative"}}><input type="number" value={retRate} onChange={e=>setRetRate(e.target.value)} style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Safe Withdrawal Rate</label><div style={{position:"relative"}}><input type="number" value={withdrawRate} onChange={e=>setWithdrawRate(e.target.value)} step="0.5" style={{...is,paddingRight:"22px"}} /><span style={{position:"absolute",right:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>%</span></div><div style={{fontSize:"10px",color:t.textMuted,marginTop:"2px"}}>4% is the standard safe rate</div></div>
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["FIRE Number",fmt(fireNumber),t.accent],["FIRE Age","Age "+fireAge,fireAge<=55?t.green:t.text],["Years to FIRE",yrsToFire<100?yrsToFire+" years":"100+",t.blue]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"14px",textAlign:"center"}}>
            <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"20px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      <div style={{background:t.surface,borderRadius:"8px",border:"1px solid "+t.border,padding:"14px 16px",marginBottom:"14px"}}>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>
          <span style={{fontWeight:"600",color:t.text}}>What this means: </span>
          {"You need "+fmt(fireNumber)+" invested to safely withdraw "+fmt(num(annualSpend))+"/yr forever. At your current pace, you\u2019ll reach that by age "+fireAge+". Your portfolio at that point: "+fmt(projected)+"."}
        </p>
      </div>
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>The two fastest ways to reach FIRE: increase income or decrease spending. Cutting $500/mo from spending both lowers your FIRE number AND increases your monthly investment.</p>
      </div>
    </div>
  );
}

// ===================== CRYPTO DCA =====================
function CryptoDCA({t}) {
  const [coin,setCoin]=useState("BTC-USD");const[monthly,setMonthly]=useState("200");const[years,setYears]=useState("5");const[startPrice,setStartPrice]=useState("30000");const[endPrice,setEndPrice]=useState("100000");
  const num=v=>parseFloat(v)||0;
  const months=num(years)*12;const totalInvested=num(monthly)*months;
  // Simulate linear price appreciation with DCA
  const sp=num(startPrice),ep=num(endPrice);
  let coins=0;
  for(let m=0;m<months;m++){const price=sp+(ep-sp)*(m/months);if(price>0)coins+=num(monthly)/price}
  const portfolioVal=coins*ep;const gain=portfolioVal-totalInvested;const roi=totalInvested>0?((portfolioVal/totalInvested-1)*100):0;
  const avgCost=coins>0?totalInvested/coins:0;
  const is={width:"100%",padding:"7px 10px",fontSize:"13px",fontFamily:"inherit",border:"1px solid "+t.inputBorder,borderRadius:"5px",background:t.inputBg,color:t.text,outline:"none"};
  const fmt=n=>n>=1e6?"$"+(n/1e6).toFixed(2)+"M":"$"+Math.round(n).toLocaleString();
  return (
    <div style={{maxWidth:"650px",margin:"0 auto"}}>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"18px 20px",marginBottom:"14px"}}>
        <h2 style={{fontSize:"16px",fontWeight:"700",margin:"0 0 6px"}}>Crypto DCA Simulator</h2>
        <p style={{fontSize:"12px",color:t.textSecondary,lineHeight:"1.6",margin:0}}>Simulate dollar-cost averaging into crypto. Set a start and target price to see how DCA smooths out your entry and what your returns would look like.</p>
      </div>
      <div style={{background:t.surface,borderRadius:"9px",border:"1px solid "+t.border,padding:"20px",marginBottom:"14px"}}>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"12px",marginBottom:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Asset</label><select value={coin} onChange={e=>setCoin(e.target.value)} style={{...is,cursor:"pointer"}}><option value="BTC-USD">Bitcoin (BTC)</option><option value="ETH-USD">Ethereum (ETH)</option><option value="SOL-USD">Solana (SOL)</option><option value="CUSTOM">Custom</option></select></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Monthly DCA Amount</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={monthly} onChange={e=>setMonthly(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"12px"}}>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Start Price</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={startPrice} onChange={e=>setStartPrice(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Target End Price</label><div style={{position:"relative"}}><span style={{position:"absolute",left:"8px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"12px"}}>$</span><input type="number" value={endPrice} onChange={e=>setEndPrice(e.target.value)} style={{...is,paddingLeft:"22px"}} /></div></div>
          <div><label style={{fontSize:"10px",color:t.textMuted,display:"block",marginBottom:"3px"}}>Time Period</label><select value={years} onChange={e=>setYears(e.target.value)} style={{...is,cursor:"pointer"}}>{[1,2,3,4,5,7,10].map(y=><option key={y} value={y}>{y+" years"}</option>)}</select></div>
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"8px",marginBottom:"14px"}}>
        {[["Portfolio Value",fmt(portfolioVal),t.accent],["Total Invested",fmt(totalInvested),t.blue],["Gain/Loss",fmt(gain),gain>=0?t.green:t.red],["ROI",roi.toFixed(1)+"%",roi>=0?t.green:t.red]].map(function(x){return(
          <div key={x[0]} style={{background:t.surface,border:"1px solid "+t.border,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
            <div style={{fontSize:"9px",color:t.textMuted,textTransform:"uppercase",marginBottom:"3px"}}>{x[0]}</div>
            <div style={{fontSize:"16px",fontWeight:"700",color:x[2]}}>{x[1]}</div>
          </div>
        )})}
      </div>
      <div style={{background:t.surface,borderRadius:"8px",border:"1px solid "+t.border,padding:"14px 16px",marginBottom:"14px"}}>
        <div style={{display:"flex",justifyContent:"space-between",marginBottom:"4px"}}><span style={{fontSize:"12px",color:t.textSecondary}}>Coins accumulated</span><span style={{fontSize:"12px",fontWeight:"600"}}>{coins.toFixed(6)}</span></div>
        <div style={{display:"flex",justifyContent:"space-between"}}><span style={{fontSize:"12px",color:t.textSecondary}}>Average cost per coin</span><span style={{fontSize:"12px",fontWeight:"600"}}>{fmt(avgCost)}</span></div>
      </div>
      <div style={{padding:"10px 12px",background:t.tipBg,border:"1px solid "+t.tipBorder,borderRadius:"6px"}}>
        <div style={{fontSize:"10px",fontWeight:"600",color:t.tipText,marginBottom:"2px"}}>Quick Tip</div>
        <p style={{fontSize:"11px",color:t.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>DCA removes the stress of timing the market. Your average cost will always be lower than the average price. Just pick an amount, automate it, and stop checking the price daily.</p>
      </div>
    </div>
  );
}

const POPULAR_TICKERS = [
  {symbol:"AAPL",name:"Apple"},{symbol:"MSFT",name:"Microsoft"},{symbol:"NVDA",name:"NVIDIA"},
  {symbol:"GOOG",name:"Google"},{symbol:"AMZN",name:"Amazon"},{symbol:"TSLA",name:"Tesla"},
  {symbol:"META",name:"Meta"},{symbol:"SPY",name:"S&P 500"},{symbol:"QQQ",name:"Nasdaq 100"},
  {symbol:"BTC-USD",name:"Bitcoin"},{symbol:"ETH-USD",name:"Ethereum"},{symbol:"SOL-USD",name:"Solana"},
];

// ===================== HISTORICAL MARKET DATA (120 trading days) =====================
const HISTORICAL_DATA = {
"AAPL":{name:"Apple",closes:[214.07,201.77,201.61,203.05,202.42,202.3,204.92,203.62,203.74,201.31,203.63,205.59,207.77,210.17,208.55,204.97,210.31,219.19,219.54,220,218.26,217.81,214.88,219.3,221.38,219.44,225.04,224.55,232.11,230.81,224.83,224.99,222.67,222.63,225,226.86,233,230.63,224.98,228.11,227.8,227.6,230.31,226.41,225.11,224.84,226.41,224.02,222.03,219.26,214.61,212.68,205.36,209.29,207.32,211.03,205.33,201.32,198.01,200.32,192.09,190.36,185.75,187.95,191.44,189.97,186.47,183.37,182.35,182.52,180.09,181.44,182.15,184.29,184.2,181.43,179.31,176.13,173,170.7,170.02,173.49,169.89,173.13,174.25,174.47,175.5,176.06,175.83,174.71,175.64,178,178.44,182.17,183.58,185.42,185.45,182.96,181.19,180.52,178.34,177.42,180.32,181.54,179.33,176.37,178.26,176.39,179.33,178.19,179.89,184.5,184.28,183.58,179.46,175.79,173.11,174,172.99,172.35]},
"MSFT":{name:"Microsoft",closes:[386.85,380.35,366.36,369.99,375.81,374.51,379.42,393.81,387.56,380.7,376.63,380.25,381.64,380.53,369.8,370.85,367.55,367.83,365.38,376.23,380.82,383.33,373.16,369.69,362.08,361.46,353.92,351.6,353.52,353.22,348.59,342.62,336.97,329.41,334.1,330.19,336.06,346.6,344.02,341.35,345.22,349.92,342.91,341.27,342.65,339.19,342.18,339.86,340.57,340.46,339.65,336.99,330.38,326.62,323.54,317.13,314.47,315.14,313.12,310.89,303.08,306.25,304.49,309.49,308.08,307.83,302.14,307.45,313.42,312.3,310.53,305.76,306.61,304.93,308.39,306.76,309.11,307.81,307.21,308.03,309.74,315.48,311.84,312.89,313.54,308.47,311.26,307.56,305.77,302.82,302.76,297.19,305.07,309.24,308.05,321.49,320.74,324.59,318.98,321.9,322.1,319.88,327.88,322.88,326.24,328.24,329.23,328.01,335.41,335.67,337.14,339.43,337.33,344.66,353.63,364.7,365.54,369.23,362.75,368.94]},
"NVDA":{name:"NVIDIA",closes:[129.15,131.94,133.71,138.22,134.18,133.17,127.58,125.4,125.21,121.53,119.46,118.51,116.12,115.04,116.51,120.3,119.06,122.83,126.26,130.35,130.45,129.93,129.87,131.09,130.95,134.2,135.55,136.09,137.16,134.05,133.06,133.36,132.2,130,125.39,125.3,125.43,127.18,122.36,121.52,122.55,124.69,126.03,125.01,125.9,129.53,131.16,130.13,134.35,141.27,139.53,137.51,139.68,145.42,146.57,143.5,143.02,136.92,134.45,130.09,132.85,134.85,132.02,131.93,132.81,134.07,133.41,133.14,130.98,133.34,134.62,135.15,134.16,140.38,137.5,137.4,139.29,141.35,138.74,146.25,142.82,140.19,141.05,142.08,144.16,144.35,146.96,145.99,141.79,139.23,142.47,144.77,148.57,147.1,146.57,147.57,141,143.08,141.95,141.23,148.88,159.13,159.14,161.13,170.13,176.27,175.75,178.02,178.84,179.09,176.78,183.36,193.19,197.45,200.82,196.99,202.96,200.98,209.66,203.38]},
"GOOG":{name:"Google",closes:[162.64,158.66,161.21,158.37,154.84,152.37,151.84,147.17,149.64,147.43,147.73,147.25,149.69,152.57,151.89,149.57,147.41,148.58,146.94,145.44,147.75,149.72,151.71,148.87,145.45,146.96,144.41,145.64,148.87,152.08,148.76,150.17,148.2,149.29,148.87,148.53,150.73,152.72,150.49,149.76,148.51,149.92,151.59,149.07,150.81,148.1,146.51,149.34,144.13,142.83,145.72,149.86,151.34,152.25,153.61,154.44,152.66,149.61,151.02,150.58,149.41,148.4,149.53,153.59,154.38,161.01,162.95,166.44,163.74,164.68,161.05,167.7,167.33,168.37,170.83,172.62,170.77,171.79,164.26,160.77,160.9,162.82,160.34,155.8,157.48,157.55,159.3,162.68,160.68,159.95,162,162.91,157.65,159.11,162.7,167.3,171.88,172.19,170.39,168.32,166.04,168.82,173.59,170.91,171.46,169.88,171.96,169.53,171.66,168.35,169.13,168.91,167.66,172.36,172.99,173,171.42,174.19,174.39,171.33]},
"AMZN":{name:"Amazon",closes:[190.05,187.69,193.98,197.03,195.77,192.6,193.82,191.4,193.03,194.36,197.63,198,199.35,197.52,200.7,197.66,196.24,192.68,189.98,190.71,193.68,198.29,190.81,195.5,195.97,199.65,195.79,196.21,197.81,200.32,201.94,198.16,204.13,194.05,198.05,193.64,195.9,196.62,190.53,190.17,187.25,186.52,189.39,194.15,197.9,197.95,196.57,191.02,190.88,199.75,195.95,205.49,209.35,205.97,207.16,204.77,207.93,208.92,216.86,218.15,218.36,222.6,225.49,226.33,223.24,222.06,223.1,223.96,223.47,221.04,226.3,228.16,230,226.22,221.96,221.15,223.38,228.86,233.88,232.53,239.86,237.51,237.71,243.58,245.84,243.73,246.57,249.01,252.54,260.59,269.18,265.53,266.02,266.81,269.21,264.3,269.37,280.55,277.44,276.77,280.89,278.41,272.52,274.53,281.41,276.63,274.78,274.71,273.05,270.66,269.64,266.02,264.71,265.26,264.05,260.8,260.76,255.52,255.41,259.04]},
"TSLA":{name:"Tesla",closes:[322.9,320.56,329.82,342.69,341.59,337.24,342.48,333.55,337.18,336.65,346.53,338.92,349.2,354.65,382.24,384.86,369.73,379.03,386.89,383.23,389.22,375.44,376.45,389.51,394.36,392.03,389.54,395.98,397.29,400.17,401.58,403.6,385.14,375.69,375.77,354.71,364.56,366.22,357.1,371.61,354.32,353.92,355.24,355.52,372.36,375.68,365.96,372.72,352.44,363.42,362.05,346.38,358,343.79,340.7,328.43,335.81,335.75,328.88,339.36,326.47,326.44,319.52,312.02,316.83,307.08,292.25,280.94,272.24,279.05,289.12,302,280.11,276.55,281.76,281.59,286.49,282.14,284.42,285.47,282.3,265.31,272.7,275.08,273.12,268.86,265.38,256.72,252.94,250.85,246.96,244.18,242.76,248.49,242.48,240.11,234.36,242.67,245.96,233.91,234.65,239.98,235.56,238.86,241.75,238.62,241.19,245.63,254.84,249.02,260.01,259.53,255.91,268.65,267.01,268.16,257.58,268.42,267.19,260.9]},
"META":{name:"Meta",closes:[546.98,558.14,554.56,541.42,551.33,544.67,536.22,533.54,517.39,513.28,510.98,513.39,526.9,511.96,503.53,513.93,510.23,510.42,520.62,515.82,506.9,491.16,479.9,479.58,479.89,497.19,508.82,510.53,527.98,529.27,547.12,539.8,545.42,551.38,553.56,568.9,562.85,567.81,569.28,563.46,566.77,553.22,548.36,544.52,528.64,522.44,530.12,530.65,539.9,548.27,558.9,554.23,554.23,548.48,552.3,557.2,560.19,543.61,548.17,553.1,558.75,558.85,554.95,558.67,594.13,589.94,589.32,606.56,607.82,622.09,627.06,644.41,646.57,638.52,639.56,646.7,657.47,667.27,658.76,659.14,676.37,682.53,700.97,694.93,705.97,713.24,729.12,728.41,730.44,755.73,764.22,776.36,782.29,792.79,798.33,815.71,810.66,811.06,804.71,819.5,853.26,828.46,828.93,804.34,794.34,799.81,809.99,815.65,820.57,813.56,809.93,800.98,807.44,824.07,801.93,775.22,765.36,755.64,754.86,756.12]},
"SPY":{name:"S&P 500",closes:[561.22,560,560.59,562.88,571.28,572.49,579.82,583.12,581.39,585.8,589.03,585.61,582.04,582.17,583.16,591.97,599.78,595.55,594.91,594.19,603.19,602.95,603.85,598.43,600.1,594.84,596.09,591.86,589.48,595.08,596.14,599.11,603.46,601.56,599.18,597.96,601.33,606.07,598.89,604.55,602.64,601.49,600.79,605.75,605.02,599.69,603.4,600.8,600.76,595.15,596.34,593.27,583.6,585.91,581.33,577.46,574.61,578.56,585.19,578.55,582.48,586.19,584.39,573.87,572.14,577.38,571.68,571.7,572.32,568.23,570.18,568.69,580.65,585.09,586.19,580.58,579.98,583.64,583.4,587.06,592.49,592.79,586.1,582.05,586.36,585.77,590.42,588.05,585.2,595.73,596.03,594.92,593.12,591.95,594.98,597.46,594.69,595.51,598.11,593.59,588.2,586.59,588.96,590.46,580.67,574.41,571.5,564.77,558.6,552.05,551.06,540.12,545.13,538.4,534.54,537.47,536.6,538.27,541.17,551.35]},
"QQQ":{name:"Nasdaq 100",closes:[488.32,486.82,488.19,488.32,498.24,506.96,507.18,507.95,504.86,510.2,516.08,517.02,512.11,510.11,508.81,508.17,512.17,509.53,512.19,509.11,522.44,522.66,524.79,529.03,525.04,516.68,512.81,508.27,505.96,502.29,504.75,506.99,502.69,500.01,494.63,490.75,500.18,504.51,506.75,504.34,514.21,515.5,517.9,520.05,512.32,510.8,513.29,503.05,500.08,499.99,496.59,495.97,494.37,490.94,485.8,485.9,493.57,493.42,494.12,490.72,493.63,489.27,490.77,486.04,482,486.17,484.22,476.27,465.51,462.62,466.33,469.23,472.08,462.9,465.35,466.3,458.91,468.3,473.18,470.42,461.02,470.59,471.22,471.98,467.74,471.22,474.65,472.39,473,477.6,475.38,474.47,473.86,477.38,477.24,478.16,475.96,472.55,468.16,469.33,469.86,470.41,466.7,468.99,451.87,453.4,455.97,458.95,464.45,463.18,464.32,466.18,461,460.12,459.83,466.36,458.79,460.91,463.1,460.59]},
"BTC-USD":{name:"Bitcoin",closes:[89608.63,89294.1,86612.57,87205.8,87860.45,90897.35,91700.8,91750.13,92454.82,91066.85,93386.92,95852.33,92597.31,92066.07,94221.61,96082.42,97451.89,99151.75,100776.99,97736.01,96724.81,97058.14,97893.35,101329.23,103616.46,100833.23,97562.89,99029.29,101970.58,101462.11,99205.93,99946.64,97468.75,100750.53,96163.3,94500.22,96283.45,94408.94,89910.83,89812.61,89994.91,91212,92183.33,92214.58,94710.32,94611.5,96290.47,94169.47,95460.43,95950.2,94521.13,94873.49,91830.13,88326.8,88414.02,86696.56,87528.91,86981.75,87659.84,91593,94495.34,94608.48,96634.39,94770.95,95041.33,94177.59,92382.95,93807.77,90882.83,89878.26,89844.14,89312.5,88480.7,87365.11,87165.7,90195.64,89526.93,88225.76,87509.4,91698.64,92007.92,88385.54,87967.87,88484.88,86966.88,86808.19,88187.45,89241.09,92402.53,97413.07,99664.54,98722.41,96815.43,97341.97,96515.47,97137.39,98639.99,97578.96,95986.05,97031.95,93907.16,93852.29,95703.57,96648.52,96158.8,100105.53,102430.89,106201.14,104772.47,104332.15,106072.69,107157.72,108208.4,106574.05,106933.63,109781.28,106581.38,105999.07,108570.48,106949.97]},
"ETH-USD":{name:"Ethereum",closes:[3136.53,3003.33,2990.29,3018.96,2990.27,2953.72,3068.16,3100.61,2992.73,2808.78,2878.36,2976.09,3072.23,3218.17,3199.58,3208.02,3128.3,3075.68,2892.4,2876.8,2926.01,2795.11,2913.86,2892.48,2911.49,2845.6,2782.55,2743.27,2766.01,2838.04,2716.74,2584.07,2606.32,2642.44,2576.24,2693.22,2676.95,2704.02,2697.6,2684.46,2728.94,2589.57,2550.08,2585.73,2497.29,2541.69,2500.69,2423.63,2297.93,2265.93,2255.99,2156.02,2086.52,2007.4,1924.33,1880.17,1826.59,1839.59,1846.55,1818.06,1895,1879.78,1884.91,1865.22,1918.06,1921.61,1868.31,1846.91,1887.62,1906.8,1834.25,1891.27,1871.22,1821.45,1873.59,1930.59,1934.26,1899.14,1842.78,1786.47,1756.46,1754.79,1717.7,1705.74,1662.79,1704.87,1684.24,1606.61,1610.53,1711.57,1754.65,1703.6,1737.82,1681.35,1668.78,1657.9,1628.03,1622.26,1569.48,1555.07,1579.94,1585.76,1542.27,1569.1,1561.03,1533.08,1536.21,1537.91,1570.01,1591.2,1645.12,1639.52,1642.95,1615.17,1671.59,1667.68,1708.19,1680.07,1686.37,1728.82]},
"SOL-USD":{name:"Solana",closes:[175.83,184.95,192.41,197.34,201,202.45,202.55,197.23,197.71,192.21,193.69,188.23,202.01,220.93,232.21,234.26,222,221.49,221.26,218.83,220.7,222.59,226.78,226.17,224.3,205.92,212.97,214.29,231.49,235.47,244.47,244.77,250.54,257.91,267.2,273.02,288,282.87,279.97,280.34,273.78,281.21,271.66,262.19,268.61,266.86,273.59,267.43,259.39,258.09,270.12,256.95,270.5,259.11,258.58,269.9,256.76,268.86,289.51,307.22,302.58,306.16,307.14,322.04,312.4,332.31,344.15,352.46,350.61,361.28,361.16,350.54,352.08,359.45,375.23,372.09,364.45,374.17,379.06,384.99,382.49,374.6,370.55,354.81,349.31,332.84,326.65,329.62,343.4,356.5,365.35,362.08,367.81,356.14,349.35,376.71,378.81,377.23,384.68,373.86,366.62,345.49,333.96,329.81,311.16,305.57,308.96,314.03,322.06,316.25,309.03,317.56,332.63,324.69,316.91,324.54,305.66,297.89,306.05,299.57]},
};

// ===================== TECHNICAL ANALYSIS =====================
function calcEMA(d,p){const k=2/(p+1);const e=[d[0]];for(let i=1;i<d.length;i++)e.push(d[i]*k+e[i-1]*(1-k));return e}
function calcSMA(d,p){const s=[];for(let i=0;i<d.length;i++){if(i<p-1){s.push(null);continue}let sum=0;for(let j=0;j<p;j++)sum+=d[i-j];s.push(sum/p)}return s}
function calcMACD(c){const e12=calcEMA(c,12),e26=calcEMA(c,26),ml=e12.map((v,i)=>v-e26[i]),sl=calcEMA(ml,9),h=ml.map((v,i)=>v-sl[i]);return{macdLine:ml,signalLine:sl,histogram:h}}
function calcRSI(c,p=14){const r=[null];let ag=0,al=0;for(let i=1;i<=p;i++){const d=c[i]-c[i-1];if(d>0)ag+=d;else al-=d}ag/=p;al/=p;for(let i=1;i<p;i++)r.push(null);r.push(al===0?100:100-100/(1+ag/al));for(let i=p+1;i<c.length;i++){const d=c[i]-c[i-1];ag=(ag*(p-1)+(d>0?d:0))/p;al=(al*(p-1)+(d<0?-d:0))/p;r.push(al===0?100:100-100/(1+ag/al))}return r}
function calcBollinger(c,p=20,m=2){const ema=calcEMA(c,p),u=[],l=[];for(let i=0;i<c.length;i++){const lookback=Math.min(i+1,p);let v=0;for(let j=0;j<lookback;j++)v+=Math.pow(c[i-j]-ema[i],2);const sd=Math.sqrt(v/lookback);u.push(ema[i]+m*sd);l.push(ema[i]-m*sd)}return{sma:ema,upper:u,lower:l}}

function generateForecast(closes,strategy,days=30){
  const last=closes[closes.length-1],returns=[];
  for(let i=1;i<closes.length;i++)returns.push((closes[i]-closes[i-1])/closes[i-1]);
  const avgR=returns.reduce((a,b)=>a+b,0)/returns.length;
  const vol=Math.sqrt(returns.reduce((a,b)=>a+Math.pow(b-avgR,2),0)/returns.length);
  let bias=0,confidence="Medium",signal="Neutral",reasoning="";
  if(strategy==="macd"){const{macdLine:ml,signalLine:sl,histogram:h}=calcMACD(closes);if(ml[ml.length-1]>sl[sl.length-1]){bias=0.002;signal="Bullish";reasoning="MACD above signal line"}else{bias=-0.002;signal="Bearish";reasoning="MACD below signal line"}if(Math.abs(h[h.length-1])>Math.abs(h[h.length-2])){bias*=1.5;confidence="High";reasoning+=", momentum increasing"}else{confidence="Low";reasoning+=", momentum fading"}}
  else if(strategy==="rsi"){const rsi=calcRSI(closes);const last=rsi[rsi.length-1];if(last>70){bias=-0.003;signal="Bearish";confidence="High";reasoning=`RSI at ${last.toFixed(1)} — overbought`}else if(last<30){bias=0.003;signal="Bullish";confidence="High";reasoning=`RSI at ${last.toFixed(1)} — oversold`}else{bias=last>50?0.001:-0.001;signal=last>50?"Bullish":"Bearish";confidence="Medium";reasoning=`RSI at ${last.toFixed(1)} — ${last>50?"above":"below"} midline`}}
  else if(strategy==="bollinger"){const{sma,upper,lower}=calcBollinger(closes);const lc=closes[closes.length-1],lu=upper[upper.length-1],ll=lower[lower.length-1],ls=sma[sma.length-1];const bw=(lu-ll)/ls;if(lc>lu){bias=-0.002;signal="Bearish";reasoning="Price above upper band"}else if(lc<ll){bias=0.002;signal="Bullish";reasoning="Price below lower band"}else if(bw<0.05){signal="Neutral";confidence="High";reasoning="Squeeze detected — big move coming"}else{bias=lc>ls?0.001:-0.001;signal=lc>ls?"Bullish":"Bearish";reasoning=`Price ${lc>ls?"above":"below"} middle band`}}
  else if(strategy==="sma"){const s20=calcSMA(closes,20),s50=calcSMA(closes,50);const lp=closes[closes.length-1],l20=s20[s20.length-1],l50=s50[s50.length-1];if(l20&&l50){if(lp>l20&&l20>l50){bias=0.002;signal="Bullish";confidence="High";reasoning="Price > SMA20 > SMA50"}else if(lp<l20&&l20<l50){bias=-0.002;signal="Bearish";confidence="High";reasoning="Price < SMA20 < SMA50"}else{bias=lp>l50?0.001:-0.001;signal=lp>l50?"Bullish":"Bearish";confidence="Low";reasoning="Mixed — MAs not aligned"}}}
  else if(strategy==="volume"){const rc=closes.slice(-10);const up=rc[rc.length-1]>rc[0];bias=up?0.001:-0.001;signal=up?"Bullish":"Bearish";reasoning=`Recent trend ${up?"up":"down"}`}
  else if(strategy==="fibonacci"){const hi=Math.max(...closes.slice(-60)),lo=Math.min(...closes.slice(-60)),lp=closes[closes.length-1];const ret=(hi-lp)/(hi-lo);if(ret>0.618){bias=0.002;signal="Bullish";confidence="High";reasoning=`Near 61.8% retracement (${(ret*100).toFixed(1)}%)`}else if(ret>0.382){bias=0.001;signal="Bullish";confidence="Medium";reasoning=`In 38-62% zone (${(ret*100).toFixed(1)}%)`}else{bias=0.001;signal="Bullish";confidence="Low";reasoning=`Shallow retracement (${(ret*100).toFixed(1)}%)`}}
  else if(strategy==="vwap"){const lp=closes[closes.length-1];const avg=closes.slice(-20).reduce((a,b)=>a+b,0)/20;if(lp>avg*1.02){bias=-0.001;signal="Bearish";confidence="Medium";reasoning=`Price ${((lp/avg-1)*100).toFixed(1)}% above VWAP — may revert`}else if(lp<avg*0.98){bias=0.001;signal="Bullish";confidence="Medium";reasoning=`Price ${((1-lp/avg)*100).toFixed(1)}% below VWAP — may revert`}else{signal="Neutral";confidence="Low";reasoning="Price near VWAP — no clear edge"}}
  else if(strategy==="stochastic"){const p=14,sl=closes.slice(-p);const hi=Math.max(...sl),lo=Math.min(...sl);const k=lo===hi?50:((closes[closes.length-1]-lo)/(hi-lo))*100;if(k>80){bias=-0.002;signal="Bearish";confidence="High";reasoning=`Stochastic %K at ${k.toFixed(1)} — overbought`}else if(k<20){bias=0.002;signal="Bullish";confidence="High";reasoning=`Stochastic %K at ${k.toFixed(1)} — oversold`}else{bias=k>50?0.001:-0.001;signal=k>50?"Bullish":"Bearish";confidence="Medium";reasoning=`Stochastic %K at ${k.toFixed(1)} — mid range`}}
  else if(strategy==="atr"){const atr=[];for(let i=1;i<closes.length;i++)atr.push(Math.abs(closes[i]-closes[i-1]));const recent=atr.slice(-14).reduce((a,b)=>a+b,0)/14;const prev=atr.slice(-28,-14).reduce((a,b)=>a+b,0)/14;const pct=(recent/closes[closes.length-1]*100).toFixed(2);if(recent>prev*1.3){signal="Neutral";confidence="High";reasoning=`ATR expanding (${pct}% of price) — volatility increasing, big move underway`}else if(recent<prev*0.7){signal="Neutral";confidence="High";reasoning=`ATR contracting (${pct}% of price) — squeeze building, breakout imminent`}else{const up=closes[closes.length-1]>closes[closes.length-10];bias=up?0.001:-0.001;signal=up?"Bullish":"Bearish";confidence="Medium";reasoning=`ATR stable (${pct}% of price), trending ${up?"up":"down"}`}}
  else if(strategy==="ichimoku"){const s9=calcEMA(closes,9),s26=calcEMA(closes,26);const lp=closes[closes.length-1],t9=s9[s9.length-1],t26=s26[s26.length-1];if(t9&&t26){const cloudTop=Math.max(t9,t26),cloudBot=Math.min(t9,t26);if(lp>cloudTop){bias=0.002;signal="Bullish";confidence="High";reasoning="Price above Ichimoku cloud"}else if(lp<cloudBot){bias=-0.002;signal="Bearish";confidence="High";reasoning="Price below Ichimoku cloud"}else{signal="Neutral";confidence="Low";reasoning="Price inside cloud — consolidation"}}}
  else if(strategy==="support_resistance"){const hi60=Math.max(...closes.slice(-60)),lo60=Math.min(...closes.slice(-60)),lp=closes[closes.length-1];const range=hi60-lo60;const pctFromHi=(hi60-lp)/range,pctFromLo=(lp-lo60)/range;if(pctFromLo<0.1){bias=0.002;signal="Bullish";confidence="High";reasoning=`Near support at $${lo60.toFixed(2)} — ${(pctFromLo*100).toFixed(1)}% from low`}else if(pctFromHi<0.1){bias=-0.002;signal="Bearish";confidence="High";reasoning=`Near resistance at $${hi60.toFixed(2)} — ${(pctFromHi*100).toFixed(1)}% from high`}else{bias=lp>((hi60+lo60)/2)?0.001:-0.001;signal=lp>((hi60+lo60)/2)?"Bullish":"Bearish";confidence="Medium";reasoning=`Mid-range between $${lo60.toFixed(2)} support and $${hi60.toFixed(2)} resistance`}}
  else if(strategy==="candlestick"){const c=closes,n=c.length;const d1=c[n-1]-c[n-2],d2=c[n-2]-c[n-3],d3=c[n-3]-c[n-4];if(d1>0&&d2>0&&d3>0){bias=0.002;signal="Bullish";confidence="High";reasoning="Three consecutive up closes — strong bullish momentum"}else if(d1<0&&d2<0&&d3<0){bias=-0.002;signal="Bearish";confidence="High";reasoning="Three consecutive down closes — strong bearish pressure"}else if(Math.abs(d1)<Math.abs(d2)*0.3){signal="Neutral";confidence="Medium";reasoning="Small body after large move — indecision (doji-like)"}else{bias=d1>0?0.001:-0.001;signal=d1>0?"Bullish":"Bearish";confidence="Low";reasoning=`Last close ${d1>0?"up":"down"} $${Math.abs(d1).toFixed(2)} — no clear pattern`}}
  else if(strategy==="dca"){const m3=closes.slice(-60),m1=closes.slice(-20);const avg3=m3.reduce((a,b)=>a+b,0)/m3.length,avg1=m1.reduce((a,b)=>a+b,0)/m1.length;const lp=closes[closes.length-1];if(lp<avg3*0.95){bias=0.001;signal="Bullish";confidence="High";reasoning=`Price ${((1-lp/avg3)*100).toFixed(1)}% below 3-month average — DCA buys more here`}else if(lp>avg3*1.05){bias=-0.001;signal="Neutral";confidence="Medium";reasoning=`Price ${((lp/avg3-1)*100).toFixed(1)}% above 3-month average — DCA buys less here`}else{signal="Neutral";confidence="High";reasoning=`Price near 3-month average — DCA working as designed, consistent accumulation`}}
  const scenarios={bull:[],base:[],bear:[]};const seed=closes.reduce((a,b)=>a+b,0);
  for(const[key,mult]of[["bull",1.5],["base",0],["bear",-1.5]]){let price=last;scenarios[key].push(price);for(let d=1;d<=days;d++){const db=bias+mult*vol*0.3;const pr=Math.sin(seed*d*(key==="bull"?1.1:key==="bear"?0.9:1))*0.5+0.5;price=price*(1+db+(pr-0.5)*vol*0.8);scenarios[key].push(price)}}
  return{scenarios,signal,confidence,reasoning,volatility:vol};
}

// ===================== STOCK CHART =====================
function StockChart({closes,strategy,t}){
  const canvasRef=useRef(null);const[showForecast,setShowForecast]=useState(true);const[forecast,setForecast]=useState(null);
  useEffect(()=>{if(closes.length>0&&strategy)setForecast(generateForecast(closes,strategy))},[closes,strategy]);
  useEffect(()=>{
    const canvas=canvasRef.current;if(!canvas||closes.length===0)return;
    const ctx=canvas.getContext("2d");const dpr=window.devicePixelRatio||1;const rect=canvas.getBoundingClientRect();
    canvas.width=rect.width*dpr;canvas.height=rect.height*dpr;ctx.scale(dpr,dpr);const W=rect.width,H=rect.height;ctx.clearRect(0,0,W,H);
    const pT=20,pB=30,pL=60,pR=showForecast&&forecast?95:20;const cW=W-pL-pR,cH=H-pT-pB;
    const fd=showForecast&&forecast?30:0;const allP=[...closes];if(forecast&&showForecast)allP.push(...forecast.scenarios.bull,...forecast.scenarios.bear);
    const minP=Math.min(...allP)*0.98,maxP=Math.max(...allP)*1.02;const tot=closes.length+fd;
    const toX=i=>pL+(i/(tot-1))*cW;const toY=p=>pT+cH-((p-minP)/(maxP-minP))*cH;
    // Helper to draw a line from array
    const drawLine=(data,color,width,dash)=>{ctx.beginPath();ctx.strokeStyle=color;ctx.lineWidth=width;if(dash)ctx.setLineDash(dash);let started=false;for(let i=0;i<data.length;i++){if(data[i]===null||data[i]===undefined)continue;const x=toX(i),y=toY(data[i]);if(!started){ctx.moveTo(x,y);started=true}else ctx.lineTo(x,y)}ctx.stroke();if(dash)ctx.setLineDash([])};
    // Grid
    ctx.strokeStyle=t.border;ctx.lineWidth=1;
    for(let i=0;i<=4;i++){const y=pT+(cH/4)*i;ctx.beginPath();ctx.moveTo(pL,y);ctx.lineTo(W-pR,y);ctx.stroke();ctx.fillStyle=t.textMuted;ctx.font="10px Inter,sans-serif";ctx.textAlign="right";const val=maxP-(maxP-minP)*(i/4);ctx.fillText("$"+(val>1000?val.toFixed(0):val.toFixed(2)),pL-6,y+3)}

    // === STRATEGY OVERLAYS (drawn FIRST, under price) ===

    if(strategy==="bollinger"){
      const{sma,upper,lower}=calcBollinger(closes);
      // Band fill
      ctx.beginPath();let st=false;for(let i=0;i<closes.length;i++){if(upper[i]===null)continue;if(!st){ctx.moveTo(toX(i),toY(upper[i]));st=true}else ctx.lineTo(toX(i),toY(upper[i]))}for(let i=closes.length-1;i>=0;i--){if(lower[i]!==null)ctx.lineTo(toX(i),toY(lower[i]))}ctx.closePath();ctx.fillStyle=t.purple+"18";ctx.fill();
      drawLine(upper,t.purple+"70",1.2);drawLine(lower,t.purple+"70",1.2);drawLine(sma,t.purple,1.5,[4,3]);
    }
    if(strategy==="sma"){
      drawLine(calcEMA(closes,20),t.orange,2);drawLine(calcEMA(closes,50),t.red+"CC",2);
    }
    if(strategy==="vwap"){
      drawLine(calcEMA(closes,20),t.orange,2,[5,3]);
      drawLine(calcEMA(closes,50),t.purple+"80",1.5,[3,3]);
    }
    if(strategy==="dca"){
      // DCA cost basis — average buy price if buying $100/week
      const freq=5;const costBasis=[];let totalShares=0,totalCost=0;
      for(let i=0;i<closes.length;i++){
        if(i%freq===0){totalShares+=100/closes[i];totalCost+=100;}
        costBasis.push(totalShares>0?totalCost/totalShares:null);
      }
      drawLine(costBasis,t.green,2,[5,3]);
      // Horizontal avg cost reference
      const finalAvg=costBasis[costBasis.length-1];
      if(finalAvg){
        ctx.strokeStyle=t.green+"40";ctx.setLineDash([3,5]);ctx.lineWidth=1;ctx.beginPath();ctx.moveTo(pL,toY(finalAvg));ctx.lineTo(pL+cW,toY(finalAvg));ctx.stroke();ctx.setLineDash([]);
        ctx.fillStyle=t.green+"90";ctx.font="bold 9px Inter,sans-serif";ctx.textAlign="left";
        ctx.fillText("Avg Cost $"+finalAvg.toFixed(2),pL+4,toY(finalAvg)-5);
      }
      // Buy markers (dots on purchase days)
      for(let i=0;i<closes.length;i++){if(i%freq===0){ctx.fillStyle=t.green+"70";ctx.beginPath();ctx.arc(toX(i),toY(closes[i]),2.5,0,Math.PI*2);ctx.fill()}}
    }
    if(strategy==="ichimoku"){
      const s9=calcEMA(closes,9),s26=calcEMA(closes,26);
      // Draw cloud segments — green where s9>s26, red where s9<s26
      // Find first valid index
      let startIdx=-1;for(let i=0;i<closes.length;i++){if(s9[i]!==null&&s26[i]!==null){startIdx=i;break}}
      if(startIdx>=0){
        // Draw cloud in segments by color
        let segStart=startIdx;
        for(let i=startIdx+1;i<=closes.length;i++){
          const prevAbove=s9[i-1]>=s26[i-1];
          const currAbove=i<closes.length&&s9[i]!==null&&s26[i]!==null?s9[i]>=s26[i]:prevAbove;
          if(i===closes.length||currAbove!==prevAbove){
            // Draw segment from segStart to i-1
            ctx.beginPath();
            for(let j=segStart;j<i;j++){if(s9[j]!==null&&s26[j]!==null)ctx.lineTo(toX(j),toY(Math.max(s9[j],s26[j])))}
            for(let j=i-1;j>=segStart;j--){if(s9[j]!==null&&s26[j]!==null)ctx.lineTo(toX(j),toY(Math.min(s9[j],s26[j])))}
            ctx.closePath();ctx.fillStyle=(prevAbove?t.green:t.red)+"1A";ctx.fill();
            segStart=i-1;
          }
        }
      }
      drawLine(s9,t.blue,1.8);drawLine(s26,t.red+"CC",1.8);
    }
    if(strategy==="support_resistance"){
      const hi60=Math.max(...closes.slice(-60)),lo60=Math.min(...closes.slice(-60)),mid=(hi60+lo60)/2;
      // Resistance zone
      ctx.fillStyle=t.red+"0C";ctx.fillRect(pL,toY(hi60),cW,toY(hi60*0.99)-toY(hi60));
      ctx.fillStyle=t.green+"0C";ctx.fillRect(pL,toY(lo60*1.01),cW,toY(lo60)-toY(lo60*1.01));
      for(const[val,color,label]of[[hi60,t.red,"Resistance"],[lo60,t.green,"Support"],[mid,t.textMuted+"60","Mid"]]){
        ctx.strokeStyle=color;ctx.setLineDash([6,4]);ctx.lineWidth=1.5;ctx.beginPath();ctx.moveTo(pL,toY(val));ctx.lineTo(pL+cW,toY(val));ctx.stroke();ctx.setLineDash([]);
        ctx.fillStyle=color;ctx.font="bold 9px Inter,sans-serif";ctx.textAlign="left";ctx.fillText(label+" $"+val.toFixed(2),pL+4,toY(val)-5);
      }
    }
    if(strategy==="fibonacci"){
      const hi=Math.max(...closes.slice(-60)),lo=Math.min(...closes.slice(-60));
      const fibs=[[0,"100%",t.red],[0.236,"76.4%",t.orange],[0.382,"61.8%",t.orange],[0.5,"50%",t.purple],[0.618,"38.2%",t.blue],[0.786,"23.6%",t.blue],[1,"0%",t.green]];
      for(const[lvl,label,color]of fibs){
        const price=hi-lvl*(hi-lo);
        ctx.strokeStyle=color+"40";ctx.setLineDash([3,3]);ctx.lineWidth=1;ctx.beginPath();ctx.moveTo(pL,toY(price));ctx.lineTo(pL+cW,toY(price));ctx.stroke();ctx.setLineDash([]);
        ctx.fillStyle=color+"90";ctx.font="9px Inter,sans-serif";ctx.textAlign="right";ctx.fillText(`${label} $${price.toFixed(2)}`,pL+cW-2,toY(price)-3);
      }
      // Highlight the golden pocket zone (61.8-78.6%)
      const g1=hi-0.382*(hi-lo),g2=hi-0.236*(hi-lo);
      ctx.fillStyle=t.orange+"0A";ctx.fillRect(pL,toY(g2),cW,toY(g1)-toY(g2));
    }
    if(strategy==="atr"){
      // EMA-based ATR channel — starts from bar 1
      const tr=[];for(let i=1;i<closes.length;i++)tr.push(Math.abs(closes[i]-closes[i-1]));
      const atrEma=calcEMA(tr,14);
      // atrEma has length closes.length-1, offset by 1
      const upper=[null],lower=[null];
      for(let i=0;i<atrEma.length;i++){upper.push(closes[i+1]+atrEma[i]*1.5);lower.push(closes[i+1]-atrEma[i]*1.5)}
      ctx.beginPath();for(let i=1;i<closes.length;i++)ctx.lineTo(toX(i),toY(upper[i]));for(let i=closes.length-1;i>=1;i--)ctx.lineTo(toX(i),toY(lower[i]));ctx.closePath();ctx.fillStyle=t.orange+"10";ctx.fill();
      drawLine(upper,t.orange+"50",1,[3,3]);drawLine(lower,t.orange+"50",1,[3,3]);
    }
    if(strategy==="candlestick"){
      // Draw candlestick bodies for ALL bars
      const candleW=Math.max(2,Math.min(8,(cW/(tot-1))*0.65));
      for(let i=1;i<closes.length;i++){
        const open=closes[i-1],close=closes[i];const bullish=close>=open;
        const top=Math.max(open,close),bot=Math.min(open,close);
        // Wick — approximate high/low from neighboring closes
        const prevClose=i>1?closes[i-2]:open;
        const hi2=Math.max(open,close,close+(Math.random()*0.003*close)),lo2=Math.min(open,close,close-(Math.random()*0.003*close));
        ctx.strokeStyle=bullish?t.green+"90":t.red+"90";ctx.lineWidth=1;
        ctx.beginPath();ctx.moveTo(toX(i),toY(hi2));ctx.lineTo(toX(i),toY(lo2));ctx.stroke();
        // Body
        ctx.fillStyle=bullish?t.green+"50":t.red+"50";ctx.strokeStyle=bullish?t.green:t.red;ctx.lineWidth=1;
        const bodyTop=toY(top),bodyBot=toY(bot),bodyH=Math.max(1.5,bodyBot-bodyTop);
        ctx.fillRect(toX(i)-candleW/2,bodyTop,candleW,bodyH);ctx.strokeRect(toX(i)-candleW/2,bodyTop,candleW,bodyH);
      }
    }
    if(strategy==="volume"){
      // Simulate volume with price change magnitude
      const maxChg=Math.max(...closes.slice(1).map((c,i)=>Math.abs(c-closes[i])));
      const barW=Math.max(1,(cW/(tot-1))*0.5);
      for(let i=1;i<closes.length;i++){
        const chg=closes[i]-closes[i-1];const mag=Math.abs(chg)/maxChg;
        ctx.fillStyle=(chg>=0?t.green:t.red)+"30";
        const barH=mag*cH*0.3;ctx.fillRect(toX(i)-barW/2,pT+cH-barH,barW,barH);
      }
    }

    // === PRICE LINE (drawn AFTER overlays so it's on top) ===
    if(strategy!=="candlestick"){
      // Gradient fill under price
      ctx.beginPath();ctx.moveTo(toX(0),toY(closes[0]));for(let i=1;i<closes.length;i++)ctx.lineTo(toX(i),toY(closes[i]));ctx.lineTo(toX(closes.length-1),pT+cH);ctx.lineTo(toX(0),pT+cH);ctx.closePath();
      const grd=ctx.createLinearGradient(0,pT,0,pT+cH);grd.addColorStop(0,t.accent+"18");grd.addColorStop(1,t.accent+"00");ctx.fillStyle=grd;ctx.fill();
      // Price line
      ctx.beginPath();ctx.strokeStyle=t.accent;ctx.lineWidth=2;for(let i=0;i<closes.length;i++){const x=toX(i),y=toY(closes[i]);i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}ctx.stroke();
    }

    // === FORECAST (drawn last) ===
    if(showForecast&&forecast){
      const divX=toX(closes.length-1);ctx.strokeStyle=t.textMuted+"40";ctx.setLineDash([4,4]);ctx.beginPath();ctx.moveTo(divX,pT);ctx.lineTo(divX,pT+cH);ctx.stroke();ctx.setLineDash([]);
      for(const[key,color]of[["bull",t.green],["base",t.textMuted],["bear",t.red]]){
        const pts=forecast.scenarios[key];ctx.beginPath();ctx.strokeStyle=color+"80";ctx.lineWidth=1.5;ctx.setLineDash([3,3]);
        for(let i=0;i<pts.length;i++){const x=toX(closes.length-1+i),y=toY(pts[i]);i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}ctx.stroke();ctx.setLineDash([]);
        const ev=pts[pts.length-1],ex=toX(closes.length-1+pts.length-1),ey=toY(ev);
        ctx.fillStyle=color+"CC";ctx.font="bold 10px Inter,sans-serif";ctx.textAlign="left";
        const pct=((ev-closes[closes.length-1])/closes[closes.length-1]*100).toFixed(1);
        ctx.fillText(`$${ev.toFixed(ev>100?0:2)} (${pct>0?"+":""}${pct}%)`,ex+4,ey+3);
      }
    }
  },[closes,strategy,forecast,showForecast,t]);

  // Legend config per strategy
  const legends={
    bollinger:[["Upper/Lower",t.purple+"70","solid"],["SMA(20)",t.purple,"dash"]],
    sma:[["EMA(20)",t.orange,"solid"],["EMA(50)",t.red+"CC","solid"]],
    vwap:[["EMA(20) ≈ VWAP",t.orange,"dash"],["EMA(50)",t.purple+"80","dash"]],
    dca:[["DCA Cost Basis",t.green,"dash"],["Buy Points",t.green,"dot"]],
    ichimoku:[["Conversion (9)",t.blue,"solid"],["Base (26)",t.red+"CC","solid"],["Cloud","","fill"]],
    support_resistance:[["Resistance",t.red,"dash"],["Support",t.green,"dash"]],
    fibonacci:[["Fib Levels",t.purple,"dash"]],
    atr:[["ATR Channel (1.5x)",t.orange+"50","dash"]],
    candlestick:[["Green = Bullish",t.green,"solid"],["Red = Bearish",t.red,"solid"]],
    volume:[["Green = Buying",t.green,"solid"],["Red = Selling",t.red,"solid"]],
  };
  const leg=legends[strategy]||[];

  return(<div>
    <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:"8px",flexWrap:"wrap",gap:"6px"}}>
      <div style={{display:"flex",gap:"10px",flexWrap:"wrap"}}>
        {leg.map(([label,color])=><span key={label} style={{fontSize:"10px",color:t.textMuted,display:"flex",alignItems:"center",gap:"3px"}}><span style={{display:"inline-block",width:"12px",height:"2px",background:color,borderRadius:"1px"}}></span>{label}</span>)}
      </div>
      <button onClick={()=>setShowForecast(!showForecast)} style={{background:showForecast?t.accentBg:"transparent",border:`1px solid ${showForecast?t.accentBorder:t.border}`,borderRadius:"5px",padding:"5px 10px",cursor:"pointer",color:showForecast?t.accentText:t.textMuted,fontSize:"11px",fontFamily:"inherit"}}>{showForecast?"Forecast On":"Forecast Off"}</button>
    </div>
    <canvas ref={canvasRef} style={{width:"100%",height:"300px",borderRadius:"8px",background:t.bg,border:`1px solid ${t.border}`}}/>
    {forecast&&<div style={{marginTop:"12px",display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"8px"}}>
      {[["Signal",forecast.signal,forecast.signal==="Bullish"?t.green:forecast.signal==="Bearish"?t.red:t.accent],["Confidence",forecast.confidence,t.text],["Volatility",(forecast.volatility*100).toFixed(1)+"%",t.text]].map(([l,v,c])=>
        <div key={l} style={{background:t.surface,border:`1px solid ${t.border}`,borderRadius:"8px",padding:"10px"}}>
          <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>{l}</div>
          <div style={{fontSize:"15px",fontWeight:"700",color:c}}>{v}</div></div>)}
      <div style={{gridColumn:"1/-1",background:t.surface,border:`1px solid ${t.border}`,borderRadius:"8px",padding:"10px"}}>
        <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>Analysis</div>
        <div style={{fontSize:"12px",color:t.textSecondary}}>{forecast.reasoning}</div></div>
    </div>}
  </div>);
}

// ===================== SUB INDICATOR =====================
function SubIndicator({closes,strategy,t}){
  const canvasRef=useRef(null);
  const hasPanel=["macd","rsi","stochastic","atr"].includes(strategy);
  useEffect(()=>{
    const canvas=canvasRef.current;if(!canvas||closes.length===0||!hasPanel)return;
    const ctx=canvas.getContext("2d");const dpr=window.devicePixelRatio||1;const rect=canvas.getBoundingClientRect();
    canvas.width=rect.width*dpr;canvas.height=rect.height*dpr;ctx.scale(dpr,dpr);const W=rect.width,H=rect.height;ctx.clearRect(0,0,W,H);
    const pT=8,pB=8,pL=60,pR=16,cW=W-pL-pR,cH=H-pT-pB;
    const toX=i=>pL+(i/(closes.length-1))*cW;

    if(strategy==="macd"){
      const{macdLine:ml,signalLine:sl,histogram:h}=calcMACD(closes);const maxV=Math.max(...[...ml,...sl].map(Math.abs))*1.2;
      const toY=v=>pT+cH/2-(v/maxV)*(cH/2);
      ctx.strokeStyle=t.textMuted+"30";ctx.beginPath();ctx.moveTo(pL,toY(0));ctx.lineTo(W-pR,toY(0));ctx.stroke();
      const bw=Math.max(2,cW/closes.length*0.7);
      for(let i=0;i<h.length;i++){ctx.fillStyle=h[i]>=0?t.green+"60":t.red+"60";const y0=toY(0),y1=toY(h[i]);ctx.fillRect(toX(i)-bw/2,Math.min(y0,y1),bw,Math.abs(y1-y0))}
      ctx.beginPath();ctx.strokeStyle=t.blue;ctx.lineWidth=1.5;for(let i=0;i<ml.length;i++){i===0?ctx.moveTo(toX(i),toY(ml[i])):ctx.lineTo(toX(i),toY(ml[i]))}ctx.stroke();
      ctx.beginPath();ctx.strokeStyle=t.orange;ctx.lineWidth=1.5;for(let i=0;i<sl.length;i++){i===0?ctx.moveTo(toX(i),toY(sl[i])):ctx.lineTo(toX(i),toY(sl[i]))}ctx.stroke();
    }
    if(strategy==="rsi"){
      const rsi=calcRSI(closes);const toY=v=>pT+cH-((v||0)/100)*cH;
      ctx.fillStyle=t.red+"0A";ctx.fillRect(pL,toY(100),cW,toY(70)-toY(100));
      ctx.fillStyle=t.green+"0A";ctx.fillRect(pL,toY(30),cW,toY(0)-toY(30));
      for(const[v,a]of[[70,"30"],[50,"15"],[30,"30"]]){ctx.strokeStyle=t.textMuted+a;ctx.setLineDash([3,3]);ctx.beginPath();ctx.moveTo(pL,toY(v));ctx.lineTo(W-pR,toY(v));ctx.stroke();ctx.setLineDash([])}
      ctx.beginPath();ctx.strokeStyle=t.purple;ctx.lineWidth=1.5;let st=false;for(let i=0;i<rsi.length;i++){if(rsi[i]===null)continue;if(!st){ctx.moveTo(toX(i),toY(rsi[i]));st=true}else ctx.lineTo(toX(i),toY(rsi[i]))}ctx.stroke();
      ctx.fillStyle=t.textMuted;ctx.font="10px Inter,sans-serif";ctx.textAlign="right";ctx.fillText("70",pL-6,toY(70)+3);ctx.fillText("50",pL-6,toY(50)+3);ctx.fillText("30",pL-6,toY(30)+3);
      // Current value label
      const lastRSI=rsi.filter(v=>v!==null).pop();if(lastRSI){ctx.fillStyle=t.purple;ctx.textAlign="left";ctx.fillText(lastRSI.toFixed(1),pL+cW+4,toY(lastRSI)+3)}
    }
    if(strategy==="stochastic"){
      const p=14;const kVals=[],dVals=[];
      for(let i=p-1;i<closes.length;i++){const sl=closes.slice(i-p+1,i+1);const hi=Math.max(...sl),lo=Math.min(...sl);kVals.push(lo===hi?50:((closes[i]-lo)/(hi-lo))*100)}
      // %D = 3-period SMA of %K
      for(let i=0;i<kVals.length;i++){if(i<2){dVals.push(null)}else{dVals.push((kVals[i]+kVals[i-1]+kVals[i-2])/3)}}
      const toXk=i=>pL+((i+p-1)/(closes.length-1))*cW;const toY=v=>pT+cH-(v/100)*cH;
      ctx.fillStyle=t.red+"0A";ctx.fillRect(pL,toY(100),cW,toY(80)-toY(100));
      ctx.fillStyle=t.green+"0A";ctx.fillRect(pL,toY(20),cW,toY(0)-toY(20));
      for(const[v,a]of[[80,"30"],[50,"15"],[20,"30"]]){ctx.strokeStyle=t.textMuted+a;ctx.setLineDash([3,3]);ctx.beginPath();ctx.moveTo(pL,toY(v));ctx.lineTo(W-pR,toY(v));ctx.stroke();ctx.setLineDash([])}
      ctx.beginPath();ctx.strokeStyle=t.orange;ctx.lineWidth=1.5;for(let i=0;i<kVals.length;i++){i===0?ctx.moveTo(toXk(i),toY(kVals[i])):ctx.lineTo(toXk(i),toY(kVals[i]))}ctx.stroke();
      ctx.beginPath();ctx.strokeStyle=t.blue;ctx.lineWidth=1;for(let i=0;i<dVals.length;i++){if(dVals[i]===null)continue;if(i===0||dVals[i-1]===null)ctx.moveTo(toXk(i),toY(dVals[i]));else ctx.lineTo(toXk(i),toY(dVals[i]))}ctx.stroke();
      ctx.fillStyle=t.textMuted;ctx.font="10px Inter,sans-serif";ctx.textAlign="right";ctx.fillText("80",pL-6,toY(80)+3);ctx.fillText("20",pL-6,toY(20)+3);
      const lastK=kVals[kVals.length-1];ctx.fillStyle=t.orange;ctx.textAlign="left";ctx.fillText(lastK.toFixed(1),pL+cW+4,toY(lastK)+3);
    }
    if(strategy==="atr"){
      const tr=[];for(let i=1;i<closes.length;i++)tr.push(Math.abs(closes[i]-closes[i-1]));
      const atrLine=calcEMA(tr,14);
      const maxATR=Math.max(...atrLine)*1.2;const minATR=Math.min(...atrLine)*0.8;
      const toY=v=>pT+cH-((v-minATR)/(maxATR-minATR))*cH;
      ctx.beginPath();ctx.strokeStyle=t.orange;ctx.lineWidth=1.5;
      for(let i=0;i<atrLine.length;i++){const x=toX(i+1),y=toY(atrLine[i]);i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}ctx.stroke();
      ctx.beginPath();ctx.moveTo(toX(1),toY(atrLine[0]));
      for(let i=1;i<atrLine.length;i++)ctx.lineTo(toX(i+1),toY(atrLine[i]));
      ctx.lineTo(toX(atrLine.length),pT+cH);ctx.lineTo(toX(1),pT+cH);ctx.closePath();ctx.fillStyle=t.orange+"15";ctx.fill();
      ctx.fillStyle=t.textMuted;ctx.font="10px Inter,sans-serif";ctx.textAlign="right";
      ctx.fillText("$"+maxATR.toFixed(2),pL-6,pT+8);ctx.fillText("$"+minATR.toFixed(2),pL-6,pT+cH);
      const lastATR=atrLine[atrLine.length-1];
      ctx.fillStyle=t.orange;ctx.textAlign="left";ctx.fillText("$"+lastATR.toFixed(2),pL+cW+4,toY(lastATR)+3);
    }
  },[closes,strategy,t]);
  if(!hasPanel)return null;
  const labels={macd:[["MACD",t.blue],["Signal",t.orange]],rsi:[["RSI (14)",t.purple]],stochastic:[["%K (14)",t.orange],["%D (3)",t.blue]],atr:[["ATR (14)",t.orange]]};
  return(<div style={{marginTop:"8px"}}>
    <div style={{fontSize:"10px",color:t.textMuted,marginBottom:"4px",display:"flex",gap:"12px"}}>
      {(labels[strategy]||[]).map(([label,color])=><span key={label}><span style={{color}}>—</span> {label}</span>)}
    </div>
    <canvas ref={canvasRef} style={{width:"100%",height:"110px",borderRadius:"8px",background:t.bg,border:`1px solid ${t.border}`}}/>
  </div>);
}

// ===================== INVESTMENT CALCULATOR =====================
function InvestmentCalc({t}){
  const[monthly,setMonthly]=useState(2000);const[years,setYears]=useState(10);const[rate,setRate]=useState(10);const[initial,setInitial]=useState(0);
  const canvasRef=useRef(null);
  const r=rate/100/12,n=years*12;const fv=r===0?initial+monthly*n:initial*Math.pow(1+r,n)+monthly*((Math.pow(1+r,n)-1)/r);
  const contrib=initial+monthly*12*years;const growth=fv-contrib;
  useEffect(()=>{
    const canvas=canvasRef.current;if(!canvas)return;const ctx=canvas.getContext("2d");const dpr=window.devicePixelRatio||1;const rect=canvas.getBoundingClientRect();
    canvas.width=rect.width*dpr;canvas.height=rect.height*dpr;ctx.scale(dpr,dpr);const W=rect.width,H=rect.height;ctx.clearRect(0,0,W,H);
    const rm=rate/100/12;const pts=[],cpts=[];for(let m=0;m<=years*12;m++){const fi=initial*Math.pow(1+rm,m);const fs=rm>0?monthly*((Math.pow(1+rm,m)-1)/rm):monthly*m;pts.push(fi+fs);cpts.push(initial+monthly*m)}
    const maxV=Math.max(...pts,1);const pT=20,pB=30,pL=60,pR=15,cW=W-pL-pR,cH=H-pT-pB;
    ctx.strokeStyle=t.border;ctx.lineWidth=1;for(let i=0;i<=4;i++){const y=pT+(cH/4)*i;ctx.beginPath();ctx.moveTo(pL,y);ctx.lineTo(W-pR,y);ctx.stroke();ctx.fillStyle=t.textMuted;ctx.font="10px Inter,sans-serif";ctx.textAlign="right";const v=maxV*(1-i/4);ctx.fillText("$"+(v>=1e6?(v/1e6).toFixed(1)+"M":v>=1e3?(v/1e3).toFixed(0)+"k":v.toFixed(0)),pL-6,y+3)}
    ctx.beginPath();ctx.moveTo(pL,pT+cH);for(let i=0;i<cpts.length;i++)ctx.lineTo(pL+(i/(cpts.length-1))*cW,pT+cH-(cpts[i]/maxV)*cH);ctx.lineTo(pL+cW,pT+cH);ctx.closePath();ctx.fillStyle=t.blue+"18";ctx.fill();
    ctx.beginPath();for(let i=0;i<pts.length;i++){const x=pL+(i/(pts.length-1))*cW,y=pT+cH-(pts[i]/maxV)*cH;i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}for(let i=cpts.length-1;i>=0;i--)ctx.lineTo(pL+(i/(cpts.length-1))*cW,pT+cH-(cpts[i]/maxV)*cH);ctx.closePath();ctx.fillStyle=t.accent+"18";ctx.fill();
    ctx.beginPath();ctx.strokeStyle=t.accent;ctx.lineWidth=2;for(let i=0;i<pts.length;i++){const x=pL+(i/(pts.length-1))*cW,y=pT+cH-(pts[i]/maxV)*cH;i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}ctx.stroke();
    ctx.beginPath();ctx.strokeStyle=t.blue;ctx.lineWidth=1.5;ctx.setLineDash([5,3]);for(let i=0;i<cpts.length;i++){const x=pL+(i/(cpts.length-1))*cW,y=pT+cH-(cpts[i]/maxV)*cH;i===0?ctx.moveTo(x,y):ctx.lineTo(x,y)}ctx.stroke();ctx.setLineDash([]);
    const step=years<=10?1:years<=20?2:5;ctx.fillStyle=t.textMuted;ctx.textAlign="center";ctx.font="10px Inter,sans-serif";for(let yr=0;yr<=years;yr+=step)ctx.fillText("Yr "+yr,pL+(yr/years)*cW,H-pB+16);
  },[monthly,years,rate,initial,t]);
  const fmt=n=>n>=1e6?"$"+(n/1e6).toFixed(2)+"M":"$"+n.toLocaleString("en-US",{maximumFractionDigits:0});
  const inputStyle={width:"100%",padding:"9px 12px",fontSize:"14px",fontFamily:"inherit",border:`1px solid ${t.inputBorder}`,borderRadius:"6px",background:t.inputBg,color:t.text,outline:"none"};
  return(<div>
    <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"14px",marginBottom:"16px"}}>
      {[["Initial Investment",initial,setInitial,"$"],[" Monthly Contribution",monthly,setMonthly,"$"],["Annual Return %",rate,setRate,null,"%"],["Years",years,setYears]].map(([l,v,s,pre,suf])=>
        <label key={l} style={{display:"flex",flexDirection:"column",gap:"5px"}}>
          <span style={{fontSize:"12px",fontWeight:"500",color:t.textSecondary}}>{l}</span>
          <div style={{position:"relative"}}>
            {pre&&<span style={{position:"absolute",left:"11px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"13px",pointerEvents:"none"}}>{pre}</span>}
            <input type="number" value={v} step={l.includes("Return")?0.5:1} onChange={e=>s(+e.target.value)} style={{...inputStyle,paddingLeft:pre?"26px":"12px",paddingRight:suf?"30px":"12px"}}/>
            {suf&&<span style={{position:"absolute",right:"11px",top:"50%",transform:"translateY(-50%)",color:t.textMuted,fontSize:"13px",pointerEvents:"none"}}>{suf}</span>}
          </div></label>)}
    </div>
    <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:"8px",marginBottom:"16px"}}>
      {[["Future Value",fmt(fv),t.accent],["Contributed",fmt(contrib),t.blue],["Growth",fmt(growth),t.accent]].map(([l,v,c])=>
        <div key={l} style={{background:t.surface,border:`1px solid ${t.border}`,borderRadius:"8px",padding:"12px",textAlign:"center"}}>
          <div style={{fontSize:"10px",color:t.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>{l}</div>
          <div style={{fontSize:"18px",fontWeight:"700",color:c}}>{v}</div></div>)}
    </div>
    <canvas ref={canvasRef} style={{width:"100%",height:"250px",borderRadius:"8px",background:t.bg,border:`1px solid ${t.border}`}}/>
  </div>);
}

// ===================== MAIN APP =====================
function App(){
  const[themeName,setThemeName]=useState("graphite");
  const[activeTab,setActiveTab]=useState("business");
  const[activeCalc,setActiveCalc]=useState("profit_margin");
  const[values,setValues]=useState({});
  const[results,setResults]=useState(null);
  const[filterCat,setFilterCat]=useState("All");
  const[searchGlossary,setSearchGlossary]=useState("");
  const[glossaryCat,setGlossaryCat]=useState("All");
  const[showSettings,setShowSettings]=useState(false);
  const[ticker,setTicker]=useState("AAPL");
  const[inputTicker,setInputTicker]=useState("AAPL");
  const[closes,setCloses]=useState([]);
  const[loading,setLoading]=useState(false);
  const[error,setError]=useState(null);
  const[lastPrice,setLastPrice]=useState(null);
  const[priceChange,setPriceChange]=useState(null);
  const[selectedStrategy,setSelectedStrategy]=useState("macd");
  const[expandedStrategy,setExpandedStrategy]=useState(null);
  const[filterDiff,setFilterDiff]=useState("All");
  const[learnCat,setLearnCat]=useState("All");
  const[sidebarOpen,setSidebarOpen]=useState(false);

  const th=THEMES[themeName];const calc=BIZ_CALCS[activeCalc];

  const handleChange=useCallback((key,val)=>{const nv={...values,[key]:val};setValues(nv);try{setResults(calc.calculate(nv))}catch{setResults(null)}},[values,calc]);
  const switchCalc=(id)=>{setActiveCalc(id);setValues({});setResults(null);setSidebarOpen(false)};
  const filteredCalcs=Object.entries(BIZ_CALCS).filter(([_,c])=>filterCat==="All"||c.category===filterCat);
  const filteredGlossary=GLOSSARY.filter(g=>(glossaryCat==="All"||g.cat===glossaryCat)&&(g.term.toLowerCase().includes(searchGlossary.toLowerCase())||g.def.toLowerCase().includes(searchGlossary.toLowerCase())));
  const GLOSSARY_CATS=["All",...[...new Set(GLOSSARY.map(g=>g.cat))]];
  const filteredStrats=LEARN_TOPICS.filter(s=>(learnCat==="All"||s.category===learnCat)&&(filterDiff==="All"||s.difficulty===filterDiff));
  const LEARN_CATS=["All",...[...new Set(LEARN_TOPICS.map(t=>t.category))]];

  useEffect(()=>{setValues({});setResults(null)},[activeCalc]);

  const loadTickerData = useCallback((sym) => {
    setLoading(true); setError(null);
    const d = HISTORICAL_DATA[sym];
    if (d) {
      const c = d.closes;
      setCloses(c);
      setLastPrice(c[c.length - 1]);
      setPriceChange(((c[c.length - 1] - c[c.length - 2]) / c[c.length - 2]) * 100);
    } else {
      setError("No data for this ticker");
      setCloses([]);
    }
    setLoading(false);
  }, []);
  useEffect(() => { if (activeTab === "market") loadTickerData(ticker) }, [ticker, activeTab]);


  const NAV_GROUPS = [
    {label:"Tools", items:[["business","Business"],["invest","Investing"],["market","Market"]]},
    {label:"Personal", items:[["budget","Budget"],["debt","Debt"],["networth","Net Worth"],["tax","Tax"]]},
    {label:"Planning", items:[["military","Military"],["retire","Retire"],["realestate","Real Estate"],["sidehustle","Side Hustle"],["crypto","Crypto DCA"]]},
    {label:"Learn", items:[["learn","Topics"],["glossary","Glossary"]]},
  ];
  const ALL_TABS = NAV_GROUPS.flatMap(g=>g.items);
  const activeGroup = NAV_GROUPS.find(g=>g.items.some(([k])=>k===activeTab));
  const [navOpen, setNavOpen] = useState(false);
  const inputStyle={width:"100%",padding:"9px 12px",fontSize:"14px",fontFamily:"inherit",border:`1px solid ${th.inputBorder}`,borderRadius:"6px",background:th.inputBg,color:th.text,outline:"none"};
  const diffColors={Beginner:th.green,Intermediate:th.accent,Advanced:th.red};

  // Floating calculator
  const [showCalc, setShowCalc] = useState(false);
  const [calcDisplay, setCalcDisplay] = useState("0");
  const [calcPrev, setCalcPrev] = useState(null);
  const [calcOp, setCalcOp] = useState(null);
  const [calcReset, setCalcReset] = useState(false);
  const calcInput = (v) => { if(calcReset){setCalcDisplay(v);setCalcReset(false)} else setCalcDisplay(calcDisplay==="0"?v:calcDisplay+v) };
  const calcOpFn = (op) => { setCalcPrev(parseFloat(calcDisplay)); setCalcOp(op); setCalcReset(true) };
  const calcEquals = () => {
    if(calcPrev===null||!calcOp) return;
    const cur=parseFloat(calcDisplay);
    let res=0;
    if(calcOp==="+") res=calcPrev+cur;
    else if(calcOp==="-") res=calcPrev-cur;
    else if(calcOp==="*") res=calcPrev*cur;
    else if(calcOp==="/") res=cur!==0?calcPrev/cur:0;
    setCalcDisplay(String(parseFloat(res.toFixed(8))));setCalcPrev(null);setCalcOp(null);setCalcReset(true);
  };
  const calcClear = () => { setCalcDisplay("0");setCalcPrev(null);setCalcOp(null);setCalcReset(false) };
  const calcPct = () => { setCalcDisplay(String(parseFloat(calcDisplay)/100)); setCalcReset(true) };
  const calcNeg = () => { setCalcDisplay(String(parseFloat(calcDisplay)*-1)) };
  const calcDot = () => { if(!calcDisplay.includes(".")) setCalcDisplay(calcDisplay+".") };

  return(
    <div style={{minHeight:"100vh",background:th.bg,color:th.text,fontFamily:"'Inter',-apple-system,BlinkMacSystemFont,sans-serif",transition:"background 0.3s"}}>
      <style>{`@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');*{box-sizing:border-box;margin:0;padding:0}input:focus,select:focus{border-color:${th.accent}!important;outline:none}::selection{background:${th.accentBg}}@media(max-width:720px){.cl-layout{grid-template-columns:1fr!important}.cl-sidebar{display:none!important}.cl-sidebar.open{display:flex!important;position:fixed;inset:0;z-index:100;background:${th.bg};padding:20px;overflow-y:auto}.cl-mob{display:flex!important}}`}</style>

      {/* Header */}
      <div style={{background:th.headerBg,borderBottom:`1px solid ${th.border}`}}>
        <div style={{maxWidth:"960px",margin:"0 auto",padding:"12px 20px",display:"flex",justifyContent:"space-between",alignItems:"center"}}>
          <div style={{display:"flex",alignItems:"center",gap:"10px"}}>
            <button className="cl-mob" onClick={()=>setSidebarOpen(!sidebarOpen)} style={{display:"none",alignItems:"center",justifyContent:"center",width:"30px",height:"30px",background:th.surface,border:`1px solid ${th.border}`,borderRadius:"5px",color:th.textMuted,cursor:"pointer",fontSize:"13px",fontFamily:"inherit"}}>{"\u2630"}</button>
            <div>
              <h1 style={{fontSize:"17px",fontWeight:"700",letterSpacing:"-0.3px"}}>Zuvo</h1>
              <p style={{fontSize:"11px",color:th.textMuted,marginTop:"1px"}}>Finance toolkit</p>
            </div>
          </div>
          <div style={{display:"flex",alignItems:"center",gap:"6px"}}>
            <div style={{position:"relative"}}>
              <button onClick={()=>setShowSettings(!showSettings)} style={{width:"30px",height:"30px",display:"flex",alignItems:"center",justifyContent:"center",background:showSettings?th.accentBg:th.surface,border:`1px solid ${showSettings?th.accentBorder:th.border}`,borderRadius:"5px",cursor:"pointer",color:showSettings?th.accentText:th.textMuted,fontSize:"13px",fontFamily:"inherit"}}>{"\u2699"}</button>
              {showSettings&&<div style={{position:"absolute",top:"38px",right:0,background:th.surface,border:`1px solid ${th.border}`,borderRadius:"9px",padding:"10px",width:"180px",zIndex:50,boxShadow:"0 8px 30px rgba(0,0,0,0.3)"}}>
                <div style={{fontSize:"10px",fontWeight:"600",color:th.textMuted,textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"6px"}}>Theme</div>
                {Object.entries(THEMES).map(([k,v])=><button key={k} onClick={()=>{setThemeName(k);setShowSettings(false)}} style={{display:"flex",alignItems:"center",gap:"8px",width:"100%",padding:"7px 8px",border:"none",borderRadius:"5px",cursor:"pointer",fontFamily:"inherit",fontSize:"12px",fontWeight:"500",textAlign:"left",background:themeName===k?th.accentBg:"transparent",color:themeName===k?th.accentText:th.textSecondary}}>
                  <span style={{width:"12px",height:"12px",borderRadius:"3px",background:v.accent,border:`1px solid ${v.border}`,flexShrink:0}}></span>{v.name}</button>)}
              </div>}
            </div>
          </div>
        </div>
        {/* Nav: Category groups on top, active group items below */}
        <div style={{maxWidth:"960px",margin:"0 auto",padding:"0 20px 10px"}}>
          <div style={{display:"flex",gap:"4px",marginBottom:"8px"}}>
            {NAV_GROUPS.map(function(g){
              const isActive = g === activeGroup;
              return <button key={g.label} onClick={function(){if(!isActive){setActiveTab(g.items[0][0]);setNavOpen(false)}}} style={{padding:"5px 12px",fontSize:"11px",fontWeight:isActive?"600":"500",border:"1px solid "+(isActive?th.accentBorder:th.border),borderRadius:"6px",cursor:"pointer",fontFamily:"inherit",background:isActive?th.accentBg:"transparent",color:isActive?th.accentText:th.textMuted,transition:"all 0.15s"}}>{g.label}</button>
            })}
          </div>
          {activeGroup && <div style={{display:"flex",gap:"2px",flexWrap:"wrap"}}>
            {activeGroup.items.map(function(item){
              var k=item[0],l=item[1];
              return <button key={k} onClick={function(){setActiveTab(k)}} style={{padding:"4px 10px",fontSize:"11px",fontWeight:activeTab===k?"600":"400",border:"none",borderRadius:"4px",cursor:"pointer",fontFamily:"inherit",background:activeTab===k?th.surface:"transparent",color:activeTab===k?th.text:th.textMuted,transition:"all 0.15s"}}>{l}</button>
            })}
          </div>}
        </div>
      </div>
      {showSettings&&<div onClick={()=>setShowSettings(false)} style={{position:"fixed",inset:0,zIndex:40}}></div>}

      <div style={{maxWidth:"960px",margin:"0 auto",padding:"20px"}}>

        {/* BUSINESS CALCS */}
        {activeTab==="business"&&<div className="cl-layout" style={{display:"grid",gridTemplateColumns:"200px 1fr",gap:"20px"}}>
          <div className={`cl-sidebar${sidebarOpen?" open":""}`} style={{display:"flex",flexDirection:"column",gap:"2px"}}>
            {sidebarOpen&&<button onClick={()=>setSidebarOpen(false)} style={{alignSelf:"flex-end",padding:"5px 10px",marginBottom:"10px",background:th.surface,border:`1px solid ${th.border}`,borderRadius:"5px",color:th.textMuted,fontSize:"11px",cursor:"pointer",fontFamily:"inherit"}}>Close</button>}
            <div style={{display:"flex",flexWrap:"wrap",gap:"3px",marginBottom:"8px"}}>{BIZ_CATEGORIES.map(c=><button key={c} onClick={()=>setFilterCat(c)} style={{padding:"3px 8px",fontSize:"10px",fontWeight:"500",border:`1px solid ${filterCat===c?th.accentBorder:th.border}`,borderRadius:"4px",cursor:"pointer",fontFamily:"inherit",background:filterCat===c?th.accentBg:"transparent",color:filterCat===c?th.accentText:th.textMuted}}>{c}</button>)}</div>
            {filteredCalcs.map(([id,c])=><button key={id} onClick={()=>switchCalc(id)} style={{padding:"8px 10px",fontSize:"12px",fontWeight:activeCalc===id?"600":"400",border:"none",borderRadius:"5px",cursor:"pointer",fontFamily:"inherit",textAlign:"left",background:activeCalc===id?th.sidebarActive:"transparent",color:activeCalc===id?th.sidebarActiveText:th.textSecondary}}>{c.name}</button>)}
          </div>
          <div style={{background:th.surface,borderRadius:"9px",border:`1px solid ${th.border}`}}>
            <div style={{padding:"16px 20px",borderBottom:`1px solid ${th.borderLight}`}}>
              <h2 style={{fontSize:"15px",fontWeight:"700",marginBottom:"2px"}}>{calc.name}</h2>
              <p style={{fontSize:"12px",color:th.textMuted}}>{calc.description}</p></div>
            <div style={{padding:"20px"}}>
              <div style={{display:"grid",gridTemplateColumns:calc.fields.length<=2?"1fr":"1fr 1fr",gap:"12px",marginBottom:"16px"}}>
                {calc.fields.map(f=><div key={f.key}>
                  <label style={{display:"block",fontSize:"11px",fontWeight:"500",color:th.textSecondary,marginBottom:"4px"}}>{f.label}</label>
                  {f.type==="toggle"?<button onClick={()=>handleChange(f.key,!values[f.key])} style={{...inputStyle,cursor:"pointer",textAlign:"center",fontSize:"12px",fontWeight:"500",background:values[f.key]?th.accentBg:th.inputBg,color:values[f.key]?th.accentText:th.textMuted,borderColor:values[f.key]?th.accentBorder:th.inputBorder}}>{values[f.key]?"Yes — include SE tax":"No — W-2 employee"}</button>
                  :f.type==="select"?<select value={values[f.key]||f.options[0]} onChange={e=>handleChange(f.key,e.target.value)} style={{...inputStyle,cursor:"pointer"}}>{f.options.map(o=><option key={o} value={o}>{o}</option>)}</select>
                  :<div style={{position:"relative"}}>{f.prefix&&<span style={{position:"absolute",left:"11px",top:"50%",transform:"translateY(-50%)",color:th.textMuted,fontSize:"13px",pointerEvents:"none"}}>{f.prefix}</span>}<input type="number" placeholder={f.placeholder} value={values[f.key]||""} onChange={e=>handleChange(f.key,e.target.value)} style={{...inputStyle,paddingLeft:f.prefix?"26px":"12px",paddingRight:f.suffix?"28px":"12px"}}/>{f.suffix&&<span style={{position:"absolute",right:"11px",top:"50%",transform:"translateY(-50%)",color:th.textMuted,fontSize:"13px",pointerEvents:"none"}}>{f.suffix}</span>}</div>}
                </div>)}
              </div>
              {results&&results.length>0&&<div style={{borderTop:`1px solid ${th.borderLight}`,paddingTop:"14px"}}>
                {results.map((r,i)=>r.divider?<div key={i} style={{fontSize:"10px",color:th.textMuted,textAlign:"center",padding:"5px 0"}}>{r.label}</div>
                  :<div key={i} style={{display:"flex",justifyContent:"space-between",alignItems:"center",padding:"8px 10px",borderRadius:"5px",marginBottom:"2px",background:r.highlight?th.resultHighlight:"transparent",border:`1px solid ${r.highlight?th.resultHighlightBorder:"transparent"}`}}>
                    <span style={{fontSize:"12px",color:r.highlight?th.resultHighlightText:th.textMuted,fontWeight:r.highlight?"500":"400"}}>{r.label}</span>
                    <span style={{fontSize:r.highlight?"15px":"13px",fontWeight:r.highlight?"700":"500",color:r.highlight?th.resultHighlightText:th.text,fontVariantNumeric:"tabular-nums"}}>{r.value}</span></div>)}
              </div>}
              <div style={{marginTop:"16px",padding:"10px 12px",background:th.tipBg,border:`1px solid ${th.tipBorder}`,borderRadius:"6px"}}>
                <div style={{fontSize:"10px",fontWeight:"600",color:th.tipText,marginBottom:"2px"}}>Quick Tip</div>
                <p style={{fontSize:"11px",color:th.tipText,lineHeight:"1.5",margin:0,opacity:0.85}}>{calc.tip}</p></div>
            </div>
          </div>
        </div>}

        {/* INVESTMENT */}
        {activeTab==="invest"&&<div style={{maxWidth:"700px",margin:"0 auto"}}><InvestmentCalc t={th}/></div>}

        {/* MARKET ANALYSIS */}
        {activeTab==="market"&&<div>
          <div style={{display:"flex",gap:"8px",marginBottom:"12px"}}>
            <input value={inputTicker} onChange={e=>setInputTicker(e.target.value.toUpperCase())} onKeyDown={e=>e.key==="Enter"&&(()=>{setTicker(inputTicker.trim().toUpperCase())})()}
              placeholder="Ticker..." style={{...inputStyle,flex:1,maxWidth:"200px"}}/>
            <button onClick={()=>setTicker(inputTicker.trim().toUpperCase())} style={{padding:"9px 16px",background:th.accentBg,border:`1px solid ${th.accentBorder}`,borderRadius:"6px",color:th.accentText,fontSize:"12px",cursor:"pointer",fontFamily:"inherit",fontWeight:"500"}}>Search</button>
          </div>
          <div style={{display:"flex",gap:"4px",marginBottom:"14px",flexWrap:"wrap"}}>
            {POPULAR_TICKERS.map(t2=><button key={t2.symbol} onClick={()=>{setTicker(t2.symbol);setInputTicker(t2.symbol)}} style={{background:ticker===t2.symbol?th.accentBg:"transparent",border:`1px solid ${ticker===t2.symbol?th.accentBorder:th.border}`,borderRadius:"4px",padding:"4px 8px",cursor:"pointer",color:ticker===t2.symbol?th.accentText:th.textMuted,fontSize:"10px",fontFamily:"inherit"}}>{t2.symbol}</button>)}
          </div>
          {lastPrice&&!loading&&<div style={{marginBottom:"12px",display:"flex",alignItems:"baseline",gap:"10px"}}>
            <span style={{fontSize:"24px",fontWeight:"700"}}>{ticker}</span>
            <span style={{fontSize:"20px",color:th.textSecondary}}>${lastPrice.toFixed(lastPrice>100?2:4)}</span>
            {priceChange!==null&&<span style={{fontSize:"13px",color:priceChange>=0?th.green:th.red}}>{priceChange>=0?"+":""}{priceChange.toFixed(2)}%</span>}
          </div>}
          <div style={{display:"flex",gap:"4px",marginBottom:"12px",flexWrap:"wrap"}}>
            {STRATEGIES.map(s=><button key={s.id} onClick={()=>setSelectedStrategy(s.id)} style={{background:selectedStrategy===s.id?th.accentBg:"transparent",border:`1px solid ${selectedStrategy===s.id?th.accentBorder:th.border}`,borderRadius:"4px",padding:"5px 10px",cursor:"pointer",color:selectedStrategy===s.id?th.accentText:th.textMuted,fontSize:"11px",fontFamily:"inherit"}}>{s.name}</button>)}
          </div>
          {loading&&<div style={{textAlign:"center",padding:"50px",color:th.textMuted}}>Loading {ticker}...</div>}
          {error&&<div style={{textAlign:"center",padding:"30px",color:th.red}}>{error}</div>}
          {!loading&&!error&&closes.length>0&&<><StockChart closes={closes} strategy={selectedStrategy} t={th}/><SubIndicator closes={closes} strategy={selectedStrategy} t={th}/></>}
          <div style={{marginTop:"14px",padding:"10px 12px",background:th.tipBg,border:`1px solid ${th.tipBorder}`,borderRadius:"6px"}}>
            <p style={{fontSize:"11px",color:th.tipText,margin:0,opacity:0.85}}>Forecasts are hypothetical based on technical indicators and historical volatility. Not predictions. For educational purposes only.</p></div>
        </div>}

        {/* MILITARY */}

        {/* MILITARY */}
        {activeTab==="military"&&<MilitaryCalculator t={th}/>}

        {/* DEBT */}
        {activeTab==="debt"&&<DebtPayoff t={th}/>}

        {/* BUDGET */}
        {activeTab==="budget"&&<BudgetBuilder t={th}/>}

        {/* NET WORTH */}
        {activeTab==="networth"&&<NetWorthTracker t={th}/>}

        {/* REAL ESTATE */}
        {activeTab==="realestate"&&<RealEstateCalc t={th}/>}

        {/* TAX */}
        {activeTab==="tax"&&<TaxEstimator t={th}/>}

        {/* SIDE HUSTLE */}
        {activeTab==="sidehustle"&&<SideHustleCalc t={th}/>}

        {/* RETIRE */}
        {activeTab==="retire"&&<RetirementCalc t={th}/>}

        {/* CRYPTO DCA */}
        {activeTab==="crypto"&&<CryptoDCA t={th}/>}

        {activeTab==="learn"&&<div style={{maxWidth:"700px",margin:"0 auto"}}>
          <div style={{display:"flex",gap:"4px",marginBottom:"8px",flexWrap:"wrap"}}>
            {LEARN_CATS.map(c=><button key={c} onClick={()=>setLearnCat(c)} style={{padding:"5px 10px",fontSize:"10px",fontWeight:"500",border:`1px solid ${learnCat===c?th.accentBorder:th.border}`,borderRadius:"4px",cursor:"pointer",fontFamily:"inherit",background:learnCat===c?th.accentBg:"transparent",color:learnCat===c?th.accentText:th.textMuted}}>{c}</button>)}
          </div>
          <div style={{display:"flex",gap:"4px",marginBottom:"12px",flexWrap:"wrap",alignItems:"center"}}>
            {["All","Beginner","Intermediate","Advanced"].map(l=><button key={l} onClick={()=>setFilterDiff(l)} style={{padding:"4px 10px",fontSize:"10px",fontWeight:"500",border:`1px solid ${filterDiff===l?th.accentBorder:th.border}`,borderRadius:"4px",cursor:"pointer",fontFamily:"inherit",background:filterDiff===l?th.accentBg:"transparent",color:filterDiff===l?th.accentText:th.textMuted}}>{l}</button>)}
            <span style={{fontSize:"10px",color:th.textMuted,marginLeft:"8px"}}>{filteredStrats.length} topics</span>
          </div>
          <div style={{display:"flex",flexDirection:"column",gap:"8px"}}>
            {filteredStrats.map(s=><div key={s.id} onClick={()=>setExpandedStrategy(expandedStrategy===s.id?null:s.id)} style={{background:th.surface,border:`1px solid ${th.border}`,borderRadius:"9px",padding:"16px 18px",cursor:"pointer",borderLeft:`3px solid ${diffColors[s.difficulty]||th.accent}`}}>
              <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
                <div>
                  <div style={{display:"flex",alignItems:"center",gap:"8px",marginBottom:"2px"}}>
                    <h3 style={{margin:0,fontSize:"15px",fontWeight:"700"}}>{s.name}</h3>
                    <span style={{fontSize:"9px",fontFamily:"inherit",padding:"2px 6px",borderRadius:"3px",background:th.bg,color:diffColors[s.difficulty],border:`1px solid ${th.border}`,textTransform:"uppercase",fontWeight:"600"}}>{s.difficulty}</span>
                    <span style={{fontSize:"9px",padding:"2px 6px",borderRadius:"3px",background:th.bg,color:th.textMuted,border:`1px solid ${th.border}`}}>{s.timeframe}</span>
                    {s.category&&<span style={{fontSize:"8px",padding:"2px 5px",borderRadius:"3px",background:th.accentBg,color:th.accentText,border:`1px solid ${th.accentBorder}`,textTransform:"uppercase",letterSpacing:"0.3px"}}>{s.category}</span>}
                  </div>
                  <div style={{color:th.textMuted,fontSize:"11px"}}>{s.fullName}</div>
                </div>
                <span style={{color:th.textMuted,fontSize:"16px",transform:expandedStrategy===s.id?"rotate(180deg)":"rotate(0)",transition:"transform 0.2s"}}>▾</span>
              </div>
              {expandedStrategy===s.id&&<div style={{marginTop:"12px"}} onClick={e=>e.stopPropagation()}>
                <p style={{color:th.textSecondary,lineHeight:"1.6",fontSize:"12px",marginBottom:"12px"}}>{s.description}</p>
                <div style={{marginBottom:"12px"}}>
                  <h4 style={{color:th.accentText,fontSize:"10px",textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"6px"}}>Signals</h4>
                  {s.signals.map((sig,i)=><div key={i} style={{padding:"7px 10px",marginBottom:"3px",borderRadius:"5px",background:th.accentBg,border:`1px solid ${th.accentBorder}`,color:th.textSecondary,fontSize:"11px",lineHeight:"1.4"}}>{sig}</div>)}
                </div>
                <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"8px",marginBottom:"10px"}}>
                  {[["Settings",s.settings],["Best For",s.bestFor]].map(([l,v])=><div key={l} style={{background:th.bg,borderRadius:"6px",padding:"9px 10px",border:`1px solid ${th.border}`}}>
                    <div style={{color:th.textMuted,fontSize:"9px",textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"3px"}}>{l}</div>
                    <div style={{color:th.textSecondary,fontSize:"11px",lineHeight:"1.4"}}>{v}</div></div>)}
                </div>
                <div style={{background:th.tipBg,border:`1px solid ${th.tipBorder}`,borderRadius:"6px",padding:"9px 10px"}}>
                  <div style={{color:th.tipText,fontSize:"9px",textTransform:"uppercase",letterSpacing:"0.5px",marginBottom:"2px",fontWeight:"600"}}>Pro Tip</div>
                  <div style={{color:th.tipText,fontSize:"11px",lineHeight:"1.5",opacity:0.9}}>{s.proTip}</div></div>
              </div>}
            </div>)}
          </div>
        </div>}

        {/* GLOSSARY */}
        {activeTab==="glossary"&&<div style={{maxWidth:"650px",margin:"0 auto"}}>
          <input placeholder="Search terms..." value={searchGlossary} onChange={e=>setSearchGlossary(e.target.value)} style={{...inputStyle,marginBottom:"10px"}}/>
          <div style={{display:"flex",gap:"4px",marginBottom:"14px",flexWrap:"wrap"}}>
            {GLOSSARY_CATS.map(c=><button key={c} onClick={()=>setGlossaryCat(c)} style={{padding:"4px 10px",fontSize:"10px",fontWeight:"500",border:`1px solid ${glossaryCat===c?th.accentBorder:th.border}`,borderRadius:"4px",cursor:"pointer",fontFamily:"inherit",background:glossaryCat===c?th.accentBg:"transparent",color:glossaryCat===c?th.accentText:th.textMuted}}>{c}{c!=="All"?` (${GLOSSARY.filter(g=>g.cat===c).length})`:""}</button>)}
          </div>
          <div style={{fontSize:"11px",color:th.textMuted,marginBottom:"10px"}}>{filteredGlossary.length} terms{glossaryCat!=="All"?" in "+glossaryCat:""}</div>
          <div style={{background:th.surface,borderRadius:"9px",border:`1px solid ${th.border}`,overflow:"hidden"}}>
            {filteredGlossary.map((g,i)=><div key={i} style={{padding:"12px 16px",borderBottom:i<filteredGlossary.length-1?`1px solid ${th.borderLight}`:"none"}}>
              <div style={{display:"flex",alignItems:"center",gap:"8px",marginBottom:"2px"}}>
                <span style={{fontSize:"13px",fontWeight:"600"}}>{g.term}</span>
                <span style={{fontSize:"8px",padding:"1px 5px",borderRadius:"3px",background:th.bg,color:th.textMuted,border:`1px solid ${th.border}`,textTransform:"uppercase",letterSpacing:"0.3px"}}>{g.cat}</span>
              </div>
              <div style={{fontSize:"12px",color:th.textSecondary,lineHeight:"1.5"}}>{g.def}</div></div>)}
            {filteredGlossary.length===0&&<div style={{padding:"30px",textAlign:"center",color:th.textMuted,fontSize:"12px"}}>No terms found</div>}
          </div>
        </div>}
      </div>

      {/* Floating Calculator Toggle */}
      <button onClick={()=>setShowCalc(!showCalc)} style={{position:"fixed",bottom:"20px",right:"20px",width:"48px",height:"48px",borderRadius:"50%",background:th.accent,border:"none",cursor:"pointer",display:"flex",alignItems:"center",justifyContent:"center",boxShadow:"0 4px 12px rgba(0,0,0,0.3)",zIndex:50,fontSize:"20px",color:th.bg,fontWeight:"700"}}>
        {showCalc?"\u2715":"\u2261"}
      </button>

      {/* Floating Calculator */}
      {showCalc&&<div style={{position:"fixed",bottom:"80px",right:"20px",width:"240px",background:th.surface,border:"1px solid "+th.border,borderRadius:"12px",boxShadow:"0 8px 24px rgba(0,0,0,0.3)",zIndex:50,overflow:"hidden"}}>
        <div style={{padding:"14px 14px 8px",background:th.bg,borderBottom:"1px solid "+th.border}}>
          <div style={{fontSize:"10px",color:th.textMuted,textAlign:"right",height:"14px"}}>{calcPrev!==null?calcPrev+" "+calcOp:""}</div>
          <div style={{fontSize:"24px",fontWeight:"700",textAlign:"right",color:th.text,overflow:"hidden",textOverflow:"ellipsis"}}>{calcDisplay}</div>
        </div>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr 1fr",gap:"1px",padding:"1px",background:th.border}}>
          {[
            ["C",calcClear,th.textMuted,th.bg],["+/-",calcNeg,th.textMuted,th.bg],["%",calcPct,th.textMuted,th.bg],["/",()=>calcOpFn("/"),th.accent,th.accentBg],
            ["7",()=>calcInput("7"),th.text,th.surface],["8",()=>calcInput("8"),th.text,th.surface],["9",()=>calcInput("9"),th.text,th.surface],["*",()=>calcOpFn("*"),th.accent,th.accentBg],
            ["4",()=>calcInput("4"),th.text,th.surface],["5",()=>calcInput("5"),th.text,th.surface],["6",()=>calcInput("6"),th.text,th.surface],["-",()=>calcOpFn("-"),th.accent,th.accentBg],
            ["1",()=>calcInput("1"),th.text,th.surface],["2",()=>calcInput("2"),th.text,th.surface],["3",()=>calcInput("3"),th.text,th.surface],["+",()=>calcOpFn("+"),th.accent,th.accentBg],
            ["0",()=>calcInput("0"),th.text,th.surface],["00",()=>calcInput("00"),th.text,th.surface],[".",calcDot,th.text,th.surface],["=",calcEquals,th.bg,th.accent],
          ].map(function(x,i){return <button key={i} onClick={x[1]} style={{padding:"12px",fontSize:"15px",fontWeight:"500",border:"none",cursor:"pointer",fontFamily:"inherit",color:x[2],background:x[3]}}>{x[0]}</button>})}
        </div>
      </div>}

      <div style={{borderTop:"1px solid "+th.border,padding:"12px 20px",marginTop:"28px"}}>
        <div style={{maxWidth:"960px",margin:"0 auto",display:"flex",justifyContent:"space-between"}}>
          <span style={{fontSize:"10px",color:th.textMuted}}>Not financial advice. Consult a professional.</span>
          <span style={{fontSize:"10px",color:th.textMuted,opacity:0.5}}>Zuvo 2026</span>
        </div>
      </div>
    </div>
  );
}

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
  </script>
</body>
</html>
