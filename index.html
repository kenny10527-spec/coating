<!doctype html>
<html lang="zh-Hant">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>鍍膜營運管理系統 (雲端版)</title>
<script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.0/firebase-firestore-compat.js"></script>

<style>
:root{--bg:#000000;--panel:#121212;--panel-border:#2a2a2a;--text:#ffffff;--muted:#888888;--light-gray:#cccccc;--pill-bg:#222222}
*{box-sizing:border-box}html{background:#000}body{margin:0;background:var(--bg);color:var(--text);font-family:-apple-system,BlinkMacSystemFont,sans-serif}.app{max-width:520px;margin:auto;padding-bottom:92px}.top{position:sticky;top:0;z-index:10;padding:16px;background:#000000e8;backdrop-filter:blur(18px);border-bottom:1px solid var(--panel-border);display:flex;justify-content:space-between;align-items:center}.logo{font-size:20px;font-weight:900;letter-spacing:2px;color:#fff}.tag{font-size:10px;color:var(--muted);letter-spacing:1.5px}.page{padding:14px 16px}.hide{display:none}.hero{padding:18px;border:1px solid #333333;border-radius:18px;background:radial-gradient(circle at 90% 10%,#222222,#0a0a0a)}.label{font-size:12px;color:var(--muted)}.heroNum{font-size:44px;font-weight:900;margin:4px 0;color:#fff}.gold{color:#ffffff;font-weight:bold}.grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:10px}.card{background:var(--panel);border:1px solid var(--panel-border);border-radius:14px;padding:14px}.card b{display:block;font-size:21px;margin-top:5px;color:#fff}.section{display:flex;justify-content:space-between;align-items:center;margin:20px 2px 9px;font-weight:800;color:var(--light-gray)}.list{background:var(--panel);border:1px solid var(--panel-border);border-radius:14px;overflow:hidden}.row{display:flex;justify-content:space-between;align-items:center;padding:13px 14px;border-bottom:1px solid #222222}.row:last-child{border:0}.row small{display:block;color:var(--muted);margin-top:4px;font-size:11px}.pill{font-size:10px;padding:4px 8px;border-radius:99px;background:var(--pill-bg);color:#ffffff;border:1px solid #444444}.warn{background:#333333;color:#ffffff;border-color:#666666}.danger{background:#ffffff;color:#000000;font-weight:bold;border-color:#ffffff}.btn{width:100%;border-radius:11px;padding:13px;border:1px solid #ffffff;background:#ffffff;color:#000000;font-weight:900;font-size:15px;cursor:pointer}.btn.dark{background:#1a1a1a;color:#ffffff;border-color:#444444}.btn.red{background:#000000;color:#ffffff;border-color:#888888}.form{display:grid;gap:12px}.field label{display:flex;justify-content:space-between;color:var(--muted);font-size:12px;margin-bottom:6px}.field input,.field select{width:100%;background:#0a0a0a;border:1px solid #333333;color:#fff;border-radius:10px;padding:12px;font-size:15px;outline:0}.field input:focus,.field select:focus{border-color:#ffffff}.qty{display:grid;grid-template-columns:48px 1fr 48px;gap:7px}.qty button{border:1px solid #444444;background:#1a1a1a;color:#ffffff;border-radius:10px;font-size:22px}.qty input{text-align:center}.bottom{position:fixed;bottom:0;left:50%;transform:translateX(-50%);width:min(520px,100%);z-index:20;display:grid;grid-template-columns:repeat(5,1fr);padding:8px 4px calc(8px + env(safe-area-inset-bottom));background:#050505f2;border-top:1px solid var(--panel-border)}.nav{border:0;background:none;color:#555555;font-size:10px;cursor:pointer}.nav strong{display:block;font-size:19px}.nav.active{color:#ffffff}.empty{text-align:center;color:#666;padding:28px}.price{color:#ffffff;font-weight:800}.stock-item{padding:13px 14px;border-bottom:1px solid #222222;display:grid;gap:8px}.stock-ctrls{display:flex;gap:6px;align-items:center;margin-top:4px}.stock-ctrls button{background:#1a1a1a;border:1px solid #444444;color:#ffffff;padding:6px 12px;border-radius:6px;font-size:12px;font-weight:bold;cursor:pointer}
</style>
</head>
<body>
<div class="app">
<header class="top"><div><div class="logo">鍍膜營運管理</div><div class="tag">COATING OPERATIONS SYSTEM</div></div><div style="color:#ffffff;font-size:18px">❖</div></header>

<main id="home" class="page">
<section class="hero"><div class="label">今日鍍膜台數</div><div class="heroNum" id="today">0 台</div><div class="label">本月累計 <span class="gold" id="month">0</span> 台</div></section>
<div class="grid">
<div class="card"><span class="label">本月綜合成本 (含水電藥水)</span><b class="price" id="mCost">$0</b></div>
<div class="card"><span class="label">庫存總價值</span><b id="stockVal">$0</b></div>
<div class="card"><span class="label">低庫存</span><b id="low">0 項</b></div>
<div class="card"><span class="label">平均成本／台</span><b class="price" id="avg">$0</b></div>
</div>
<div class="section">庫存警示</div><div class="list" id="homeLow"></div>
<div class="section">最近鍍膜紀錄 (點擊可刪除)</div><div class="list" id="homeRecent"></div>
</main>

<main id="coat" class="page hide">
<div class="section">新增鍍膜紀錄</div>
<div class="form">
<div class="field"><label>施工日期</label><input id="date" type="date"></div>
<div class="field"><label>廠別</label><select id="brand"></select></div>
<div class="field"><label>車型</label><input id="model" placeholder="自行輸入車型 (例如: RAV4, Model Y)"></div>
<div class="field"><label>車色</label><input id="color" placeholder="自行輸入車色 (例如: 珍珠白, 消光黑)"></div>
<div class="field"><label>車牌</label><input id="plate" placeholder="例如 ABC-1234"></div>

<div class="grid" style="margin-top:0">
  <div class="field"><label>漆面鍍膜劑</label><select id="coatSelect"></select></div>
  <div class="field"><label>拋光劑</label><select id="polishSelect"></select></div>
</div>

<div class="field"><label>鍍膜台數</label><div class="qty"><button onclick="qty(-1)">−</button><input id="amount" type="number" value="1" min="1"><button onclick="qty(1)">＋</button></div></div>
<button class="btn" onclick="saveCoat()">確認新增＋自動扣耗材</button>
</div>
</main>

<main id="stock" class="page hide">
<div class="section">＋ 新增 / 補充耗材</div>
<div class="form" style="background:var(--panel);padding:14px;border-radius:14px;border:1px solid var(--panel-border);">
  <div class="field">
    <label>耗材名稱 (選擇現有或選擇自訂)</label>
    <select id="addNameSelect" onchange="toggleCustomStockName()"></select>
  </div>
  <div class="field hide" id="customNameField">
    <label>自訂全新耗材名稱</label>
    <input id="addCustomName" placeholder="例如：新版封體劑">
  </div>
  <div class="grid" style="margin-top:0">
    <div class="field"><label>分類</label><select id="addCat"><option>鍍膜</option><option>拋光</option><option>耗材</option></select></div>
    <div class="field"><label>單位</label><input id="addUnit" placeholder="瓶/條/個" value="瓶"></div>
  </div>
  <div class="grid" style="margin-top:0">
    <div class="field"><label>補充／新增數量</label><input id="addStock" type="number" value="10"></div>
    <div class="field"><label>安全庫存</label><input id="addSafe" type="number" value="5"></div>
  </div>
  <div class="field"><label>單價 ($)</label><input id="addPrice" type="number" value="500"></div>
  <button class="btn" onclick="addNewStock()">加入 / 補充庫存</button>
</div>

<div class="section">現有耗材清單</div>
<div class="list" id="stockList"></div>
</main>

<main id="report" class="page hide">
<div class="section">營運報表</div>
<div class="grid"><div class="card"><span class="label">鍍膜</span><b id="rcount">0 台</b></div><div class="card"><span class="label">綜合成本</span><b class="price" id="rcost">$0</b></div></div>
<div class="section">各廠別分析</div><div class="list" id="brandAnalysis"></div>
</main>

<main id="more" class="page hide">
<div class="section">更多功能</div>
<button class="btn red" onclick="resetData()">重置示範資料</button>
</main>

<nav class="bottom">
<button class="nav active" data-p="home" onclick="show('home')"><strong>⌂</strong>首頁</button>
<button class="nav" data-p="coat" onclick="show('coat')"><strong>🚗</strong>鍍膜</button>
<button class="nav" data-p="stock" onclick="show('stock')"><strong>▣</strong>庫存</button>
<button class="nav" data-p="report" onclick="show('report')"><strong>▥</strong>報表</button>
<button class="nav" data-p="more" onclick="show('more')"><strong>•••</strong>更多</button>
</nav>
</div>

<script>
const firebaseConfig = {
  apiKey: "AIzaSyAX5fgbmIHWUWfu2OZ5G0VGo5Za-UrahEw",
  authDomain: "coating-system.firebaseapp.com",
  projectId: "coating-system",
  storageBucket: "coating-system.firebasestorage.app",
  messagingSenderId: "662264286977",
  appId: "1:662264286977:web:5043b9a4f9aec66f879500",
  measurementId: "G-1BY53F0JGM"
};

if (firebaseConfig.apiKey !== "YOUR_API_KEY") {
  firebase.initializeApp(firebaseConfig);
  var db = firebase.firestore();
}

const eBrands = Array.from({length: 22}, (_, i) => `E${String(i + 1).padStart(2, '0')}`);
const FIXED_COST_PER_CAR = 1600;

const ALL_PRESET_ITEMS = [
  {id:1, name:'鍍膜藍', cat:'鍍膜', spec:'50ml', unit:'瓶', stock:10, safe:3, price:2600, usePerCar:20},
  {id:2, name:'鍍膜綠', cat:'鍍膜', spec:'50ml', unit:'瓶', stock:10, safe:3, price:2600, usePerCar:20},
  {id:3, name:'鍍膜透明', cat:'鍍膜', spec:'50ml', unit:'瓶', stock:10, safe:3, price:2600, usePerCar:20},
  {id:4, name:'0號拋劑', cat:'拋光', spec:'300ml', unit:'瓶', stock:5, safe:2, price:750, usePerCar:20},
  {id:5, name:'1號拋劑', cat:'拋光', spec:'300ml', unit:'瓶', stock:5, safe:2, price:750, usePerCar:20},
  {id:6, name:'2號拋劑', cat:'拋光', spec:'300ml', unit:'瓶', stock:5, safe:2, price:750, usePerCar:20},
  {id:7, name:'3號拋劑', cat:'拋光', spec:'300ml', unit:'瓶', stock:5, safe:2, price:750, usePerCar:20},
  {id:8, name:'玻璃鍍膜', cat:'鍍膜', spec:'50ml', unit:'瓶', stock:10, safe:3, price:750, usePerCar:5},
  {id:9, name:'鍍膜磚', cat:'耗材', spec:'個', unit:'個', stock:50, safe:15, price:35, usePerCar:1},
  {id:10, name:'擦拭布', cat:'耗材', spec:'條', unit:'條', stock:100, safe:30, price:35, usePerCar:4}
];

const seed = {
  brands: eBrands,
  items: structuredClone(ALL_PRESET_ITEMS),
  coats: []
};

let d = JSON.parse(localStorage.getItem('COATING_SYS_V1')||'null')||structuredClone(seed);
d.brands = eBrands;

let confirmDelId = null;
let confirmDelCoatIndex = null;

const $=id=>document.getElementById(id), money=n=>'$'+Math.round(n||0).toLocaleString('zh-TW'), now=()=>new Date().toISOString().slice(0,10);
$('date').value=now();

if (typeof db !== 'undefined') {
  db.collection("coating_data").doc("main").onSnapshot((doc) => {
    if (doc.exists) {
      d = doc.data();
      render();
    }
  });
}

function syncData() {
  if (typeof db !== 'undefined') {
    db.collection("coating_data").doc("main").set(d);
  } else {
    localStorage.setItem('COATING_SYS_V1', JSON.stringify(d));
  }
  render();
}

function show(id){document.querySelectorAll('main.page').forEach(x=>x.classList.add('hide'));$(id).classList.remove('hide');document.querySelectorAll('.nav').forEach(x=>x.classList.toggle('active',x.dataset.p===id));render();scrollTo(0,0)}
function qty(n){$('amount').value=Math.max(1,(+$('amount').value||1)+n)}
function capacity(it){if(it.spec&&it.spec.includes('300'))return 300;if(it.spec&&it.spec.includes('50'))return 50;return 1}

function deductSelected(selectedCoatName, selectedPolishName, units){
  d.items.forEach((it) => {
    let isSelectedCoat = (it.name === selectedCoatName);
    let isSelectedPolish = (it.name === selectedPolishName);
    let isGeneralItem = (it.name === '玻璃鍍膜' || it.name === '鍍膜磚' || it.name === '擦拭布');

    if (isSelectedCoat || isSelectedPolish || isGeneralItem) {
      let u = (it.usePerCar || 0) * units;
      if (it.cat === '鍍膜' || it.cat === '拋光') {
        it.stock = Math.max(0, it.stock - (u / capacity(it)));
      } else {
        it.stock = Math.max(0, it.stock - u);
      }
    }
  });
}

function saveCoat(){
  let modelVal = $('model').value.trim() || '通用車型';
  let colorVal = $('color').value.trim() || '未指定車色';
  let qtyNum = +$('amount').value || 1;
  let coatItem = $('coatSelect').value;
  let polishItem = $('polishSelect').value;

  let perCarCost = (coatItem === '無' && polishItem === '無') ? 0 : FIXED_COST_PER_CAR;

  let c = {
    id: Date.now(), 
    date: $('date').value||now(), 
    brand: $('brand').value, 
    model: modelVal, 
    color: colorVal, 
    plate: $('plate').value||'—', 
    coatItem: coatItem,
    polishItem: polishItem,
    qty: qtyNum, 
    cost: perCarCost * qtyNum
  };

  deductSelected(coatItem, polishItem, qtyNum);
  d.coats.unshift(c);
  syncData();

  $('model').value='';$('color').value='';$('plate').value='';$('amount').value=1;
  show('home');
}

function deleteCoat(index){
  if(confirmDelCoatIndex === index){
    d.coats.splice(index, 1);
    confirmDelCoatIndex = null;
    syncData();
  } else {
    confirmDelCoatIndex = index;
    render();
    setTimeout(()=>{ if(confirmDelCoatIndex === index){ confirmDelCoatIndex = null; render(); } }, 3000);
  }
}

function toggleCustomStockName(){
  let val = $('addNameSelect').value;
  if(val === '__CUSTOM__'){
    $('customNameField').classList.remove('hide');
  } else {
    $('customNameField').classList.add('hide');
    let item = d.items.find(x => x.name === val) || ALL_PRESET_ITEMS.find(x => x.name === val);
    if(item){
      $('addCat').value = item.cat;
      $('addUnit').value = item.unit;
      $('addSafe').value = item.safe;
      $('addPrice').value = item.price;
    }
  }
}

function addNewStock(){
  let selVal = $('addNameSelect').value;
  let name = selVal === '__CUSTOM__' ? $('addCustomName').value.trim() : selVal;
  let cat = $('addCat').value;
  let unit = $('addUnit').value || '個';
  let stockNum = +$('addStock').value || 0;
  let safe = +$('addSafe').value || 0;
  let price = +$('addPrice').value || 0;

  if(!name) return;

  let existing = d.items.find(x => x.name === name);
  if(existing){
    existing.stock += stockNum;
    existing.cat = cat;
    existing.unit = unit;
    existing.safe = safe;
    existing.price = price;
  } else {
    let preset = ALL_PRESET_ITEMS.find(x => x.name === name);
    let usePerCar = preset ? preset.usePerCar : 0;
    let spec = preset ? preset.spec : '';
    d.items.push({id: Date.now(), name, cat, spec, unit, stock: stockNum, safe, price, usePerCar});
  }

  $('addCustomName').value = '';
  syncData();
}

function adjustStock(id, amount){
  let item = d.items.find(x=>x.id===id);
  if(item){ item.stock = Math.max(0, item.stock + amount); syncData(); }
}

function deleteStock(id){
  if(confirmDelId === id){
    d.items = d.items.filter(x=>x.id!==id);
    confirmDelId = null;
    syncData();
  } else {
    confirmDelId = id;
    renderStock();
    setTimeout(()=>{ if(confirmDelId === id){ confirmDelId = null; renderStock(); } }, 3000);
  }
}

function renderStock(){
  $('stockList').innerHTML=d.items.map(x=>{
    let isDel = confirmDelId === x.id;
    return `
    <div class="stock-item">
      <div style="display:flex;justify-content:space-between;align-items:center;">
        <div><b>${x.name}</b> <small style="color:var(--muted)">(${x.cat} / ${x.spec})</small></div>
        <span class="pill ${x.stock<=0?'danger':x.stock<=x.safe?'warn':''}">${x.stock<=0?'缺貨':x.stock<=x.safe?'補貨':'正常'}</span>
      </div>
      <div style="font-size:13px;color:#aaa;display:flex;justify-content:space-between;">
        <span>庫存: <b style="color:#fff">${x.stock.toFixed(2)} ${x.unit}</b> (安全:${x.safe})</span>
        <span class="price">$${x.price}/${x.unit}</span>
      </div>
      <div class="stock-ctrls">
        <button onclick="adjustStock(${x.id}, -1)">-1</button>
        <button onclick="adjustStock(${x.id}, 1)">+1</button>
        <button onclick="adjustStock(${x.id}, 5)">+5</button>
        <button style="margin-left:auto;background:${isDel?'#ffffff':'#222222'};color:${isDel?'#000000':'#ffffff'};border:1px solid ${isDel?'#ffffff':'#555555'}" onclick="deleteStock(${x.id})">
          ${isDel ? '確認刪除' : '刪除'}
        </button>
      </div>
    </div>
  `}).join('')||'<div class="empty">無耗材資料</div>';
}

function renderBrandAnalysis(){
  let m=now().slice(0,7), mc=d.coats.filter(x=>x.date.startsWith(m)), stats={};
  mc.forEach(x=>{ stats[x.brand] = (stats[x.brand]||0) + x.qty; });
  $('brandAnalysis').innerHTML = Object.keys(stats).map(b => `<div class="row"><span>${b}</span><b>${stats[b]} 台</b></div>`).join('') || '<div class="empty">本月無資料</div>';
}

function resetData(){ d=structuredClone(seed); syncData(); }

function renderSelects(){
  $('brand').innerHTML = d.brands.map(b => `<option value="${b}">${b}</option>`).join('');
  
  let coatOptions = d.items.filter(x => x.cat === '鍍膜' && x.name !== '玻璃鍍膜').map(x => `<option value="${x.name}">${x.name}</option>`).join('');
  $('coatSelect').innerHTML = `<option value="無">不使用漆面鍍膜</option>` + coatOptions;
  
  let polishOptions = d.items.filter(x => x.cat === '拋光').map(x => `<option value="${x.name}">${x.name}</option>`).join('');
  $('polishSelect').innerHTML = `<option value="無">不使用拋光劑</option>` + polishOptions;

  let presetNames = ALL_PRESET_ITEMS.map(x => x.name);
  let customNames = d.items.map(x => x.name).filter(n => !presetNames.includes(n));
  let allOptions = [...presetNames, ...customNames];

  $('addNameSelect').innerHTML = allOptions.map(n => `<option value="${n}">${n}</option>`).join('') + `<option value="__CUSTOM__">＋ 自訂全新耗材名稱</option>`;
  toggleCustomStockName();
}

function render(){
 renderSelects();
 let m=now().slice(0,7),mc=d.coats.filter(x=>x.date.startsWith(m)),tc=d.coats.filter(x=>x.date===now()),count=mc.reduce((s,x)=>s+x.qty,0),today=tc.reduce((s,x)=>s+x.qty,0),cost=mc.reduce((s,x)=>s+x.cost,0),low=d.items.filter(x=>x.stock<=x.safe);
 $('today').textContent=`${today} 台`;$('month').textContent=count;$('mCost').textContent=money(cost);$('stockVal').textContent=money(d.items.reduce((s,x)=>s+x.stock*x.price,0));$('low').textContent=low.length+' 項';$('avg').textContent=money(count?cost/count:0);
 $('homeLow').innerHTML=low.length?low.map(x=>`<div class="row"><span>${x.name} (剩 ${x.stock.toFixed(2)}${x.unit})</span><span class="pill ${x.stock<=0?'danger':'warn'}">${x.stock<=0?'缺貨':'補貨'}</span></div>`).join(''):'<div class="empty">庫存正常</div>';
 
 $('homeRecent').innerHTML=d.coats.slice(0,10).map((x, i)=>{
   let isDel = confirmDelCoatIndex === i;
   let detailText = [x.coatItem !== '無' ? x.coatItem : '', x.polishItem !== '無' ? x.polishItem : ''].filter(Boolean).join(' + ') || '基礎施工';
   return `
   <div class="row">
     <div>
       <b>${x.brand} ${x.model} <small>(${x.color})</small></b>
       <small>${x.date}｜${x.plate}｜<span style="color:#ffffff">${detailText}</span></small>
     </div>
     <div style="display:flex;align-items:center;gap:10px;">
       <b>${x.qty} 台 ($${x.cost})</b>
       <button style="background:${isDel?'#ffffff':'#1a1a1a'};color:${isDel?'#000000':'#ffffff'};border:1px solid ${isDel?'#ffffff':'#444444'};padding:4px 8px;border-radius:6px;font-size:12px;cursor:pointer;" onclick="deleteCoat(${i})">
         ${isDel ? '確認刪除' : '刪除'}
       </button>
     </div>
   </div>
 `}).join('')||'<div class="empty">無紀錄</div>';
 
 $('rcount').textContent=count+' 台';$('rcost').textContent=money(cost);
 renderStock();
 renderBrandAnalysis();
}
render();
</script>
</body>
</html>
