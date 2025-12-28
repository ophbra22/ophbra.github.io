# ophbra.github.io
<!doctype html>
<html lang="he" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>SunVibe | משקפי שמש</title>
  <style>
    :root{
      --bg:#0b0f14; --card:#121824; --muted:#9fb0c5; --text:#e8f0ff;
      --brand:#49d0ff; --brand2:#7c5cff; --ok:#35d07f; --danger:#ff4d6d;
      --border:rgba(255,255,255,.08);
      --shadow: 0 12px 30px rgba(0,0,0,.35);
      --radius:18px;
    }
    *{box-sizing:border-box}
    body{
      margin:0; font-family: system-ui, -apple-system, Segoe UI, Arial;
      background: radial-gradient(1200px 600px at 80% -10%, rgba(124,92,255,.25), transparent 60%),
                  radial-gradient(1000px 600px at 20% 0%, rgba(73,208,255,.20), transparent 55%),
                  var(--bg);
      color:var(--text);
    }
    a{color:inherit; text-decoration:none}
    .container{max-width:1100px; margin:0 auto; padding:24px;}
    header{
      position:sticky; top:0; z-index:10;
      background: rgba(11,15,20,.78);
      backdrop-filter: blur(10px);
      border-bottom:1px solid var(--border);
    }
    .topbar{display:flex; align-items:center; gap:16px; padding:14px 24px;}
    .logo{
      display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.2px;
    }
    .mark{
      width:34px; height:34px; border-radius:12px;
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      display:grid; place-items:center; box-shadow: var(--shadow);
      font-weight:900;
    }
    .grow{flex:1}
    .search{
      flex:1; min-width:240px;
      display:flex; align-items:center; gap:10px;
      background: rgba(255,255,255,.05);
      border:1px solid var(--border);
      border-radius: 999px;
      padding:10px 14px;
    }
    .search input{
      width:100%; border:0; outline:0; background:transparent; color:var(--text);
      font-size:14px;
    }
    .pill{
      display:inline-flex; align-items:center; gap:10px;
      padding:10px 14px; border-radius:999px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      cursor:pointer;
    }
    .pill:hover{border-color: rgba(255,255,255,.18)}
    .badge{
      min-width:22px; height:22px; padding:0 7px;
      border-radius:999px; display:inline-grid; place-items:center;
      font-size:12px; font-weight:700;
      background: rgba(73,208,255,.16);
      border:1px solid rgba(73,208,255,.35);
      color: #cfefff;
    }

    .hero{
      margin-top:18px;
      border:1px solid var(--border);
      background: linear-gradient(135deg, rgba(73,208,255,.14), rgba(124,92,255,.12));
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
    }
    .hero-inner{display:grid; grid-template-columns: 1.2fr .8fr; gap:18px; padding:26px;}
    .hero h1{margin:0 0 10px; font-size:36px; line-height:1.1}
    .hero p{margin:0 0 16px; color:var(--muted); max-width:56ch}
    .cta-row{display:flex; gap:12px; flex-wrap:wrap}
    .btn{
      border:0; cursor:pointer;
      padding:12px 16px; border-radius: 14px;
      font-weight:800; letter-spacing:.2px;
      display:inline-flex; align-items:center; gap:10px;
    }
    .btn.primary{
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      color:#071018;
      box-shadow: 0 14px 30px rgba(73,208,255,.18);
    }
    .btn.ghost{
      background: rgba(255,255,255,.06);
      color:var(--text);
      border:1px solid var(--border);
    }
    .hero-card{
      border:1px solid var(--border);
      background: rgba(18,24,36,.7);
      border-radius: var(--radius);
      padding:16px;
      display:flex; flex-direction:column; gap:10px;
    }
    .stat{
      display:flex; justify-content:space-between; align-items:center;
      padding:10px 12px;
      border-radius: 14px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      color:var(--muted);
      font-size:14px;
    }
    .stat b{color:var(--text)}
    .toolbar{
      display:flex; align-items:center; gap:10px; flex-wrap:wrap;
      margin:22px 0 12px;
    }
    select{
      background: rgba(255,255,255,.05);
      border:1px solid var(--border);
      color:var(--text);
      padding:10px 12px;
      border-radius: 14px;
      outline:none;
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap:14px;
    }
    .card{
      grid-column: span 4;
      border:1px solid var(--border);
      background: rgba(18,24,36,.72);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
      display:flex; flex-direction:column;
      min-height: 360px;
    }
    .img{
      height:170px;
      background: radial-gradient(240px 140px at 20% 30%, rgba(73,208,255,.22), transparent 55%),
                  radial-gradient(240px 140px at 80% 50%, rgba(124,92,255,.20), transparent 55%),
                  rgba(255,255,255,.03);
      border-bottom:1px solid var(--border);
      display:grid; place-items:center;
      position:relative;
    }
    .img span{
      font-weight:900; letter-spacing:.3px;
      color: rgba(232,240,255,.85);
      padding:10px 12px;
      border-radius: 14px;
      border:1px dashed rgba(255,255,255,.16);
      background: rgba(0,0,0,.15);
    }
    .tag{
      position:absolute; top:12px; right:12px;
      padding:7px 10px; border-radius:999px;
      font-size:12px; font-weight:800;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(0,0,0,.2);
      color: #dbe7ff;
    }
    .content{padding:14px 14px 16px; display:flex; flex-direction:column; gap:10px; flex:1}
    .title{display:flex; justify-content:space-between; gap:10px; align-items:flex-start}
    .title h3{margin:0; font-size:16px}
    .title small{color:var(--muted)}
    .price{font-size:18px; font-weight:900}
    .row{display:flex; gap:10px; align-items:center; justify-content:space-between}
    .muted{color:var(--muted); font-size:13px; line-height:1.4}
    .chip{
      font-size:12px; font-weight:800;
      padding:6px 10px; border-radius:999px;
      border:1px solid rgba(73,208,255,.28);
      background: rgba(73,208,255,.12);
      color:#d7f4ff;
      display:inline-flex; gap:8px; align-items:center;
      width:fit-content;
    }
    .add{
      margin-top:auto;
      display:flex; gap:10px;
    }
    .qty{
      display:flex; align-items:center; gap:6px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      border-radius: 14px;
      padding:8px 10px;
    }
    .qty button{
      border:0; background:transparent; color:var(--text); cursor:pointer;
      font-size:16px; width:26px; height:26px; border-radius:10px;
    }
    .qty button:hover{background: rgba(255,255,255,.06)}
    .qty span{min-width:18px; text-align:center; font-weight:900}
    .add button.buy{
      flex:1;
      border:0; cursor:pointer;
      background: linear-gradient(135deg, rgba(73,208,255,.95), rgba(124,92,255,.92));
      color:#071018; font-weight:900;
      border-radius: 14px;
      padding:10px 12px;
    }
    .add button.buy:hover{filter:brightness(1.05)}
    .add button.wish{
      width:46px;
      border-radius: 14px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.05);
      color:var(--text);
      cursor:pointer;
    }
    .add button.wish:hover{border-color: rgba(255,255,255,.18)}

    /* Cart drawer */
    .drawer{
      position:fixed; inset:0; display:none;
      background: rgba(0,0,0,.45);
      z-index:100;
    }
    .drawer.open{display:block}
    .panel{
      position:absolute; left:0; top:0; height:100%; width:min(440px, 92vw);
      background: rgba(12,16,22,.92);
      border-right:1px solid var(--border);
      backdrop-filter: blur(12px);
      box-shadow: var(--shadow);
      display:flex; flex-direction:column;
    }
    .panel header{
      position:static;
      background: transparent;
      border-bottom:1px solid var(--border);
    }
    .panel .head{
      display:flex; align-items:center; justify-content:space-between;
      padding:16px 16px;
    }
    .panel h2{margin:0; font-size:18px}
    .close{
      border:1px solid var(--border);
      background: rgba(255,255,255,.05);
      color:var(--text);
      border-radius: 14px;
      padding:10px 12px;
      cursor:pointer;
    }
    .close:hover{border-color: rgba(255,255,255,.18)}
    .cart-list{padding:14px 16px; overflow:auto; flex:1; display:flex; flex-direction:column; gap:10px}
    .cart-item{
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      border-radius: 16px;
      padding:12px;
      display:flex; gap:10px; align-items:flex-start;
    }
    .thumb{
      width:64px; height:64px; border-radius: 16px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      display:grid; place-items:center;
      font-weight:900;
    }
    .cart-item h4{margin:0 0 4px; font-size:14px}
    .cart-item small{color:var(--muted)}
    .cart-item .right{
      margin-right:auto;
      display:flex; flex-direction:column; gap:8px; align-items:flex-start;
    }
    .cart-item .actions{
      display:flex; gap:8px; align-items:center; flex-wrap:wrap;
    }
    .mini{
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      color:var(--text);
      border-radius: 12px;
      padding:8px 10px;
      cursor:pointer;
      font-weight:800;
      font-size:12px;
    }
    .mini:hover{border-color: rgba(255,255,255,.18)}
    .mini.danger{border-color: rgba(255,77,109,.35); background: rgba(255,77,109,.12)}
    .summary{
      border-top:1px solid var(--border);
      padding:14px 16px 16px;
      display:flex; flex-direction:column; gap:10px;
    }
    .summary .line{display:flex; justify-content:space-between; color:var(--muted)}
    .summary .line b{color:var(--text)}
    .checkout{
      border:0; cursor:pointer;
      background: linear-gradient(135deg, var(--ok), rgba(73,208,255,.9));
      color:#06140e;
      font-weight:950;
      border-radius: 16px;
      padding:12px 14px;
    }
    .checkout:hover{filter:brightness(1.05)}
    .empty{
      color:var(--muted);
      border:1px dashed rgba(255,255,255,.16);
      border-radius: 16px;
      padding:14px;
      text-align:center;
    }

    /* Checkout modal (demo) */
    .modal{position:fixed; inset:0; display:none; place-items:center; z-index:200; background: rgba(0,0,0,.55)}
    .modal.open{display:grid}
    .modal .box{
      width:min(560px, 92vw);
      border-radius: 22px;
      border:1px solid var(--border);
      background: rgba(18,24,36,.92);
      box-shadow: var(--shadow);
      padding:18px;
    }
    .box h3{margin:0 0 6px}
    .box p{margin:0 0 14px; color:var(--muted)}
    .form{
      display:grid; grid-template-columns: 1fr 1fr; gap:10px;
    }
    .field{display:flex; flex-direction:column; gap:6px}
    .field label{font-size:12px; color:var(--muted)}
    .field input, .field textarea{
      border:1px solid var(--border);
      background: rgba(255,255,255,.05);
      border-radius: 14px;
      padding:10px 12px;
      color:var(--text);
      outline:none;
    }
    .field textarea{grid-column: span 2; min-height:86px; resize:vertical}
    .full{grid-column: span 2}
    .actions-row{display:flex; gap:10px; justify-content:flex-end; margin-top:12px}
    .btn2{
      border-radius: 14px; padding:10px 12px; cursor:pointer;
      border:1px solid var(--border);
      background: rgba(255,255,255,.06);
      color:var(--text);
      font-weight:900;
    }
    .btn2.primary{border:0; background: linear-gradient(135deg, var(--brand), var(--brand2)); color:#071018}
    footer{color:var(--muted); text-align:center; padding:22px 0 34px}

    @media (max-width: 900px){
      .card{grid-column: span 6}
      .hero-inner{grid-template-columns: 1fr}
      .search{display:none}
    }
    @media (max-width: 560px){
      .card{grid-column: span 12}
      .form{grid-template-columns: 1fr}
      .field textarea, .full{grid-column: span 1}
    }
  </style>
</head>
<body>
  <header>
    <div class="topbar">
      <div class="logo">
        <div class="mark">SV</div>
        <div>
          <div style="font-size:15px">SunVibe</div>
          <div style="font-size:12px;color:var(--muted);font-weight:600">משקפי שמש פרימיום</div>
        </div>
      </div>

      <div class="search grow" title="חפש מוצר">
        🔎 <input id="q" placeholder="חפש: פולארויד, טייסים, ספייס..." />
      </div>

      <button class="pill" id="openCart" aria-label="פתח עגלה">
        🛒 עגלה <span class="badge" id="cartCount">0</span>
      </button>
    </div>
  </header>

  <div class="container">
    <section class="hero">
      <div class="hero-inner">
        <div>
          <h1>משקפי שמש שנראים 🔥 ומרגישים יוקרתיים</h1>
          <p>
            בחר דגם, הוסף לעגלה, וסיים הזמנה בדמו.
            אפשר להחליף את המוצרים, מחירים ותמונות אחר כך — זה שלד מושלם לחנות.
          </p>
          <div class="cta-row">
            <button class="btn primary" onclick="document.getElementById('shop').scrollIntoView({behavior:'smooth'})">
              🕶️ לעמוד החנות
            </button>
            <button class="btn ghost" onclick="openCart()">
              🛒 לצפות בעגלה
            </button>
          </div>
        </div>

        <div class="hero-card">
          <div class="stat"><span>משלוח</span> <b>חינם מעל ₪299</b></div>
          <div class="stat"><span>אחריות</span> <b>12 חודשים</b></div>
          <div class="stat"><span>החזרות</span> <b>עד 14 יום</b></div>
          <div class="stat"><span>עדשות</span> <b>UV400 + אופציה לפולארויד</b></div>
        </div>
      </div>
    </section>

    <div class="toolbar" id="shop">
      <select id="filterType">
        <option value="all">כל הסוגים</option>
        <option value="aviator">טייסים</option>
        <option value="sport">ספורט</option>
        <option value="classic">קלאסי</option>
        <option value="fashion">פאשן</option>
      </select>

      <select id="filterLens">
        <option value="all">כל העדשות</option>
        <option value="polarized">פולארויד</option>
        <option value="uv400">UV400</option>
      </select>

      <select id="sort">
        <option value="popular">מומלצים</option>
        <option value="priceAsc">מחיר: נמוך לגבוה</option>
        <option value="priceDesc">מחיר: גבוה לנמוך</option>
        <option value="name">שם</option>
      </select>

      <button class="pill" onclick="resetFilters()">איפוס</button>
      <div class="grow"></div>
      <div style="color:var(--muted);font-size:13px">טיפ: לחץ על “♥” לשמירה (דמו)</div>
    </div>

    <section class="grid" id="grid"></section>

    <footer>© <span id="year"></span> SunVibe — אתר דמו למכירת משקפי שמש</footer>
  </div>

  <!-- Cart Drawer -->
  <div class="drawer" id="drawer" role="dialog" aria-modal="true" aria-label="עגלה">
    <div class="panel" onclick="event.stopPropagation()">
      <header>
        <div class="head">
          <h2>🛒 העגלה שלך</h2>
          <button class="close" onclick="closeCart()">סגור ✕</button>
        </div>
      </header>

      <div class="cart-list" id="cartList"></div>

      <div class="summary">
        <div class="line"><span>סכום ביניים</span><b id="subTotal">₪0</b></div>
        <div class="line"><span>משלוח</span><b id="shipping">₪0</b></div>
        <div class="line"><span>סה״כ</span><b id="total">₪0</b></div>
        <button class="checkout" onclick="openCheckout()">לתשלום (דמו) ✅</button>
        <div style="color:var(--muted);font-size:12px">* אין סליקה אמיתית, רק הדמיה</div>
      </div>
    </div>
  </div>

  <!-- Checkout Modal -->
  <div class="modal" id="checkoutModal" role="dialog" aria-modal="true" aria-label="תשלום">
    <div class="box" onclick="event.stopPropagation()">
      <h3>סיום הזמנה (דמו)</h3>
      <p>הזן פרטים — ונציג הודעת “הזמנה התקבלה”.</p>

      <form id="checkoutForm" class="form">
        <div class="field">
          <label>שם מלא</label>
          <input required name="name" placeholder="אופיר ברודה" />
        </div>
        <div class="field">
          <label>טלפון</label>
          <input required name="phone" placeholder="05X-XXXXXXX" />
        </div>
        <div class="field full">
          <label>אימייל</label>
          <input required type="email" name="email" placeholder="name@email.com" />
        </div>
        <div class="field full">
          <label>כתובת למשלוח</label>
          <input required name="address" placeholder="רחוב, מספר, עיר" />
        </div>
        <div class="field">
          <label>הערות</label>
          <input name="note" placeholder="לדוגמה: קומה 3" />
        </div>
        <div class="field">
          <label>שיטת משלוח</label>
          <input name="ship" value="שליח עד הבית" disabled />
        </div>
        <div class="field full">
          <label>סיכום הזמנה</label>
          <textarea id="orderSummary" readonly></textarea>
        </div>

        <div class="actions-row full">
          <button type="button" class="btn2" onclick="closeCheckout()">ביטול</button>
          <button type="submit" class="btn2 primary">אישור הזמנה</button>
        </div>
      </form>
    </div>
  </div>

  <script>
    // ---------- Data ----------
    const products = [
      { id:"sv-aviator-black", name:"Aviator Noir", type:"aviator", lens:"polarized", price:249, rating:4.8, badge:"פולארויד", desc:"דגם טייסים קלאסי עם עדשה פולארויד ומסגרת מתכת." },
      { id:"sv-classic-tortoise", name:"Classic Tortoise", type:"classic", lens:"uv400", price:189, rating:4.6, badge:"UV400", desc:"מראה וינטג׳ עם מסגרת טורטויס ועדשות UV400." },
      { id:"sv-sport-stealth", name:"Sport Stealth", type:"sport", lens:"polarized", price:299, rating:4.7, badge:"ספורט", desc:"נוחות גבוהה, אחיזה טובה, עדשות פולארויד לפעילות בחוץ." },
      { id:"sv-fashion-ice", name:"Fashion Ice", type:"fashion", lens:"uv400", price:219, rating:4.5, badge:"פאשן", desc:"לוק מודרני עם עדשות בהירות (UV400) למסגרת קלה." },
      { id:"sv-aviator-gold", name:"Aviator Gold", type:"aviator", lens:"uv400", price:229, rating:4.6, badge:"חדש", desc:"מסגרת זהב עדינה, עדשות UV400, סגנון נקי." },
      { id:"sv-classic-matte", name:"Classic Matte", type:"classic", lens:"polarized", price:279, rating:4.9, badge:"בסט סלר", desc:"מסגרת מט, עדשות פולארויד — חדות מעולה באור חזק." },
    ];

    // Cart: { [id]: {qty} }
    const cart = JSON.parse(localStorage.getItem("sv_cart") || "{}");
    const wishlist = JSON.parse(localStorage.getItem("sv_wish") || "{}");

    const els = {
      grid: document.getElementById("grid"),
      q: document.getElementById("q"),
      filterType: document.getElementById("filterType"),
      filterLens: document.getElementById("filterLens"),
      sort: document.getElementById("sort"),
      cartCount: document.getElementById("cartCount"),
      drawer: document.getElementById("drawer"),
      cartList: document.getElementById("cartList"),
      subTotal: document.getElementById("subTotal"),
      shipping: document.getElementById("shipping"),
      total: document.getElementById("total"),
      checkoutModal: document.getElementById("checkoutModal"),
      checkoutForm: document.getElementById("checkoutForm"),
      orderSummary: document.getElementById("orderSummary"),
    };

    document.getElementById("year").textContent = new Date().getFullYear();

    // ---------- Helpers ----------
    const fmtILS = n => "₪" + n.toLocaleString("he-IL");
    const getProduct = id => products.find(p => p.id === id);

    function save(){
      localStorage.setItem("sv_cart", JSON.stringify(cart));
      localStorage.setItem("sv_wish", JSON.stringify(wishlist));
    }

    function cartQtyTotal(){
      return Object.values(cart).reduce((s, it) => s + it.qty, 0);
    }

    function calcTotals(){
      const subtotal = Object.entries(cart).reduce((sum, [id, it]) => {
        const p = getProduct(id);
        return sum + (p ? p.price * it.qty : 0);
      }, 0);
      const shipping = subtotal === 0 ? 0 : (subtotal >= 299 ? 0 : 29);
      const total = subtotal + shipping;
      return { subtotal, shipping, total };
    }

    function updateCartBadge(){
      els.cartCount.textContent = cartQtyTotal();
    }

    // ---------- Rendering ----------
    function render(){
      const q = (els.q?.value || "").trim().toLowerCase();
      const type = els.filterType.value;
      const lens = els.filterLens.value;
      const sort = els.sort.value;

      let list = [...products];

      if(q){
        list = list.filter(p => (p.name + " " + p.desc).toLowerCase().includes(q));
      }
      if(type !== "all"){
        list = list.filter(p => p.type === type);
      }
      if(lens !== "all"){
        list = list.filter(p => p.lens === lens);
      }

      if(sort === "priceAsc") list.sort((a,b)=>a.price-b.price);
      if(sort === "priceDesc") list.sort((a,b)=>b.price-a.price);
      if(sort === "name") list.sort((a,b)=>a.name.localeCompare(b.name));
      if(sort === "popular") list.sort((a,b)=>b.rating-a.rating);

      els.grid.innerHTML = list.map(p => productCard(p)).join("");
      updateCartBadge();
    }

    function productCard(p){
      const inWish = !!wishlist[p.id];
      const currentQty = cart[p.id]?.qty || 0;

      const typeMap = { aviator:"טייסים", sport:"ספורט", classic:"קלאסי", fashion:"פאשן" };
      const lensMap = { polarized:"פולארויד", uv400:"UV400" };

      return `
        <article class="card">
          <div class="img">
            <div class="tag">${p.badge}</div>
            <span>🕶️ ${p.name}</span>
          </div>
          <div class="content">
            <div class="title">
              <div>
                <h3>${p.name}</h3>
                <small>${typeMap[p.type]} • ${lensMap[p.lens]} • ⭐ ${p.rating}</small>
              </div>
              <div class="price">${fmtILS(p.price)}</div>
            </div>
            <div class="muted">${p.desc}</div>
            <div class="row">
              <div class="chip">✅ משלוח מהיר</div>
              <div class="chip">🛡️ אחריות</div>
            </div>

            <div class="add">
              <div class="qty" aria-label="כמות">
                <button onclick="decQty('${p.id}')">−</button>
                <span id="qty-${p.id}">${currentQty}</span>
                <button onclick="incQty('${p.id}')">+</button>
              </div>

              <button class="buy" onclick="addToCart('${p.id}')">הוסף לעגלה</button>

              <button class="wish" title="שמירה" onclick="toggleWish('${p.id}')">
                ${inWish ? "💙" : "🤍"}
              </button>
            </div>
          </div>
        </article>
      `;
    }

    // ---------- Actions ----------
    function incQty(id){
      cart[id] = cart[id] || { qty:0 };
      cart[id].qty += 1;
      save(); render(); renderCart();
    }
    function decQty(id){
      if(!cart[id]) return;
      cart[id].qty -= 1;
      if(cart[id].qty <= 0) delete cart[id];
      save(); render(); renderCart();
    }
    function addToCart(id){
      cart[id] = cart[id] || { qty:0 };
      cart[id].qty += 1;
      save(); render(); renderCart();
      openCart();
    }
    function removeFromCart(id){
      delete cart[id];
      save(); render(); renderCart();
    }
    function toggleWish(id){
      if(wishlist[id]) delete wishlist[id];
      else wishlist[id] = true;
      save(); render();
    }

    function resetFilters(){
      els.filterType.value="all";
      els.filterLens.value="all";
      els.sort.value="popular";
      if(els.q) els.q.value="";
      render();
    }

    // ---------- Cart UI ----------
    function openCart(){
      els.drawer.classList.add("open");
      renderCart();
    }
    function closeCart(){
      els.drawer.classList.remove("open");
    }
    els.drawer.addEventListener("click", closeCart);

    function renderCart(){
      const entries = Object.entries(cart);

      if(entries.length === 0){
        els.cartList.innerHTML = `<div class="empty">העגלה ריקה. בחר משקפיים והוסף לעגלה 🕶️</div>`;
      } else {
        els.cartList.innerHTML = entries.map(([id, it]) => {
          const p = getProduct(id);
          if(!p) return "";
          return `
            <div class="cart-item">
              <div class="thumb">SV</div>
              <div class="right">
                <h4>${p.name}</h4>
                <small>${fmtILS(p.price)} ליחידה</small>

                <div class="actions">
                  <button class="mini" onclick="decQty('${id}')">−</button>
                  <span style="font-weight:900">כמות: ${it.qty}</span>
                  <button class="mini" onclick="incQty('${id}')">+</button>
                  <button class="mini danger" onclick="removeFromCart('${id}')">הסר</button>
                </div>
              </div>
              <div style="font-weight:950">${fmtILS(p.price * it.qty)}</div>
            </div>
          `;
        }).join("");
      }

      const {subtotal, shipping, total} = calcTotals();
      els.subTotal.textContent = fmtILS(subtotal);
      els.shipping.textContent = fmtILS(shipping);
      els.total.textContent = fmtILS(total);

      updateCartBadge();
    }

    // ---------- Checkout (demo) ----------
    function openCheckout(){
      const entries = Object.entries(cart);
      if(entries.length === 0){
        alert("העגלה ריקה 🙂");
        return;
      }
      const {subtotal, shipping, total} = calcTotals();
      const lines = entries.map(([id, it]) => {
        const p = getProduct(id);
        return `• ${p.name} × ${it.qty} = ${fmtILS(p.price * it.qty)}`;
      }).join("\n");
      els.orderSummary.value =
        `${lines}\n\nסכום ביניים: ${fmtILS(subtotal)}\nמשלוח: ${fmtILS(shipping)}\nסה״כ: ${fmtILS(total)}`;

      els.checkoutModal.classList.add("open");
    }
    function closeCheckout(){
      els.checkoutModal.classList.remove("open");
    }
    els.checkoutModal.addEventListener("click", closeCheckout);

    els.checkoutForm.addEventListener("submit", (e) => {
      e.preventDefault();
      const data = Object.fromEntries(new FormData(els.checkoutForm).entries());
      const { total } = calcTotals();

      // Demo success
      alert(`✅ תודה ${data.name}!\nהזמנתך התקבלה (דמו).\nחיוב מדומה: ${fmtILS(total)}\nניצור קשר ב-${data.phone}`);
      // clear cart
      for(const k of Object.keys(cart)) delete cart[k];
      save();
      closeCheckout();
      closeCart();
      render();
      renderCart();
      els.checkoutForm.reset();
    });

    // Search + filters
    ["input","change"].forEach(ev => {
      els.q?.addEventListener(ev, render);
      els.filterType.addEventListener(ev, render);
      els.filterLens.addEventListener(ev, render);
      els.sort.addEventListener(ev, render);
    });

    // Init
    render();
    renderCart();

    // Expose functions to inline onclick
    window.addToCart = addToCart;
    window.incQty = incQty;
    window.decQty = decQty;
    window.removeFromCart = removeFromCart;
    window.toggleWish = toggleWish;
    window.openCart = openCart;
    window.closeCart = closeCart;
    window.openCheckout = openCheckout;
    window.closeCheckout = closeCheckout;
    window.resetFilters = resetFilters;
  </script>
</body>
</html>
