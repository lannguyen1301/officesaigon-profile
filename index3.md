```html
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Đặng Thành Tín | Giám đốc điều hành Office Saigon</title>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />

        <style>
            /* ================= BIẾN HỆ THỐNG OFFICE SAIGON ================= */
            :root {
                --os-blue: #135e9c;
                --os-orange: #f26522;
                --os-green: #2e7d32;
                --os-bg-light: #f4fbf4;
                --os-border: #e0e0e0;
                --os-text-main: #333333;
                --os-text-muted: #666666;
            }

            /* ================= CƠ BẢN ================= */
            * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                font-family: Arial, Helvetica, sans-serif;
            }

            body {
                color: var(--os-text-main);
                line-height: 1.6;
                background-color: #f9fbfd;
            }

            .container {
                max-width: 1140px;
                margin: 0 auto;
                padding: 40px 20px;
            }

            /* ================= UTILITIES ================= */
            .os-radius {
                border-radius: 10px;
            }

            .bold {
                font-weight: bold;
            }

            .italic {
                font-style: italic;
            }

            .t-upper {
                text-transform: uppercase;
            }

            .txt-blue {
                color: var(--os-blue);
            }

            .txt-orange {
                color: var(--os-orange);
            }

            .txt-green {
                color: var(--os-green);
            }

            .txt-center {
                text-align: center;
            }

            .txt-right {
                text-align: right;
            }

            .mb-10 {
                margin-bottom: 10px;
            }

            .mb-15 {
                margin-bottom: 15px;
            }

            .mb-20 {
                margin-bottom: 20px;
            }

            .mt-10 {
                margin-top: 10px;
            }

            .mt-15 {
                margin-top: 15px;
            }

            .mt-30 {
                margin-top: 30px;
            }

            .pt-15 {
                padding-top: 15px;
            }

            .border-top {
                border-top: 1px solid var(--os-border);
            }

            .border-none {
                border-bottom: none !important;
            }

            .os-text-justify {
                text-align: justify;
            }

            .os-section {
                width: 100%;
                margin-bottom: 40px;
                background: #fff;
                padding: 30px;
                border: 1px solid var(--os-border);
            }

            .os-grid-2 {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 30px;
            }

            .os-box {
                border: 1px solid var(--os-border);
                padding: 20px;
                background: #fff;
            }

            .os-section-title {
                color: var(--os-blue);
                font-size: 1.2rem;
                margin-bottom: 20px;
                border-bottom: 2px solid var(--os-blue);
                padding-bottom: 10px;
                display: inline-block;
            }

            /* ================= HERO QUOTE ================= */
            .os-exp-title {
                font-size: 1.1rem;
                letter-spacing: 1px;
            }

            .os-quote-left-wrap {
                display: flex;
                align-items: flex-start;
                gap: 15px;
                background: var(--os-bg-light);
                padding: 20px;
                border: 1px solid #cce8cc;
            }

            .os-quote-icon {
                font-size: 2rem;
                color: var(--os-green);
                opacity: 0.5;
            }

            .os-quote-text {
                font-size: 1.1rem;
                color: var(--os-blue);
            }

            /* ================= DANH SÁCH ================= */
            .os-list-row {
                display: flex;
                align-items: flex-start;
                padding: 10px 0;
                border-bottom: 1px solid #eee;
            }

            .os-pc-icon {
                color: var(--os-green);
                margin-right: 12px;
                margin-top: 4px;
                font-size: 1.1rem;
            }

            /* ================= TIMELINE ================= */
            .os-timeline {
                position: relative;
                padding-left: 20px;
                margin: 10px 0;
            }

            .os-timeline::before {
                content: "";
                position: absolute;
                left: 4px;
                top: 5px;
                bottom: 5px;
                width: 2px;
                background: #e0e0e0;
            }

            .os-tl-item {
                position: relative;
                margin-bottom: 25px;
                padding-left: 25px;
            }

            .os-tl-item:last-child {
                margin-bottom: 0;
            }

            .os-tl-dot {
                position: absolute;
                left: -20px;
                top: 4px;
                width: 12px;
                height: 12px;
                border-radius: 50%;
                background: var(--os-orange);
                border: 2px solid #fff;
                box-shadow: 0 0 0 1px var(--os-orange);
            }

            .os-tl-date {
                display: block;
                font-size: 14px;
                margin-bottom: 5px;
            }

            /* ================= LOGO KHÁCH HÀNG ================= */
            .os-client-grid {
                display: flex;
                flex-wrap: wrap;
                gap: 15px;
                justify-content: center;
            }

            .os-client-logo {
                padding: 12px 25px;
                border: 1px solid var(--os-border);
                background: #f9fbfd;
                font-size: 15px;
                letter-spacing: 0.5px;
                transition: 0.3s;
            }

            .os-client-logo:hover {
                border-color: var(--os-blue);
                background: #fff;
                box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            }

            /* ================= SLIDER NHẬN XÉT ================= */
            .slider-wrapper {
                position: relative;
                width: 100%;
                padding: 0 50px;
                margin-top: 20px;
            }

            .slider-container {
                overflow: hidden;
                border-radius: 10px;
            }

            .slider-track {
                display: flex;
                transition: transform 0.5s ease-in-out;
            }

            .slide {
                min-width: 100%;
                padding: 0 10px;
                box-sizing: border-box;
            }

            .slider-btn {
                position: absolute;
                top: 50%;
                transform: translateY(-50%);
                width: 40px;
                height: 40px;
                background: #fff;
                border: 1px solid var(--os-blue);
                color: var(--os-blue);
                border-radius: 50%;
                display: flex;
                align-items: center;
                justify-content: center;
                cursor: pointer;
                transition: 0.3s;
                z-index: 10;
            }

            .slider-btn:hover {
                background: var(--os-blue);
                color: #fff;
            }

            .prev-btn {
                left: 0;
            }

            .next-btn {
                right: 0;
            }

            .slider-dots {
                display: flex;
                justify-content: center;
                gap: 8px;
                margin-top: 20px;
            }

            .dot {
                width: 10px;
                height: 10px;
                border-radius: 50%;
                background: #ccc;
                cursor: pointer;
                transition: 0.3s;
            }

            .dot.active {
                background: var(--os-blue);
                transform: scale(1.2);
            }

            /* ================= RESPONSIVE ================= */
            @media screen and (max-width: 768px) {
                .os-grid-2 {
                    grid-template-columns: 1fr;
                }

                .slider-wrapper {
                    padding: 0;
                }

                .slider-btn {
                    display: none;
                }
            }
        </style>
    </head>

    <body>
        <div class="container">
            <!-- ================= HERO SECTION ================= -->
            <div class="os-section os-radius">
                <div class="os-grid-2" style="align-items: center;">
                    <div class="os-box-flex txt-center">
                        <img
                            src="./data/upload/dang-thanh-tin.jpg"
                            alt="Giám đốc Đặng Thành Tín"
                            class="os-radius"
                            style="max-width: 100%; box-shadow: 0 10px 20px rgba(0,0,0,0.05);"
                        />
                    </div>

                    <div class="os-box-flex">
                        <p class="os-exp-title txt-orange t-upper bold mb-10">Giám đốc điều hành</p>
                        <h1 class="txt-blue bold t-upper mb-15" style="font-size: 2.8rem;">Đặng Thành Tín</h1>

                        <div class="os-quote-left-wrap os-radius mb-20">
                            <i class="fa-solid fa-quote-left os-quote-icon"></i>
                            <div>
                                <p class="os-quote-text italic bold">
                                    "Hãy làm Khách hàng hài lòng và họ sẽ trao cho bạn cuộc sống của họ"
                                </p>
                                <p class="mt-10 txt-right bold">- Paul Orfalea (Kinko's)</p>
                            </div>
                        </div>

                        <p class="os-text-justify mb-15">
                            Trong công việc tôi luôn hướng tới sự hài lòng của khách hàng là phương châm sống của tôi.
                        </p>
                        <p class="os-text-justify">
                            Trong suốt thời gian làm việc trên 10 năm qua mỗi khi đáp ứng sự hài lòng của khách hàng là
                            niềm hạnh phúc cao cả vô bờ bến đối với tôi là động lực giúp tôi làm việc vô cùng hiệu quả.
                        </p>
                    </div>
                </div>
            </div>

            <!-- ================= NĂNG LỰC & HỌC VẤN ================= -->
            <div class="os-section os-radius">
                <h2 class="os-section-title t-upper bold">Chức vụ hiện tại & Trình độ học vấn</h2>
                <div class="os-grid-2">
                    <div class="os-box os-radius">
                        <p class="bold mb-15 txt-blue">Công ty TNHH Office Saigon</p>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Office Saigon Top 10 thương hiệu dẫn đầu năm 2019</span>
                        </div>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Top 10 thương hiệu mạnh Quốc gia năm 2019</span>
                        </div>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Top 30 thương hiệu BĐS xuất sắc Việt Nam</span>
                        </div>
                    </div>

                    <div class="os-box os-radius">
                        <p class="bold mb-15 txt-blue">Nền tảng tri thức</p>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Cao Đẳng Sư Phạm</span>
                        </div>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Chứng chỉ quản trị quản lý cấp cao CEO - Pace</span>
                        </div>
                        <div class="os-list-row border-none">
                            <i class="fa-solid fa-check os-pc-icon"></i>
                            <span>Chứng chỉ kiểm định giá cho thuê tòa nhà</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- ================= QUÁ TRÌNH CÔNG TÁC ================= -->
            <!-- <div class="os-section os-radius">
            <h2 class="os-section-title t-upper bold">Quá trình công tác</h2>
            <div class="os-box os-radius">
                <div class="os-timeline">
                    <div class="os-tl-item">
                        <div class="os-tl-dot"></div>
                        <div class="os-tl-content">
                            <span class="os-tl-date bold txt-orange">2017 - Nay</span>
                            <p class="bold txt-blue">GĐĐH Công ty TNHH Office Saigon.</p>
                        </div>
                    </div>
                    <div class="os-tl-item">
                        <div class="os-tl-dot"></div>
                        <div class="os-tl-content">
                            <span class="os-tl-date bold txt-orange">2015 - 2017</span>
                            <p class="bold txt-blue">P.GĐ Công ty TNHH Office Saigon.</p>
                        </div>
                    </div>
                    <div class="os-tl-item">
                        <div class="os-tl-dot"></div>
                        <div class="os-tl-content">
                            <span class="os-tl-date bold txt-orange">2013 - 2015</span>
                            <p class="bold txt-blue">Tp.Kinh doanh Cty TNHH DV BĐS Leader Real.</p>
                        </div>
                    </div>
                    <div class="os-tl-item">
                        <div class="os-tl-dot"></div>
                        <div class="os-tl-content">
                            <span class="os-tl-date bold txt-orange">2008 - 2013</span>
                            <p class="bold txt-blue">Thầu xây dựng công trình nhà phố tại Tp.HCM.</p>
                        </div>
                    </div>
                </div>
            </div>

            <div class="os-box os-radius mt-15" style="background: #f0f6fa; border-color: #bbdefb;">
                <p class="os-text-justify">Hiện tôi đã có trên 10 năm kinh nghiệm làm việc trong lĩnh vực BĐS và Văn
                    Phòng Cho Thuê, cùng với những kỹ năng và kiến thức có được từ khóa học về quản lý CEO, kiến thức
                    chuyên sâu về bán hàng Bất Động Sản trường Pace, tôi đã hợp tác và hỗ trợ thành công được trên 200
                    doanh nghiệp lớn nhỏ, tập đoàn đa quốc gia trong và ngoài nước tìm được mặt bằng phù hợp trong thời
                    gian qua.</p>
            </div>
        </div> -->

            <!-- ================= KHÁCH HÀNG & ĐỐI TÁC ================= -->
            <!-- <div class="os-section os-radius">
            <h2 class="os-section-title t-upper bold">Khách hàng tiêu biểu</h2>
            <div class="os-box os-radius txt-center mb-20">
                <p class="bold txt-blue" style="font-size: 1.8rem;">2013 - Nay</p>
                <p class="os-text-justify mt-10" style="text-align: center;">Đã hỗ trợ thành công hơn 200 doanh nghiệp
                    trong và ngoài nước thuê được văn phòng phù hợp từ văn phòng Hạng C đến văn phòng Hạng A tại Tp.HCM.
                </p>
            </div>

            <div class="os-client-grid">
                <span class="os-client-logo os-radius bold txt-blue">CADIVI</span>
                <span class="os-client-logo os-radius bold txt-green">CỐC CỐC</span>
                <span class="os-client-logo os-radius bold txt-orange">POLY</span>
                <span class="os-client-logo os-radius bold txt-blue">KHANG ĐIỀN</span>
                <span class="os-client-logo os-radius bold txt-green">TOÀN THỊNH PHÁT</span>
            </div>
        </div> -->

            <!-- ================= NHẬN XÉT TỪ KHÁCH HÀNG ================= -->
            <!-- <div class="os-section os-radius">
            <h2 class="os-section-title t-upper bold">Nhận xét từ khách hàng</h2>

            <div class="slider-wrapper">
                <button class="slider-btn prev-btn" id="prevSlide"><i class="fa-solid fa-chevron-left"></i></button>
                <div class="slider-container">
                    <div class="slider-track" id="sliderTrack">

                        <div class="slide">
                            <div class="os-box os-radius" style="height: 100%;">
                                <div class="os-quote-left-wrap border-none mb-15"
                                    style="background: transparent; border: none; padding: 0;">
                                    <i class="fa-solid fa-quote-left os-quote-icon"></i>
                                    <p class="os-text-justify italic">"Hơn 1 năm tìm thuê mặt bằng cho Công ty nhưng vẫn
                                        chưa tìm thấy vị trí nào phù hợp, mất thời gian nên tôi đã liên hệ Công ty
                                        Office Saigon và được anh Tín tư vấn, hỗ trợ và đi khảo sát 1 số vị trí và bên
                                        tôi đã chọn được vị trí bên tòa nhà Beta 2 với 727m2. Anh Tín bên Office Saigon
                                        đã deal giá rất tốt với bên tòa nhà Beta 2 và BLĐ Cadivi đã quyết định chốt thuê
                                        tại tòa nhà Beta 2."</p>
                                </div>
                                <div class="pt-15 border-top">
                                    <p class="bold txt-blue">Anh Hà</p>
                                    <p style="font-size: 0.9rem;">Giám đốc nhân sự - CADIVI</p>
                                </div>
                            </div>
                        </div>

                        <div class="slide">
                            <div class="os-box os-radius" style="height: 100%;">
                                <div class="os-quote-left-wrap border-none mb-15"
                                    style="background: transparent; border: none; padding: 0;">
                                    <i class="fa-solid fa-quote-left os-quote-icon"></i>
                                    <p class="os-text-justify italic">"Sau 6 tháng, chúng tôi mất quá nhiều thời gian
                                        nhưng lại không tìm được văn phòng mong muốn. Vì vậy tôi đã liên hệ Office
                                        Saigon và đã được anh Tín hỗ trợ rất nhiệt tình với thông tin chính xác và nhanh
                                        chóng, sau khi đi xem diện tích tại tòa nhà Saigon Trade Center, trong vòng 2
                                        tuần anh Tín đã thương lượng cho Công ty chúng tôi mức giá phù hợp với tòa nhà
                                        và BLĐ AsiaFood đã quyết định thuê 517m2 tại tòa nhà Saigon Trade Center Q1."
                                    </p>
                                </div>
                                <div class="pt-15 border-top">
                                    <p class="bold txt-blue">Chị Thảo</p>
                                    <p style="font-size: 0.9rem;">Trợ lý Tổng Giám đốc - AsiaFood</p>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
                <button class="slider-btn next-btn" id="nextSlide"><i class="fa-solid fa-chevron-right"></i></button>
                <div class="slider-dots" id="sliderDots"></div>
            </div>
        </div> -->
        </div>

        <!-- ================= JAVASCRIPT CHO SLIDER ================= -->
        <script>
            document.addEventListener("DOMContentLoaded", () => {
                const track = document.getElementById("sliderTrack");
                const slides = Array.from(track.children);
                const nextBtn = document.getElementById("nextSlide");
                const prevBtn = document.getElementById("prevSlide");
                const dotsNav = document.getElementById("sliderDots");

                let currentIndex = 0;
                let slideInterval;

                slides.forEach((_, index) => {
                    const dot = document.createElement("div");
                    dot.classList.add("dot");
                    if (index === 0) dot.classList.add("active");
                    dot.addEventListener("click", () => {
                        moveToSlide(index);
                        resetInterval();
                    });
                    dotsNav.appendChild(dot);
                });
                const dots = Array.from(dotsNav.children);

                const moveToSlide = (index) => {
                    track.style.transform = `translateX(-${index * 100}%)`;
                    dots.forEach((d) => d.classList.remove("active"));
                    dots[index].classList.add("active");
                    currentIndex = index;
                };

                nextBtn.addEventListener("click", () => {
                    const targetIndex = currentIndex === slides.length - 1 ? 0 : currentIndex + 1;
                    moveToSlide(targetIndex);
                    resetInterval();
                });

                prevBtn.addEventListener("click", () => {
                    const targetIndex = currentIndex === 0 ? slides.length - 1 : currentIndex - 1;
                    moveToSlide(targetIndex);
                    resetInterval();
                });

                const startInterval = () => {
                    slideInterval = setInterval(() => {
                        const targetIndex = currentIndex === slides.length - 1 ? 0 : currentIndex + 1;
                        moveToSlide(targetIndex);
                    }, 5000);
                };

                const resetInterval = () => {
                    clearInterval(slideInterval);
                    startInterval();
                };

                startInterval();
            });
        </script>
    </body>
</html>
```
