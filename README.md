<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>JAI MATA DI MOBILE AGENCY</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Nunito:wght@400;500;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --red: #e63946;
    --gold: #f4a261;
    --dark: #0d0d0d;
    --dark2: #1a1a2e;
    --dark3: #16213e;
    --card: #1e2a45;
    --card2: #243050;
    --text: #f0f0f0;
    --muted: #8892a4;
    --border: rgba(255,255,255,0.08);
    --radius: 16px;
    --shadow: 0 8px 32px rgba(0,0,0,0.4);
  }
  *,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{font-family:'Nunito',sans-serif;background:var(--dark2);color:var(--text);min-height:100vh;overflow-x:hidden}

  /* ─── HEADER ─── */
  header{
    background:linear-gradient(135deg,#0d0d0d 0%,#1a1a2e 60%,#16213e 100%);
    border-bottom:2px solid var(--red);
    padding:0;
    position:sticky;top:0;z-index:100;
    box-shadow:0 4px 24px rgba(230,57,70,0.18);
  }
  .header-inner{
    max-width:900px;margin:0 auto;
    display:flex;align-items:center;justify-content:space-between;
    padding:12px 16px;gap:12px;
  }
  .logo-block{display:flex;align-items:center;gap:10px;text-decoration:none}
  .logo-icon{
    width:46px;height:46px;border-radius:12px;
    background:linear-gradient(135deg,var(--red),var(--gold));
    display:flex;align-items:center;justify-content:center;
    font-size:22px;flex-shrink:0;
    box-shadow:0 4px 14px rgba(230,57,70,0.4);
  }
  .logo-text .shop-name{
    font-family:'Rajdhani',sans-serif;
    font-size:1.15rem;font-weight:700;line-height:1.1;
    color:#fff;letter-spacing:0.5px;
  }
  .logo-text .tagline{font-size:0.65rem;color:var(--gold);font-weight:600;letter-spacing:1px;text-transform:uppercase}
  .header-cart-btn{
    background:linear-gradient(135deg,var(--red),#c1121f);
    border:none;border-radius:12px;
    padding:10px 16px;cursor:pointer;
    display:flex;align-items:center;gap:8px;
    color:#fff;font-family:'Nunito',sans-serif;font-weight:700;font-size:0.9rem;
    box-shadow:0 4px 14px rgba(230,57,70,0.35);
    transition:transform 0.18s,box-shadow 0.18s;flex-shrink:0;
  }
  .header-cart-btn:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(230,57,70,0.5)}
  .cart-count-badge{
    background:#fff;color:var(--red);
    border-radius:999px;min-width:22px;height:22px;
    display:flex;align-items:center;justify-content:center;
    font-size:0.78rem;font-weight:800;padding:0 5px;
  }

  /* ─── HERO STRIP ─── */
  .hero-strip{
    background:linear-gradient(90deg,#e63946 0%,#c1121f 50%,#9d0208 100%);
    padding:10px 16px;text-align:center;
    font-family:'Rajdhani',sans-serif;font-size:0.9rem;font-weight:600;
    letter-spacing:1.5px;color:#fff;
  }
  .hero-strip span{opacity:0.75;margin:0 8px}

  /* ─── MAIN ─── */
  main{max-width:900px;margin:0 auto;padding:20px 12px 120px}

  /* ─── CATEGORIES ─── */
  .section-label{
    font-family:'Rajdhani',sans-serif;font-size:0.72rem;font-weight:700;
    letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:10px;
  }
  .cat-filters{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:24px}
  .cat-btn{
    background:var(--card);border:1.5px solid var(--border);
    border-radius:999px;padding:7px 16px;cursor:pointer;
    font-family:'Nunito',sans-serif;font-weight:700;font-size:0.82rem;color:var(--muted);
    transition:all 0.2s;white-space:nowrap;
  }
  .cat-btn:hover{border-color:var(--gold);color:var(--gold)}
  .cat-btn.active{background:linear-gradient(135deg,var(--red),#c1121f);border-color:var(--red);color:#fff;box-shadow:0 4px 12px rgba(230,57,70,0.3)}

  /* ─── PRODUCT GRID ─── */
  .products-heading{
    font-family:'Rajdhani',sans-serif;font-size:1.4rem;font-weight:700;
    margin-bottom:16px;color:#fff;display:flex;align-items:center;gap:10px;
  }
  .products-heading::after{content:'';flex:1;height:2px;background:linear-gradient(90deg,var(--red),transparent)}
  .product-grid{
    display:grid;
    grid-template-columns:repeat(auto-fill,minmax(160px,1fr));
    gap:14px;
  }
  .product-card{
    background:var(--card);border:1.5px solid var(--border);border-radius:var(--radius);
    overflow:hidden;display:flex;flex-direction:column;
    transition:transform 0.22s,box-shadow 0.22s,border-color 0.22s;
    position:relative;
  }
  .product-card:hover{transform:translateY(-5px);box-shadow:0 12px 32px rgba(0,0,0,0.4);border-color:rgba(230,57,70,0.4)}
  .product-card.hidden{display:none}
  .badge{
    position:absolute;top:8px;left:8px;z-index:2;
    background:linear-gradient(135deg,var(--red),#c1121f);color:#fff;
    font-size:0.62rem;font-weight:800;letter-spacing:0.8px;text-transform:uppercase;
    padding:3px 8px;border-radius:999px;box-shadow:0 2px 8px rgba(230,57,70,0.4);
  }
  .product-img-wrap{
    width:100%;aspect-ratio:1/1;overflow:hidden;background:#11182a;
    display:flex;align-items:center;justify-content:center;
  }
  .product-img-wrap img{
    width:100%;height:100%;object-fit:cover;
    transition:transform 0.35s;
  }
  .product-card:hover .product-img-wrap img{transform:scale(1.07)}
  .product-info{padding:10px 10px 12px;flex:1;display:flex;flex-direction:column;gap:4px}
  .product-cat{font-size:0.62rem;color:var(--gold);font-weight:700;text-transform:uppercase;letter-spacing:1px}
  .product-name{font-size:0.82rem;font-weight:700;color:#fff;line-height:1.3;flex:1}
  .product-price{font-family:'Rajdhani',sans-serif;font-size:1.15rem;font-weight:700;color:var(--red)}
  .add-btn{
    margin:0 10px 10px;padding:9px 0;border:none;border-radius:10px;cursor:pointer;
    background:linear-gradient(135deg,var(--red),#c1121f);color:#fff;
    font-family:'Nunito',sans-serif;font-weight:800;font-size:0.82rem;
    transition:all 0.2s;box-shadow:0 3px 10px rgba(230,57,70,0.3);
    display:flex;align-items:center;justify-content:center;gap:6px;
  }
  .add-btn:hover{transform:translateY(-1px);box-shadow:0 5px 16px rgba(230,57,70,0.5)}
  .add-btn:active{transform:scale(0.97)}
  .add-btn.added{background:linear-gradient(135deg,#2dc653,#1a9e3f)}

  /* ─── FLOATING BUTTONS ─── */
  .fab-group{position:fixed;bottom:22px;right:16px;display:flex;flex-direction:column;gap:10px;z-index:200}
  .fab{
    width:52px;height:52px;border-radius:50%;border:none;cursor:pointer;
    display:flex;align-items:center;justify-content:center;font-size:22px;
    box-shadow:var(--shadow);transition:transform 0.18s,box-shadow 0.18s;
    position:relative;
  }
  .fab:hover{transform:scale(1.1);box-shadow:0 8px 24px rgba(0,0,0,0.5)}
  .fab-wa{background:linear-gradient(135deg,#25d366,#128c7e)}
  .fab-cart{background:linear-gradient(135deg,var(--red),#c1121f)}
  .fab-badge{
    position:absolute;top:-4px;right:-4px;
    background:#fff;color:var(--red);border-radius:999px;
    min-width:20px;height:20px;font-size:0.7rem;font-weight:800;
    display:flex;align-items:center;justify-content:center;padding:0 4px;
    border:2px solid var(--dark2);
  }

  /* ─── CART MODAL ─── */
  .overlay{
    position:fixed;inset:0;background:rgba(0,0,0,0.7);z-index:300;
    display:flex;align-items:flex-end;justify-content:center;
    opacity:0;pointer-events:none;transition:opacity 0.25s;
  }
  .overlay.open{opacity:1;pointer-events:all}
  .modal{
    background:var(--dark3);border-radius:24px 24px 0 0;
    width:100%;max-width:560px;max-height:90vh;
    display:flex;flex-direction:column;
    transform:translateY(100%);transition:transform 0.3s cubic-bezier(.4,0,.2,1);
    border-top:2px solid var(--red);
  }
  .overlay.open .modal{transform:translateY(0)}
  .modal-header{
    padding:18px 20px 14px;display:flex;align-items:center;justify-content:space-between;
    border-bottom:1.5px solid var(--border);
  }
  .modal-title{font-family:'Rajdhani',sans-serif;font-size:1.3rem;font-weight:700;color:#fff;display:flex;align-items:center;gap:8px}
  .close-btn{
    background:var(--card);border:1.5px solid var(--border);border-radius:8px;
    width:34px;height:34px;cursor:pointer;color:var(--muted);font-size:18px;
    display:flex;align-items:center;justify-content:center;transition:all 0.15s;
  }
  .close-btn:hover{background:var(--red);color:#fff;border-color:var(--red)}
  .modal-body{overflow-y:auto;flex:1;padding:12px 16px}
  .cart-empty{text-align:center;padding:50px 20px;color:var(--muted)}
  .cart-empty .empty-icon{font-size:52px;margin-bottom:12px}
  .cart-empty p{font-size:1rem;font-weight:600}
  .cart-item{
    display:flex;align-items:center;gap:12px;padding:12px 0;
    border-bottom:1.5px solid var(--border);
  }
  .cart-item-img{width:56px;height:56px;border-radius:10px;object-fit:cover;background:#11182a;flex-shrink:0}
  .cart-item-info{flex:1;min-width:0}
  .cart-item-name{font-weight:700;font-size:0.85rem;color:#fff;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
  .cart-item-sub{font-size:0.75rem;color:var(--muted);margin-top:2px}
  .cart-item-price{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:700;color:var(--gold);margin-top:3px}
  .qty-controls{display:flex;align-items:center;gap:6px;margin-top:4px}
  .qty-btn{
    background:var(--card2);border:1.5px solid var(--border);border-radius:7px;
    width:28px;height:28px;cursor:pointer;color:#fff;font-size:15px;font-weight:700;
    display:flex;align-items:center;justify-content:center;transition:all 0.15s;
  }
  .qty-btn:hover{background:var(--red);border-color:var(--red)}
  .qty-display{font-weight:800;font-size:0.9rem;min-width:22px;text-align:center}
  .remove-btn{
    background:transparent;border:1.5px solid rgba(230,57,70,0.3);
    border-radius:8px;padding:6px 10px;cursor:pointer;color:var(--red);
    font-size:0.72rem;font-weight:700;transition:all 0.15s;flex-shrink:0;
  }
  .remove-btn:hover{background:var(--red);color:#fff}
  .modal-footer{padding:14px 16px;border-top:1.5px solid var(--border)}
  .total-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px}
  .total-label{font-family:'Rajdhani',sans-serif;font-size:1rem;font-weight:700;color:var(--muted);letter-spacing:1px}
  .total-amount{font-family:'Rajdhani',sans-serif;font-size:1.5rem;font-weight:700;color:var(--gold)}
  .checkout-btn{
    width:100%;padding:14px;border:none;border-radius:12px;cursor:pointer;
    background:linear-gradient(135deg,var(--red),#c1121f);color:#fff;
    font-family:'Nunito',sans-serif;font-weight:800;font-size:1rem;
    transition:all 0.2s;box-shadow:0 4px 16px rgba(230,57,70,0.4);
  }
  .checkout-btn:hover{transform:translateY(-2px);box-shadow:0 6px 22px rgba(230,57,70,0.55)}
  .checkout-btn:disabled{opacity:0.5;cursor:not-allowed;transform:none}

  /* ─── CHECKOUT MODAL ─── */
  #checkoutOverlay .modal{border-top-color:var(--gold)}
  .form-group{margin-bottom:14px}
  .form-group label{
    display:block;font-weight:700;font-size:0.82rem;color:var(--muted);
    margin-bottom:6px;letter-spacing:0.5px;text-transform:uppercase;
  }
  .form-group input,.form-group textarea{
    width:100%;background:var(--card);border:1.5px solid var(--border);
    border-radius:10px;padding:11px 14px;color:#fff;
    font-family:'Nunito',sans-serif;font-size:0.9rem;
    transition:border-color 0.2s;outline:none;
  }
  .form-group input:focus,.form-group textarea:focus{border-color:var(--red)}
  .form-group textarea{resize:vertical;min-height:80px}
  .order-summary-box{
    background:var(--card);border:1.5px solid var(--border);border-radius:12px;
    padding:12px;margin-bottom:16px;font-size:0.82rem;
  }
  .order-summary-box .summary-title{font-weight:800;color:var(--gold);margin-bottom:8px;font-size:0.85rem}
  .order-summary-box .summary-item{display:flex;justify-content:space-between;padding:4px 0;color:var(--muted)}
  .order-summary-box .summary-item span:last-child{color:#fff;font-weight:700}
  .order-summary-box .summary-total{border-top:1.5px solid var(--border);margin-top:6px;padding-top:8px;display:flex;justify-content:space-between}
  .order-summary-box .summary-total span:first-child{font-weight:700;color:var(--muted)}
  .order-summary-box .summary-total span:last-child{font-family:'Rajdhani',sans-serif;font-size:1.1rem;font-weight:700;color:var(--gold)}
  .submit-btn{
    width:100%;padding:14px;border:none;border-radius:12px;cursor:pointer;
    background:linear-gradient(135deg,var(--gold),#e76f51);color:#fff;
    font-family:'Nunito',sans-serif;font-weight:800;font-size:1rem;
    transition:all 0.2s;box-shadow:0 4px 16px rgba(244,162,97,0.4);
    display:flex;align-items:center;justify-content:center;gap:8px;
  }
  .submit-btn:hover{transform:translateY(-2px);box-shadow:0 6px 22px rgba(244,162,97,0.55)}
  .submit-btn:disabled{opacity:0.6;cursor:not-allowed;transform:none}

  /* ─── SUCCESS TOAST ─── */
  .toast{
    position:fixed;top:20px;left:50%;transform:translateX(-50%) translateY(-80px);
    background:linear-gradient(135deg,#2dc653,#1a9e3f);color:#fff;
    border-radius:14px;padding:16px 22px;z-index:500;
    font-weight:700;font-size:0.9rem;text-align:center;
    box-shadow:0 8px 24px rgba(0,0,0,0.4);
    transition:transform 0.4s cubic-bezier(.4,0,.2,1);
    max-width:90vw;min-width:260px;
  }
  .toast.show{transform:translateX(-50%) translateY(0)}
  .toast .wa-link{color:#b7f5c7;font-weight:800;text-decoration:none;display:block;margin-top:6px;font-size:0.85rem}

  /* ─── INFO STRIP ─── */
  .info-strip{
    background:var(--card);border:1.5px solid var(--border);border-radius:14px;
    padding:14px 16px;margin-bottom:22px;
    display:flex;flex-wrap:wrap;gap:12px;align-items:center;justify-content:space-between;
  }
  .info-item{display:flex;align-items:center;gap:7px;font-size:0.8rem;color:var(--muted)}
  .info-item strong{color:#fff;font-size:0.82rem}
  .info-dot{width:7px;height:7px;border-radius:50%;background:var(--red);flex-shrink:0}

  /* ─── FOOTER ─── */
  footer{
    background:var(--dark);border-top:2px solid var(--border);
    padding:22px 16px;text-align:center;color:var(--muted);font-size:0.8rem;
  }
  footer strong{color:var(--gold)}

  /* ─── RESPONSIVE ─── */
  @media(max-width:480px){
    .product-grid{grid-template-columns:repeat(2,1fr)}
    .modal{max-height:95vh}
  }
  @media(min-width:600px){
    .product-grid{grid-template-columns:repeat(3,1fr)}
  }
  @media(min-width:800px){
    .product-grid{grid-template-columns:repeat(4,1fr)}
  }

  /* ─── ANIMATIONS ─── */
  @keyframes pop{0%{transform:scale(1)}50%{transform:scale(1.3)}100%{transform:scale(1)}}
  .pop{animation:pop 0.3s ease}
  @keyframes fadeIn{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
  .product-card{animation:fadeIn 0.4s ease both}

  /* Loading spinner */
  .spinner{display:inline-block;width:16px;height:16px;border:2px solid rgba(255,255,255,0.3);border-top-color:#fff;border-radius:50%;animation:spin 0.7s linear infinite}
  @keyframes spin{to{transform:rotate(360deg)}}
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="header-inner">
    <a class="logo-block" href="#">
      <div class="logo-icon">📱</div>
      <div class="logo-text">
        <div class="shop-name">JAI MATA DI MOBILE AGENCY</div>
        <div class="tagline">Mobile Phone &amp; Accessories</div>
      </div>
    </a>
    <button class="header-cart-btn" onclick="openCart()">
      🛒 Cart <span class="cart-count-badge" id="cartBadge1">0</span>
    </button>
  </div>
</header>

<!-- HERO STRIP -->
<div class="hero-strip">
  📍 Tengrari Minapur, Muzaffarpur, Bihar 843128 <span>|</span> 📞 9939676883 <span>|</span> 🚚 Order &amp; We'll Contact You!
</div>

<!-- MAIN -->
<main>
  <!-- Info Strip -->
  <div class="info-strip">
    <div class="info-item"><div class="info-dot"></div> <div><strong>How it works?</strong> Add items → Place Order → We contact you to confirm</div></div>
    <div class="info-item"><div class="info-dot" style="background:var(--gold)"></div> <div><strong>Free Delivery</strong> available in local area</div></div>
    <div class="info-item"><div class="info-dot" style="background:#2dc653"></div> <div><strong>WhatsApp</strong> confirmation after order</div></div>
  </div>

  <!-- Categories -->
  <p class="section-label">Browse By Category</p>
  <div class="cat-filters" id="catFilters"></div>

  <!-- Products -->
  <div class="products-heading">All Products</div>
  <div class="product-grid" id="productGrid"></div>
</main>

<!-- FOOTER -->
<footer>
  <div style="margin-bottom:6px">📱 <strong>JAI MATA DI MOBILE AGENCY</strong> — Mobile Phone &amp; Accessories</div>
  <div>Tengrari Minapur, Muzaffarpur, Bihar 843128 &nbsp;|&nbsp; ✉️ rajeevk2418@gmail.com</div>
  <div style="margin-top:8px;font-size:0.72rem;opacity:0.6">This is an order collection system. Payment &amp; confirmation via WhatsApp/Phone.</div>
</footer>

<!-- FLOATING BUTTONS -->
<div class="fab-group">
  <button class="fab fab-wa" title="Chat on WhatsApp" onclick="window.open('https://wa.me/919939676883?text=Hi%2C%20I%20want%20to%20enquire%20about%20your%20products','_blank')">💬</button>
  <button class="fab fab-cart" title="View Cart" onclick="openCart()">
    🛒
    <span class="fab-badge" id="cartBadge2">0</span>
  </button>
</div>

<!-- CART MODAL -->
<div class="overlay" id="cartOverlay" onclick="handleOverlayClick(event,'cartOverlay')">
  <div class="modal" id="cartModal">
    <div class="modal-header">
      <div class="modal-title">🛒 Your Cart</div>
      <button class="close-btn" onclick="closeCart()">✕</button>
    </div>
    <div class="modal-body" id="cartBody">
      <div class="cart-empty"><div class="empty-icon">🛒</div><p>Your cart is empty</p></div>
    </div>
    <div class="modal-footer" id="cartFooter" style="display:none">
      <div class="total-row">
        <span class="total-label">GRAND TOTAL</span>
        <span class="total-amount" id="cartTotal">₹0</span>
      </div>
      <button class="checkout-btn" onclick="openCheckout()">Proceed to Place Order →</button>
    </div>
  </div>
</div>

<!-- CHECKOUT MODAL -->
<div class="overlay" id="checkoutOverlay" onclick="handleOverlayClick(event,'checkoutOverlay')">
  <div class="modal" id="checkoutModal">
    <div class="modal-header">
      <div class="modal-title">📋 Place Order</div>
      <button class="close-btn" onclick="closeCheckout()">✕</button>
    </div>
    <div class="modal-body">
      <div class="order-summary-box" id="orderSummaryBox"></div>
      <!-- Formspree form — replace YOUR_FORM_ID with your actual Formspree form ID -->
      <form id="orderForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
        <!-- Hidden fields for email content -->
        <input type="hidden" name="_subject" id="emailSubject"/>
        <input type="hidden" name="Order_Summary" id="hiddenOrderSummary"/>
        <input type="hidden" name="Grand_Total" id="hiddenTotal"/>
        <input type="hidden" name="_next" value=""/>

        <div class="form-group">
          <label>Your Name *</label>
          <input type="text" name="Customer_Name" id="custName" placeholder="Enter your full name" required/>
        </div>
        <div class="form-group">
          <label>Phone Number *</label>
          <input type="tel" name="Customer_Phone" id="custPhone" placeholder="10-digit mobile number" required pattern="[0-9]{10}"/>
        </div>
        <div class="form-group">
          <label>Delivery Address *</label>
          <textarea name="Delivery_Address" id="custAddress" placeholder="House no., street, village/town, district, PIN" required></textarea>
        </div>
        <div class="form-group">
          <label>Special Instructions (optional)</label>
          <textarea name="Special_Instructions" id="custInstructions" placeholder="Any notes for the shop…" style="min-height:60px"></textarea>
        </div>
        <button type="submit" class="submit-btn" id="submitBtn">
          ✅ Place Order
        </button>
      </form>
    </div>
  </div>
</div>

<!-- SUCCESS TOAST -->
<div class="toast" id="successToast">
  <div>🎉 Order Placed Successfully!</div>
  <div style="font-size:0.82rem;opacity:0.9;margin-top:4px">JAI MATA DI MOBILE AGENCY will contact you on WhatsApp to confirm.</div>
  <a class="wa-link" href="https://wa.me/919939676883" target="_blank">💬 Message us directly: 9939676883</a>
</div>

<script>
// ─── PRODUCT DATA ───
const PRODUCTS = [
  {
    id:1, name:"Oppo Reno 15 Pro Mini 12/256",
    price:59999, category:"Smartphones",
    badge:"NEW",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Oppo Reno 15 Pro Mini 12/256GB Smartphone"
  },
  {
    id:2, name:"Samsung Galaxy A55 5G 8/128",
    price:38999, category:"Smartphones",
    badge:"HOT",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Samsung Galaxy A55 5G"
  },
  {
    id:3, name:"Redmi Note 14 Pro 5G 8/256",
    price:27999, category:"Smartphones",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Redmi Note 14 Pro 5G"
  },
  {
    id:4, name:"Realme 13 Pro+ 5G 12/256",
    price:35999, category:"Smartphones",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Realme 13 Pro Plus 5G"
  },
  {
    id:5, name:"boAt Rockerz 450 Wireless Headphone",
    price:1499, category:"Accessories",
    badge:"SALE",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"boAt Rockerz 450 Headphone"
  },
  {
    id:6, name:"USB-C Fast Charging Cable 65W",
    price:299, category:"Accessories",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"USB-C 65W Fast Charging Cable"
  },
  {
    id:7, name:"Tempered Glass Screen Guard (Universal)",
    price:149, category:"Accessories",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Tempered Glass Screen Protector"
  },
  {
    id:8, name:"65W GaN Fast Charger Adapter",
    price:899, category:"Chargers",
    badge:"NEW",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"65W GaN Fast Charger"
  },
  {
    id:9, name:"Wireless Bluetooth Earbuds TWS",
    price:999, category:"Accessories",
    badge:"HOT",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Wireless Bluetooth TWS Earbuds"
  },
  {
    id:10, name:"Vivo Y200e 5G 8/128GB",
    price:21999, category:"Smartphones",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Vivo Y200e 5G"
  },
  {
    id:11, name:"Mobile Back Cover (Silicon Shockproof)",
    price:199, category:"Accessories",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"Silicon Shockproof Phone Case"
  },
  {
    id:12, name:"Power Bank 20000mAh 22.5W",
    price:1799, category:"Chargers",
    badge:"",
    img:"https://i.ibb.co/1f7tyyLb/17743444996368791820999309670802.jpg",
    alt:"20000mAh Fast Charging Power Bank"
  }
];

// ─── STATE ───
let cart = JSON.parse(localStorage.getItem('jmda_cart') || '[]');
let activeCategory = 'All';

// ─── INIT ───
function init(){
  buildCategories();
  renderProducts();
  updateCartBadge();
}

function buildCategories(){
  const cats = ['All', ...new Set(PRODUCTS.map(p => p.category))];
  const container = document.getElementById('catFilters');
  container.innerHTML = '';
  cats.forEach(cat => {
    const btn = document.createElement('button');
    btn.className = 'cat-btn' + (cat === activeCategory ? ' active' : '');
    btn.textContent = cat === 'All' ? '🔍 All Products' : cat;
    btn.onclick = () => filterCategory(cat);
    container.appendChild(btn);
  });
}

function filterCategory(cat){
  activeCategory = cat;
  buildCategories();
  const cards = document.querySelectorAll('.product-card');
  cards.forEach(card => {
    const cardCat = card.dataset.category;
    if(cat === 'All' || cardCat === cat) card.classList.remove('hidden');
    else card.classList.add('hidden');
  });
  const heading = document.querySelector('.products-heading');
  heading.firstChild.textContent = cat === 'All' ? 'All Products' : cat + ' ';
}

function renderProducts(){
  const grid = document.getElementById('productGrid');
  grid.innerHTML = '';
  PRODUCTS.forEach((p, i) => {
    const inCart = cart.find(c => c.id === p.id);
    const card = document.createElement('div');
    card.className = 'product-card';
    card.dataset.category = p.category;
    card.style.animationDelay = (i * 0.05) + 's';
    card.innerHTML = `
      ${p.badge ? `<div class="badge">${p.badge}</div>` : ''}
      <div class="product-img-wrap">
        <img src="${p.img}" alt="${p.alt}" loading="lazy"/>
      </div>
      <div class="product-info">
        <div class="product-cat">${p.category}</div>
        <div class="product-name">${p.name}</div>
        <div class="product-price">₹${p.price.toLocaleString('en-IN')}</div>
      </div>
      <button class="add-btn${inCart ? ' added' : ''}" onclick="addToCart(${p.id},this)" id="addbtn-${p.id}">
        ${inCart ? '✅ Added' : '🛒 Add to Cart'}
      </button>
    `;
    grid.appendChild(card);
  });
}

// ─── CART LOGIC ───
function addToCart(id, btn){
  const product = PRODUCTS.find(p => p.id === id);
  const existing = cart.find(c => c.id === id);
  if(existing){
    existing.qty += 1;
  } else {
    cart.push({id: product.id, name: product.name, price: product.price, img: product.img, alt: product.alt, qty: 1});
  }
  saveCart();
  updateCartBadge();
  if(btn){
    btn.textContent = '✅ Added';
    btn.classList.add('added');
    btn.classList.add('pop');
    setTimeout(() => btn.classList.remove('pop'), 300);
  }
  if(document.getElementById('cartOverlay').classList.contains('open')) renderCartBody();
}

function removeFromCart(id){
  cart = cart.filter(c => c.id !== id);
  saveCart();
  updateCartBadge();
  renderCartBody();
  refreshAddButtons();
}

function changeQty(id, delta){
  const item = cart.find(c => c.id === id);
  if(!item) return;
  item.qty += delta;
  if(item.qty <= 0){ removeFromCart(id); return; }
  saveCart();
  updateCartBadge();
  renderCartBody();
}

function saveCart(){
  localStorage.setItem('jmda_cart', JSON.stringify(cart));
}

function getCartCount(){
  return cart.reduce((sum, c) => sum + c.qty, 0);
}

function getGrandTotal(){
  return cart.reduce((sum, c) => sum + c.price * c.qty, 0);
}

function updateCartBadge(){
  const count = getCartCount();
  document.getElementById('cartBadge1').textContent = count;
  document.getElementById('cartBadge2').textContent = count;
}

function refreshAddButtons(){
  PRODUCTS.forEach(p => {
    const btn = document.getElementById('addbtn-' + p.id);
    if(!btn) return;
    const inCart = cart.find(c => c.id === p.id);
    btn.textContent = inCart ? '✅ Added' : '🛒 Add to Cart';
    btn.className = 'add-btn' + (inCart ? ' added' : '');
  });
}

function renderCartBody(){
  const body = document.getElementById('cartBody');
  const footer = document.getElementById('cartFooter');
  const total = document.getElementById('cartTotal');
  if(cart.length === 0){
    body.innerHTML = '<div class="cart-empty"><div class="empty-icon">🛒</div><p>Your cart is empty</p></div>';
    footer.style.display = 'none';
    return;
  }
  body.innerHTML = cart.map(item => `
    <div class="cart-item">
      <img class="cart-item-img" src="${item.img}" alt="${item.alt}" loading="lazy"/>
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-sub">₹${item.price.toLocaleString('en-IN')} each</div>
        <div class="cart-item-price">₹${(item.price * item.qty).toLocaleString('en-IN')}</div>
        <div class="qty-controls">
          <button class="qty-btn" onclick="changeQty(${item.id},-1)">−</button>
          <span class="qty-display">${item.qty}</span>
          <button class="qty-btn" onclick="changeQty(${item.id},1)">+</button>
        </div>
      </div>
      <button class="remove-btn" onclick="removeFromCart(${item.id})">Remove</button>
    </div>
  `).join('');
  total.textContent = '₹' + getGrandTotal().toLocaleString('en-IN');
  footer.style.display = 'block';
}

// ─── MODAL CONTROLS ───
function openCart(){
  renderCartBody();
  document.getElementById('cartOverlay').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeCart(){
  document.getElementById('cartOverlay').classList.remove('open');
  document.body.style.overflow = '';
}
function openCheckout(){
  if(cart.length === 0) return;
  closeCart();
  buildOrderSummary();
  document.getElementById('checkoutOverlay').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeCheckout(){
  document.getElementById('checkoutOverlay').classList.remove('open');
  document.body.style.overflow = '';
}
function handleOverlayClick(e, id){
  if(e.target.id === id){ 
    document.getElementById(id).classList.remove('open');
    document.body.style.overflow='';
  }
}

function buildOrderSummary(){
  const box = document.getElementById('orderSummaryBox');
  const grand = getGrandTotal();
  box.innerHTML = `
    <div class="summary-title">📦 Order Summary</div>
    ${cart.map(item => `
      <div class="summary-item">
        <span>${item.name} × ${item.qty}</span>
        <span>₹${(item.price * item.qty).toLocaleString('en-IN')}</span>
      </div>
    `).join('')}
    <div class="summary-total">
      <span>Grand Total</span>
      <span>₹${grand.toLocaleString('en-IN')}</span>
    </div>
  `;
  // Build hidden field values
  const summaryText = cart.map(item =>
    `${item.name} x${item.qty} = Rs.${(item.price * item.qty).toLocaleString('en-IN')}`
  ).join(' | ');
  document.getElementById('hiddenOrderSummary').value = summaryText;
  document.getElementById('hiddenTotal').value = 'Rs.' + grand.toLocaleString('en-IN');
  document.getElementById('emailSubject').value = `New Order - JAI MATA DI MOBILE AGENCY - Rs.${grand.toLocaleString('en-IN')}`;
}

// ─── FORM SUBMIT ───
document.getElementById('orderForm').addEventListener('submit', async function(e){
  e.preventDefault();
  const btn = document.getElementById('submitBtn');
  btn.disabled = true;
  btn.innerHTML = '<span class="spinner"></span> Sending…';

  const name = document.getElementById('custName').value.trim();
  const phone = document.getElementById('custPhone').value.trim();
  const addr = document.getElementById('custAddress').value.trim();
  const instructions = document.getElementById('custInstructions').value.trim();

  // Build complete email body for Formspree
  const grand = getGrandTotal();
  const orderLines = cart.map(item =>
    `${item.name} x${item.qty} @ Rs.${item.price.toLocaleString('en-IN')} = Rs.${(item.price * item.qty).toLocaleString('en-IN')}`
  ).join('\n');

  const fullMessage = 
`=== NEW ORDER — JAI MATA DI MOBILE AGENCY ===

CUSTOMER DETAILS:
Name: ${name}
Phone: ${phone}
Address: ${addr}
${instructions ? 'Instructions: ' + instructions : ''}

ORDER ITEMS:
${orderLines}

GRAND TOTAL: Rs.${grand.toLocaleString('en-IN')}

==============================================`;

  // Update hidden field with full order
  document.getElementById('hiddenOrderSummary').value = fullMessage;
  document.getElementById('hiddenTotal').value = 'Rs.' + grand.toLocaleString('en-IN');

  try {
    const formData = new FormData(this);
    const response = await fetch(this.action, {
      method: 'POST',
      body: formData,
      headers: { 'Accept': 'application/json' }
    });

    if(response.ok){
      // Success
      cart = [];
      saveCart();
      updateCartBadge();
      refreshAddButtons();
      closeCheckout();
      this.reset();
      showSuccessToast();
    } else {
      const data = await response.json();
      if(data.error === 'INACTIVE_FORM'){
        alert('⚠️ Formspree form not set up yet.\n\nShop owner: Please create a free account at formspree.io, create a form, and replace YOUR_FORM_ID in the HTML file with your actual form ID.\n\nFor demo, order details:\n' + fullMessage);
        // Still treat as success for demo purposes
        cart = [];
        saveCart();
        updateCartBadge();
        refreshAddButtons();
        closeCheckout();
        this.reset();
        showSuccessToast();
      } else {
        alert('Order could not be sent. Please call us at 9939676883 or message on WhatsApp.');
      }
    }
  } catch(err) {
    // Network error — show fallback
    alert('⚠️ Could not send order online.\n\nPlease call: 9939676883\nOr WhatsApp: 9939676883\n\nYour order:\n' + fullMessage);
  }
  
  btn.disabled = false;
  btn.innerHTML = '✅ Place Order';
});

function showSuccessToast(){
  const toast = document.getElementById('successToast');
  toast.classList.add('show');
  setTimeout(() => toast.classList.remove('show'), 6000);
}

// ─── BOOT ───
init();
</script>
</body>
</html>
