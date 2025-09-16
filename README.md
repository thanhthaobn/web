# web
<!doctype html>
<!--
  Landing Page - HTML5 + CSS (single file)
  - Responsive, semantic HTML5 structure
  - Minimal vanilla JS for form handling and mobile menu
  - Replace images/placeholders with your own assets
-->
<html lang="vi">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>MySite — Landing Page</title>
    <meta name="description" content="Mẫu landing page HTML5, responsive, tối ưu cho mobile và desktop." />

    <style>
      /* Reset cơ bản */
      :root{--accent:#4f46e5;--muted:#6b7280;--bg:#f8fafc}
      *{box-sizing:border-box}
      html,body{height:100%}
      body{margin:0;font-family:Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;color:#0f172a;background:var(--bg);}

      /* Container */
      .container{max-width:1100px;margin:0 auto;padding:24px}

      /* Header */
      header{background:#fff;border-bottom:1px solid #e6edf3}
      .nav{display:flex;align-items:center;justify-content:space-between;padding:16px 0}
      .brand{display:flex;align-items:center;gap:8px}
      .brand .logo{font-weight:800;font-size:1.15rem}
      nav a{margin-left:18px;color:var(--muted);text-decoration:none}
      .cta{background:var(--accent);color:#fff;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:600}
      .mobile-toggle{display:none;border:0;background:transparent;font-size:20px}

      /* Hero */
      .hero{display:grid;grid-template-columns:1fr 1fr;gap:28px;align-items:center;padding:48px 0}
      .hero h1{font-size:2.2rem;margin:0;line-height:1.05}
      .hero p{color:var(--muted);margin-top:12px}
      .hero .actions{margin-top:22px;display:flex;gap:12px}
      .card{background:#fff;border-radius:14px;box-shadow:0 6px 18px rgba(15,23,42,0.06);overflow:hidden}
      .screenshot{height:320px;background:linear-gradient(135deg,#eef2ff,#fff);display:flex;align-items:center;justify-content:center;color:#94a3b8}

      /* Features */
      .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:20px}
      .feature{background:#fff;padding:18px;border-radius:12px}
      .feature h3{margin:0}
      .muted{color:var(--muted)}

      /* Pricing */
      .pricing{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:18px}
      .price{background:#fff;padding:20px;border-radius:12px;text-align:center}
      .price .tag{font-weight:700}

      /* Contact / Form */
      form{display:grid;gap:10px}
      input,textarea{width:100%;padding:10px;border:1px solid #e6edf3;border-radius:8px}
      button[type=submit]{background:var(--accent);color:#fff;padding:10px;border-radius:8px;border:0;font-weight:600}

      /* Footer */
      footer{padding:28px 0;text-align:center;color:var(--muted)}

      /* Responsive */
      @media (max-width:900px){
        .hero{grid-template-columns:1fr;}
        .grid{grid-template-columns:repeat(2,1fr)}
        .pricing{grid-template-columns:1fr}
      }
      @media (max-width:640px){
        nav a{display:none}
        .mobile-toggle{display:inline-block}
        .grid{grid-template-columns:1fr}
      }
    </style>
  </head>

  <body>
    <header>
      <div class="container nav">
        <div class="brand">
          <div class="logo">MySite</div>
          <div class="muted">Clean Landing</div>
        </div>

        <nav id="main-nav" aria-label="Main navigation">
          <a href="#features">Tính năng</a>
          <a href="#pricing">Bảng giá</a>
          <a href="#contact">Liên hệ</a>
        </nav>

        <div style="display:flex;gap:12px;align-items:center">
          <a class="cta" href="#contact">Bắt đầu</a>
          <button class="mobile-toggle" id="mobile-btn" aria-label="Mở menu">☰</button>
        </div>
      </div>
    </header>

    <main class="container">
      <!-- HERO -->
      <section class="hero" aria-labelledby="hero-heading">
        <div>
          <h1 id="hero-heading">Trang web HTML5 đẹp — nhanh và dễ chỉnh sửa</h1>
          <p>Mẫu landing page viết bằng HTML5, CSS thuần và JavaScript nhẹ. Thích hợp cho sản phẩm, portfolio, hoặc dịch vụ nhỏ.</p>

          <div class="actions">
            <a class="cta" href="#contact">Dùng thử miễn phí</a>
            <a href="#features" style="padding:10px 14px;border-radius:10px;border:1px solid #e6edf3;text-decoration:none;font-weight:600">Tìm hiểu thêm</a>
          </div>

          <dl style="display:flex;gap:16px;margin-top:18px;color:var(--muted);font-size:0.95rem">
            <div>
              <dt style="font-weight:700">Uptime</dt>
              <dd>99.9%</dd>
            </div>
            <div>
              <dt style="font-weight:700">Ngôn ngữ</dt>
              <dd>HTML5 + CSS + JS</dd>
            </div>
            <div>
              <dt style="font-weight:700">Bảo mật</dt>
              <dd>HTTPS-ready</dd>
            </div>
          </dl>
        </div>

        <div>
          <div class="card">
            <div class="screenshot">
              <div>
                <div style="font-size:1.25rem;font-weight:700;color:#0f172a">Ảnh demo</div>
                <div class="muted" style="margin-top:8px">Thay bằng ảnh hoặc video sản phẩm</div>
              </div>
            </div>
            <div style="padding:14px;color:var(--muted);font-size:0.95rem">Bạn có thể đặt slideshow, mô phỏng sản phẩm hoặc video ở khu vực này.</div>
          </div>
        </div>
      </section>

      <!-- FEATURES -->
      <section id="features" style="margin-top:36px">
        <h2>Tính năng chính</h2>
        <p class="muted">Điểm mạnh giúp sản phẩm của bạn nổi bật.</p>

        <div class="grid">
          <article class="feature">
            <div style="font-size:20px">⚡</div>
            <h3>Nhanh & nhẹ</h3>
            <p class="muted">Tối ưu để tải nhanh trên mọi thiết bị.</p>
          </article>

          <article class="feature">
            <div style="font-size:20px">✨</div>
            <h3>Thiết kế hiện đại</h3>
            <p class="muted">Giao diện tối giản, dễ tùy biến.</p>
          </article>

          <article class="feature">
            <div style="font-size:20px">🧩</div>
            <h3>Dễ mở rộng</h3>
            <p class="muted">Cấu trúc HTML rõ ràng, dễ thêm component.</p>
          </article>

          <article class="feature">
            <div style="font-size:20px">🔒</div>
            <h3>Bảo mật</h3>
            <p class="muted">Thiết lập HTTPS, header bảo mật đơn giản.</p>
          </article>

          <article class="feature">
            <div style="font-size:20px">📱</div>
            <h3>Responsive</h3>
            <p class="muted">Hiển thị tốt trên mobile và desktop.</p>
          </article>

          <article class="feature">
            <div style="font-size:20px">⚙️</div>
            <h3>Dễ triển khai</h3>
            <p class="muted">Đưa lên Netlify, Vercel hoặc hosting tĩnh khác.</p>
          </article>
        </div>
      </section>

      <!-- PRICING -->
      <section id="pricing" style="margin-top:36px">
        <h2>Bảng giá</h2>
        <p class="muted">Các gói phù hợp từ cá nhân đến doanh nghiệp nhỏ.</p>

        <div class="pricing">
          <div class="price">
            <div class="tag">Starter</div>
            <div style="font-size:24px;margin-top:8px;font-weight:700">Miễn phí</div>
            <ul style="text-align:left;margin:12px 0;padding-left:18px;color:var(--muted)">
              <li>1 trang tĩnh</li>
              <li>Hỗ trợ cơ bản</li>
              <li>Cập nhật thủ công</li>
            </ul>
            <button style="padding:8px 12px;border-radius:8px;border:1px solid #e6edf3">Chọn</button>
          </div>

          <div class="price" style="background:linear-gradient(180deg,#4f46e5,#6366f1);color:#fff">
            <div class="tag">Pro</div>
            <div style="font-size:24px;margin-top:8px;font-weight:700">$9 / tháng</div>
            <ul style="text-align:left;margin:12px 0;padding-left:18px;opacity:0.95">
              <li>Nhiều trang</li>
              <li>Hỗ trợ email</li>
              <li>Tự động deploy</li>
            </ul>
            <button style="padding:8px 12px;border-radius:8px;border:0;background:#fff;color:#4f46e5;font-weight:700">Dùng thử</button>
          </div>

          <div class="price">
            <div class="tag">Business</div>
            <div style="font-size:24px;margin-top:8px;font-weight:700">Liên hệ</div>
            <ul style="text-align:left;margin:12px 0;padding-left:18px;color:var(--muted)">
              <li>Tùy chỉnh thương hiệu</li>
              <li>Hỗ trợ ưu tiên</li>
              <li>Quản lý khách hàng</li>
            </ul>
            <button style="padding:8px 12px;border-radius:8px;border:1px solid #e6edf3">Liên hệ</button>
          </div>
        </div>
      </section>

      <!-- CONTACT -->
      <section id="contact" style="margin-top:36px">
        <h2>Liên hệ</h2>
        <p class="muted">Gửi thông tin để mình liên hệ lại hoặc thử bản dùng thử.</p>

        <div style="display:grid;grid-template-columns:1fr 380px;gap:18px;margin-top:12px">
          <div>
            <form id="contact-form">
              <label for="name">Họ và tên</label>
              <input id="name" name="name" placeholder="Nguyễn Văn A" required />

              <label for="email">Email</label>
              <input id="email" name="email" type="email" placeholder="you@example.com" required />

              <label for="message">Nội dung</label>
              <textarea id="message" name="message" rows="6" placeholder="Bạn cần gì?" required></textarea>

              <button type="submit">Gửi</button>

              <div id="form-msg" style="margin-top:8px;color:var(--muted)"></div>
            </form>
          </div>

          <aside style="background:#fff;padding:16px;border-radius:12px;align-self:start">
            <h3>Thông tin khác</h3>
            <p class="muted" style="margin-top:8px">Email: hello@mysite.example<br/>Địa chỉ: Hà Nội, Việt Nam</p>
          </aside>
        </div>
      </section>

    </main>

    <footer>
      <div class="container">
        <p>&copy; <span id="year"></span> MySite. All rights reserved.</p>
      </div>
    </footer>

    <script>
      // Set current year
      document.getElementById('year').textContent = new Date().getFullYear();

      // Mobile menu (very simple)
      const mobileBtn = document.getElementById('mobile-btn');
      mobileBtn.addEventListener('click', () => {
        const nav = document.getElementById('main-nav');
        if (nav.style.display === 'block') {
          nav.style.display = '';
        } else {
          nav.style.display = 'block';
          nav.style.position = 'absolute';
          nav.style.right = '24px';
          nav.style.top = '64px';
          nav.style.background = '#fff';
          nav.style.padding = '12px';
          nav.style.borderRadius = '8px';
          nav.style.boxShadow = '0 6px 18px rgba(15,23,42,0.08)';
        }
      });

      // Form submit (demo only)
      const form = document.getElementById('contact-form');
      const formMsg = document.getElementById('form-msg');
      form.addEventListener('submit', (e) => {
        e.preventDefault();
        const data = new FormData(form);
        formMsg.textContent = 'Đang gửi...';

        // Demo: mô phỏng gửi và reset form
        setTimeout(() => {
          formMsg.textContent = 'Cảm ơn! Mình sẽ liên hệ lại sớm.';
          form.reset();
        }, 800);
      });
    </script>
  </body>
</html>
