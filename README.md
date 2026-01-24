<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Hoàng Hữu Khang — Portfolio</title>
  <meta name="description" content="Portfolio cá nhân của Hoàng Hữu Khang — data science, AI, frontend, projects, blog và liên hệ." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <!-- Tailwind CDN for utility classes (production: build with PostCSS) -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Custom design system on top of Tailwind */
    :root{
      --bg:#0f172a; /* slate-900 */
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#7c3aed; /* violet-600 */
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.03);
    }
    html,body,#app{height:100%;}
    body{
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(124,58,237,0.08), transparent),
                  radial-gradient(900px 400px at 90% 90%, rgba(14,165,233,0.04), transparent),
                  var(--bg);
      color: #e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:2rem;
    }
    /* Navigation */
    .nav-blur{backdrop-filter: blur(6px); background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));}
    .logo {font-weight:800; letter-spacing: -0.02em;}
    /* Hero */
    .hero-blob{filter: blur(44px); opacity:0.9;}
    /* Cards */
    .glass-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.015)); border:1px solid rgba(255,255,255,0.04); box-shadow: 0 8px 30px rgba(2,6,23,0.6);}
    /* Fancy code block */
    pre.code-block{background:linear-gradient(180deg, rgba(0,0,0,0.25), rgba(255,255,255,0.02)); padding:1rem; border-radius:10px; overflow:auto;}
    /* project hover */
    .project-card:hover{transform: translateY(-6px) scale(1.01); transition: all 260ms cubic-bezier(.2,.9,.2,1);}    
    .monogram{width:52px;height:52px;border-radius:12px;display:inline-grid;place-items:center;font-weight:700;background:linear-gradient(90deg,var(--accent),#06b6d4);}
    /* Footer */
    .faint{color:var(--muted);}    
    /* responsive adjustments */
    @media (max-width:900px){
      body{padding:1rem}
    }
  </style>
</head>
<body>
  <div id="app" class="max-w-7xl mx-auto">

    <!-- HEADER -->
    <header class="flex items-center justify-between py-4 px-4 nav-blur rounded-2xl glass-card">
      <div class="flex items-center gap-4">
        <div class="monogram">HK</div>
        <div>
          <div class="logo text-lg">Hoàng Hữu Khang</div>
          <div class="faint text-sm">Data Science • AI • Frontend</div>
        </div>
      </div>
      <nav class="hidden md:flex items-center gap-6 text-sm faint">
        <a href="#about" class="hover:text-white">About</a>
        <a href="#projects" class="hover:text-white">Projects</a>
        <a href="#resume" class="hover:text-white">Resume</a>
        <a href="#blog" class="hover:text-white">Blog</a>
        <a href="#contact" class="px-4 py-2 bg-gradient-to-r from-violet-600 to-cyan-500 rounded-lg text-black font-semibold">Hire me</a>
      </nav>
      <button class="md:hidden p-2 rounded-md faint" aria-label="menu">☰</button>
    </header>

    <!-- HERO -->
    <section id="hero" class="mt-8 grid grid-cols-12 gap-6 items-center">
      <div class="col-span-12 lg:col-span-6">
        <h1 class="text-4xl md:text-5xl font-extrabold leading-tight">Xin chào — tôi là <span style="background: linear-gradient(90deg,#f0f,#7c3aed); -webkit-background-clip: text; color:transparent;">Hoàng Hữu Khang</span>.</h1>
        <p class="mt-4 faint max-w-xl">Sinh viên Khoa học dữ liệu & AI. Tôi xây dựng sản phẩm bằng dữ liệu, mô hình ML, và giao diện frontend đẹp — kết hợp giữa logic mạnh mẽ và trải nghiệm mượt mà.</p>

        <div class="mt-6 flex gap-4 items-center">
          <a href="#projects" class="px-5 py-3 rounded-lg glass-card font-semibold">Xem dự án</a>
          <a href="#contact" class="px-5 py-3 rounded-lg border border-white/6 faint">Liên hệ</a>
        </div>

        <!-- highlights -->
        <div class="mt-8 grid grid-cols-3 gap-3 text-center">
          <div class="glass-card p-4 rounded-lg">
            <div class="text-2xl font-bold">12+</div>
            <div class="text-sm faint mt-1">Dự án thực hành</div>
          </div>
          <div class="glass-card p-4 rounded-lg">
            <div class="text-2xl font-bold">3</div>
            <div class="text-sm faint mt-1">Ngôn ngữ lập trình</div>
          </div>
          <div class="glass-card p-4 rounded-lg">
            <div class="text-2xl font-bold">1</div>
            <div class="text-sm faint mt-1">Bằng khen học thuật</div>
          </div>
        </div>

      </div>

      <div class="col-span-12 lg:col-span-6 relative">
        <div class="absolute -right-8 -top-8 w-96 h-80 rounded-3xl opacity-90 hero-blob" style="background:linear-gradient(135deg, rgba(124,58,237,0.28), rgba(6,182,212,0.16));"></div>
        <div class="glass-card p-6 rounded-2xl shadow-xl relative z-10">
          <div class="flex items-center gap-4">
            <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=600&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="avatar" class="w-24 h-24 rounded-xl object-cover border border-white/6"/>
            <div>
              <div class="font-semibold text-lg">Hoàng Hữu Khang</div>
              <div class="faint text-sm">Sinh viên năm nhất • Data Science & AI</div>
              <div class="faint text-xs mt-1">Thành phố Hồ Chí Minh · sẵn sàng làm việc thực tập</div>
            </div>
          </div>

          <hr class="my-4 border-white/4" />

          <div class="grid grid-cols-2 gap-3">
            <div>
              <div class="faint text-xs">Kỹ năng chính</div>
              <ul class="mt-2 text-sm">
                <li>Python • Numpy • Pandas</li>
                <li>ML: scikit-learn • LightGBM</li>
                <li>Frontend: HTML/CSS • JS • React</li>
              </ul>
            </div>
            <div>
              <div class="faint text-xs">Công cụ</div>
              <ul class="mt-2 text-sm">
                <li>Git • Docker</li>
                <li>VSCode • Colab</li>
                <li>Power BI • SQL</li>
              </ul>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="mt-12 grid grid-cols-12 gap-6">
      <div class="col-span-12 lg:col-span-7 glass-card p-8 rounded-2xl">
        <h2 class="text-2xl font-bold">Về tôi</h2>
        <p class="mt-4 faint">Tôi là một người vừa yêu thích phân tích dữ liệu vừa thích xây dựng giao diện — dễ dàng dịch các kết quả mô hình thành sản phẩm người dùng. Mục tiêu: trở thành một kỹ sư dữ liệu/AI có thể thiết kế hệ thống end-to-end từ thu thập dữ liệu, huấn luyện mô hình đến triển khai sản phẩm.</p>

        <div class="mt-6 grid grid-cols-2 gap-4">
          <div>
            <h3 class="font-semibold">Học vấn</h3>
            <p class="faint text-sm mt-1">Đại học — Khoa học Dữ liệu (2025 — ...)</p>
          </div>
          <div>
            <h3 class="font-semibold">Ngoại ngữ</h3>
            <p class="faint text-sm mt-1">Tiếng Anh (giao tiếp kỹ thuật)</p>
          </div>
        </div>

        <hr class="my-6 border-white/4" />

        <h3 class="font-semibold">Phương pháp làm việc</h3>
        <ul class="mt-3 list-disc pl-5 faint">
          <li>Ưu tiên viết code rõ ràng, có test và version control.</li>
          <li>Thích làm việc theo sprint, chia task nhỏ, review thường xuyên.</li>
          <li>Tập trung vào chất lượng dữ liệu trước khi tối ưu thuật toán.</li>
        </ul>

      </div>

      <aside class="col-span-12 lg:col-span-5">
        <div class="glass-card p-6 rounded-2xl">
          <h4 class="font-semibold">Kỹ năng chi tiết</h4>
          <div class="mt-4">
            <label class="faint text-xs">Python</label>
            <div class="w-full bg-white/5 rounded-full h-3 mt-1 overflow-hidden"><div class="h-3 bg-gradient-to-r from-violet-600 to-cyan-400" style="width:88%"></div></div>
          </div>
          <div class="mt-3">
            <label class="faint text-xs">Machine Learning</label>
            <div class="w-full bg-white/5 rounded-full h-3 mt-1 overflow-hidden"><div class="h-3 bg-gradient-to-r from-violet-600 to-cyan-400" style="width:76%"></div></div>
          </div>
          <div class="mt-3">
            <label class="faint text-xs">Frontend</label>
            <div class="w-full bg-white/5 rounded-full h-3 mt-1 overflow-hidden"><div class="h-3 bg-gradient-to-r from-violet-600 to-cyan-400" style="width:68%"></div></div>
          </div>
          <div class="mt-6 faint text-sm">Tôi luôn cập nhật kiến thức qua khoá học, bài báo, và project thực tế.</div>
        </div>

        <div class="mt-6 glass-card p-6 rounded-2xl">
          <h4 class="font-semibold">Sở thích</h4>
          <ul class="mt-3 faint list-disc pl-5 text-sm">
            <li>Giải thuật, đồ thị, toán rời rạc</li>
            <li>Đọc sách về AI và khoa học dữ liệu</li>
            <li>Thiết kế UI tối giản</li>
          </ul>
        </div>
      </aside>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="mt-12">
      <h2 class="text-2xl font-bold">Dự án tiêu biểu</h2>
      <p class="faint mt-2">Một số dự án mình đã làm — có mã nguồn, demo và mô tả kỹ thuật.</p>

      <div class="mt-6 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

        <!-- Project 1 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-indigo-600 to-teal-400 flex items-center justify-center font-bold">DS</div>
            <div>
              <h3 class="font-semibold">1. Dự án phân loại review</h3>
              <p class="faint text-sm mt-1">Mô tả: mô hình NLP phân loại review sản phẩm theo cảm xúc, xử lý bằng TF-IDF và LightGBM.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: Python, scikit-learn, LightGBM, Flask (API)</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Demo</a>
          </div>
        </article>

        <!-- Project 2 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-purple-600 to-pink-400 flex items-center justify-center font-bold">CV</div>
            <div>
              <h3 class="font-semibold">2. Dashboard phân tích dữ liệu bán hàng</h3>
              <p class="faint text-sm mt-1">Mô tả: dashboard tương tác dùng Power BI/Plotly, báo cáo KPI, A/B test và phân tích cohort.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: SQL, Pandas, Power BI, Dash (Plotly)</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Demo</a>
          </div>
        </article>

        <!-- Project 3 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-cyan-400 to-blue-600 flex items-center justify-center font-bold">FE</div>
            <div>
              <h3 class="font-semibold">3. Portfolio & Interactive UI</h3>
              <p class="faint text-sm mt-1">Mô tả: website cá nhân (mẫu này) — HTML/CSS/JS, hiệu ứng mượt mà, responsive.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: HTML, CSS, JS, Tailwind, accessibility</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Live</a>
          </div>
        </article>

        <!-- filler projects to lengthen file and show variety -->
        <!-- Project 4 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-green-500 to-emerald-400 flex items-center justify-center font-bold">CVR</div>
            <div>
              <h3 class="font-semibold">4. Mô hình dự đoán churn</h3>
              <p class="faint text-sm mt-1">Mô tả: mô hình dự báo churn khách hàng, feature engineering, balancing, và deploy trên Heroku.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: Pandas, SMOTE, XGBoost, Docker</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Demo</a>
          </div>
        </article>

        <!-- Project 5 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-amber-500 to-red-400 flex items-center justify-center font-bold">RL</div>
            <div>
              <h3 class="font-semibold">5. Thí nghiệm Reinforcement Learning</h3>
              <p class="faint text-sm mt-1">Mô tả: agent học trong môi trường sederhana, so sánh DQN và Policy Gradient.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: Gym, PyTorch, OpenAI Baselines</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Paper</a>
          </div>
        </article>

        <!-- Project 6 -->
        <article class="project-card glass-card p-6 rounded-2xl">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-sky-500 to-indigo-400 flex items-center justify-center font-bold">CV</div>
            <div>
              <h3 class="font-semibold">6. Computer Vision – Detection</h3>
              <p class="faint text-sm mt-1">Mô tả: hệ thống phát hiện vật thể, fine-tune YOLOv5 trên dataset tự thu thập.</p>
            </div>
          </div>
          <div class="mt-4 text-sm faint">Kỹ thuật: PyTorch, YOLOv5, LabelImg</div>
          <div class="mt-4 flex gap-2">
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Mã nguồn</a>
            <a class="text-xs px-3 py-1 rounded-md border border-white/6">Dataset</a>
          </div>
        </article>

      </div>

    </section>

    <!-- RESUME/BIO -->
    <section id="resume" class="mt-12 grid grid-cols-12 gap-6">
      <div class="col-span-12 lg:col-span-8 glass-card p-8 rounded-2xl">
        <h2 class="text-2xl font-bold">Kinh nghiệm & Học vấn</h2>
        <div class="mt-4 space-y-6">
          <div>
            <h3 class="font-semibold">Thực tập — Công ty ABC (2024)</h3>
            <p class="faint text-sm mt-1">Phát triển ETL, tiền xử lý dữ liệu và báo cáo KPI. Tối ưu thời gian chạy pipeline bằng caching và vectorized ops.</p>
          </div>
          <div>
            <h3 class="font-semibold">Đại học — Khoa học Dữ liệu (2025 — ...)</h3>
            <p class="faint text-sm mt-1">Các môn trọng tâm: Toán rời rạc, Xác suất - Thống kê, Learning Algorithms, Database.</p>
          </div>
        </div>
      </div>

      <aside class="col-span-12 lg:col-span-4 glass-card p-6 rounded-2xl">
        <h4 class="font-semibold">Tải CV</h4>
        <p class="faint text-sm mt-2">CV PDF có thể download bằng nút bên dưới.</p>
        <div class="mt-4">
          <a class="px-4 py-2 rounded-lg bg-gradient-to-r from-violet-600 to-cyan-400 text-black font-semibold">Tải CV</a>
        </div>
        <hr class="my-4 border-white/4" />
        <h4 class="font-semibold">Thông tin liên hệ</h4>
        <p class="faint text-sm mt-2">Email: <span class="text-sm">hoanghuukhang@example.com</span></p>
        <p class="faint text-sm">SĐT: +84 9xx xxx xxx</p>
      </aside>
    </section>

    <!-- BLOG -->
    <section id="blog" class="mt-12">
      <h2 class="text-2xl font-bold">Bài viết & Ghi chú</h2>
      <p class="faint mt-2">Các ghi chép về toán, thuật toán, mô hình và kinh nghiệm học tập.</p>

      <div class="mt-6 grid grid-cols-1 md:grid-cols-2 gap-6">
        <article class="glass-card p-6 rounded-2xl">
          <h3 class="font-semibold">Làm thế nào để học tốt ML từ cơ bản</h3>
          <p class="faint text-sm mt-2">Tóm tắt lộ trình: thống kê cơ bản → linear models → tree-based → neural networks → deploy.</p>
          <div class="mt-3 text-xs faint">3 phút đọc</div>
        </article>
        <article class="glass-card p-6 rounded-2xl">
          <h3 class="font-semibold">Kinh nghiệm debug pipeline dữ liệu</h3>
          <p class="faint text-sm mt-2">Tips: kiểm tra nguồn, sampling, phân phối, và logging có hệ thống.</p>
          <div class="mt-3 text-xs faint">5 phút đọc</div>
        </article>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="mt-12 grid grid-cols-12 gap-6">
      <div class="col-span-12 lg:col-span-7 glass-card p-8 rounded-2xl">
        <h2 class="text-2xl font-bold">Liên hệ</h2>
        <p class="faint mt-2">Muốn hợp tác hay trao đổi? Gửi tin nhắn nhé — mình trả lời trong vòng vài ngày làm việc.</p>

        <form class="mt-6 grid grid-cols-1 md:grid-cols-2 gap-4" onsubmit="handleForm(event)">
          <input required name="name" placeholder="Tên của bạn" class="p-3 rounded-lg bg-transparent border border-white/6" />
          <input required name="email" placeholder="Email" class="p-3 rounded-lg bg-transparent border border-white/6" />
          <textarea required name="message" placeholder="Nội dung" class="p-3 rounded-lg bg-transparent border border-white/6 md:col-span-2" rows="5"></textarea>
          <button type="submit" class="md:col-span-2 px-4 py-3 rounded-lg bg-gradient-to-r from-violet-600 to-cyan-400 text-black font-semibold">Gửi tin nhắn</button>
        </form>

      </div>

      <aside class="col-span-12 lg:col-span-5">
        <div class="glass-card p-6 rounded-2xl">
          <h4 class="font-semibold">Vị trí</h4>
          <p class="faint text-sm mt-2">Thành phố Hồ Chí Minh, Việt Nam</p>
          <div class="mt-4">
            <iframe title="map" src="https://www.google.com/maps?q=ho%20chi%20minh%20city&output=embed" class="w-full h-48 rounded-lg border border-white/6"></iframe>
          </div>
        </div>

        <div class="mt-6 glass-card p-6 rounded-2xl">
          <h4 class="font-semibold">Mạng xã hội</h4>
          <div class="mt-3 flex gap-3">
            <a class="px-3 py-2 rounded-lg faint border border-white/6">GitHub</a>
            <a class="px-3 py-2 rounded-lg faint border border-white/6">LinkedIn</a>
            <a class="px-3 py-2 rounded-lg faint border border-white/6">Twitter</a>
          </div>
        </div>
      </aside>
    </section>

    <!-- CTA -->
    <section class="mt-12 glass-card p-8 rounded-2xl text-center">
      <h3 class="text-xl font-bold">Sẵn sàng để bắt đầu dự án?</h3>
      <p class="faint mt-2">Gửi email hoặc nhấn nút "Hire me" — mình sẽ phản hồi sớm.</p>
      <div class="mt-4">
        <a href="#contact" class="px-6 py-3 rounded-lg bg-gradient-to-r from-violet-600 to-cyan-400 text-black font-semibold">Liên hệ ngay</a>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="mt-12 text-center faint text-sm">
      <div>© "Hoàng Hữu Khang" — Portfolio. Thiết kế & code bởi bạn — cập nhật 2025.</div>
      <div class="mt-2">Build: HTML + Tailwind + Vanilla JS — Responsive & Accessible</div>
    </footer>

  </div>

  <!-- SCRIPTS -->
  <script>
    function handleForm(e){
      e.preventDefault();
      const fd = new FormData(e.target);
      alert('Cảm ơn ' + fd.get('name') + '! Tin nhắn đã được gửi (demo).');
      e.target.reset();
    }

    // Tiny interactive touches
    document.querySelectorAll('.project-card').forEach(c=>{
      c.style.transition='transform 220ms cubic-bezier(.2,.9,.2,1)';
      c.addEventListener('mouseenter', ()=> c.style.transform='translateY(-6px)');
      c.addEventListener('mouseleave', ()=> c.style.transform='translateY(0)');
    });

    // simple theme switcher (prefers-color-scheme aware)
    const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
    if(!prefersDark){
      // if light, slightly lighten background
      document.body.style.background = 'linear-gradient(180deg, #f8fafc, #eef2ff)';
      document.body.style.color = '#0b1220';
    }
  </script>

</body>
</html>
