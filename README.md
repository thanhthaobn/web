<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Landing Page</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f9fafb;
      color: #111827;
    }
    header {
      background-color: #fff;
      border-bottom: 1px solid #e5e7eb;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    nav a {
      margin-left: 1rem;
      color: #374151;
      text-decoration: none;
      font-weight: 500;
    }
    nav a:hover {
      color: #111827;
    }
    section {
      padding: 3rem 2rem;
      max-width: 960px;
      margin: auto;
    }
    .hero {
      text-align: center;
    }
    .features, .pricing {
      display: grid;
      gap: 1.5rem;
    }
    .features {
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    }
    .feature, .price-card {
      background: #fff;
      border-radius: 1rem;
      padding: 1.5rem;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }
    .price-card.highlight {
      background: #4f46e5;
      color: white;
    }
    footer {
      text-align: center;
      padding: 2rem;
      font-size: 0.9rem;
      color: #6b7280;
    }
    button, .btn {
      display: inline-block;
      padding: 0.5rem 1rem;
      border-radius: 0.5rem;
      border: none;
      cursor: pointer;
      font-weight: bold;
    }
    .btn-primary {
      background-color: #4f46e5;
      color: white;
    }
    .btn-secondary {
      background-color: #fff;
      border: 1px solid #d1d5db;
      color: #374151;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo"><strong>MySite</strong></div>
    <nav>
      <a href="#features">Tính năng</a>
      <a href="#pricing">Bảng giá</a>
      <a href="#contact">Liên hệ</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Trang web đẹp, nhanh và dễ chỉnh sửa</h1>
    <p>Mẫu landing page một trang, phù hợp cho sản phẩm, portfolio hoặc dịch vụ nhỏ.</p>
    <div style="margin-top: 1rem;">
      <a href="#contact" class="btn btn-primary">Dùng thử miễn phí</a>
      <a href="#features" class="btn btn-secondary">Tìm hiểu thêm</a>
    </div>
  </section>

  <section id="features">
    <h2>Tính năng chính</h2>
    <div class="features">
      <div class="feature">
        <h3>⚡ Nhanh & Nhẹ</h3>
        <p>Tải trang nhanh, tối ưu cho thiết bị di động và desktop.</p>
      </div>
      <div class="feature">
        <h3>✨ Thiết kế hiện đại</h3>
        <p>Giao diện tối giản, thuận tiện cho người dùng.</p>
      </div>
      <div class="feature">
        <h3>🧩 Dễ tuỳ biến</h3>
        <p>Component rõ ràng để bạn mở rộng dễ dàng.</p>
      </div>
    </div>
  </section>

  <section id="pricing">
    <h2>Bảng giá</h2>
    <div class="features">
      <div class="price-card">
        <h3>Starter</h3>
        <p><strong>Free</strong></p>
        <ul>
          <li>✓ 1 trang tĩnh</li>
          <li>✓ Hỗ trợ cơ bản</li>
          <li>✓ Cập nhật thủ công</li>
        </ul>
      </div>
      <div class="price-card highlight">
        <h3>Pro</h3>
        <p><strong>$9/mo</strong></p>
        <ul>
          <li>✓ Nhiều trang</li>
          <li>✓ Hỗ trợ email</li>
          <li>✓ Tự động deploy</li>
        </ul>
      </div>
      <div class="price-card">
        <h3>Enterprise</h3>
        <p><strong>Liên hệ</strong></p>
        <ul>
          <li>✓ Tuỳ chỉnh nâng cao</li>
          <li>✓ Hỗ trợ 24/7</li>
          <li>✓ SLA cam kết</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Liên hệ</h2>
    <form onsubmit="event.preventDefault(); alert('Form đã được gửi (demo)');">
      <input type="text" placeholder="Tên của bạn" required style="display:block;width:100%;margin-bottom:0.5rem;padding:0.5rem;border:1px solid #d1d5db;border-radius:0.5rem;">
      <input type="email" placeholder="Email" required style="display:block;width:100%;margin-bottom:0.5rem;padding:0.5rem;border:1px solid #d1d5db;border-radius:0.5rem;">
      <textarea placeholder="Tin nhắn" required style="display:block;width:100%;margin-bottom:0.5rem;padding:0.5rem;border:1px solid #d1d5db;border-radius:0.5rem;"></textarea>
      <button type="submit" class="btn btn-primary">Gửi</button>
    </form>
  </section>

  <footer>
    © 2025 MySite. All rights reserved.
  </footer>
</body>
</html>
