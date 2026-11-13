[gemini-code-1794547151999.html](https://github.com/user-attachments/files/34784984/gemini-code-1794547151999.html)
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>아이비테크 (IB TECH) - 공공기관 데스크탑 PC 전문</title>
  <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.8/dist/web/static/pretendard.css" />
  <style>
    :root {
      --bg-white: #FFFFFF;
      --text-black: #000000;
      --point-red: #CC0000;
      --gray-light: #F8F8F8;
      --border-line: #E0E0E0;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, sans-serif;
    }

    body {
      background-color: var(--bg-white);
      color: var(--text-black);
      line-height: 1.5;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* 최상단 공공조달 안내 바 */
    .top-bar {
      background-color: var(--text-black);
      color: var(--bg-white);
      font-size: 13px;
      padding: 10px 0;
    }

    .top-bar .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .top-badge {
      background-color: var(--point-red);
      color: var(--bg-white);
      padding: 3px 8px;
      font-weight: 700;
      margin-right: 8px;
    }

    /* 헤더 & 4대 간소화 카테고리 */
    .header {
      border-bottom: 2px solid var(--text-black);
      padding: 20px 0;
      position: sticky;
      top: 0;
      background-color: var(--bg-white);
      z-index: 100;
    }

    .header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 28px;
      font-weight: 900;
      letter-spacing: -1px;
      color: var(--text-black);
      text-decoration: none;
    }

    .logo span {
      color: var(--point-red);
    }

    .nav {
      display: flex;
      gap: 40px;
      list-style: none;
    }

    .nav li a {
      text-decoration: none;
      color: var(--text-black);
      font-size: 18px;
      font-weight: 800;
    }

    .nav li a:hover,
    .nav li a.active {
      color: var(--point-red);
    }

    .btn-quote {
      background-color: var(--point-red);
      color: var(--bg-white);
      padding: 12px 20px;
      font-size: 15px;
      font-weight: 800;
      border: none;
      cursor: pointer;
    }

    /* 메인 히어로 배너 */
    .hero {
      border-bottom: 1px solid var(--border-line);
      padding: 60px 0;
    }

    .hero .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 40px;
    }

    .hero-tag {
      display: inline-block;
      color: var(--point-red);
      font-weight: 800;
      font-size: 15px;
      margin-bottom: 12px;
      border-bottom: 2px solid var(--point-red);
      padding-bottom: 4px;
    }

    .hero-title {
      font-size: 40px;
      font-weight: 900;
      line-height: 1.25;
      margin-bottom: 16px;
    }

    .hero-title span {
      color: var(--point-red);
    }

    .hero-desc {
      font-size: 17px;
      font-weight: 500;
      margin-bottom: 28px;
    }

    .hero-btns {
      display: flex;
      gap: 12px;
    }

    .btn-primary {
      background-color: var(--point-red);
      color: var(--bg-white);
      padding: 16px 28px;
      font-size: 16px;
      font-weight: 800;
      border: none;
      cursor: pointer;
    }

    .btn-outline {
      background-color: var(--bg-white);
      color: var(--text-black);
      padding: 16px 28px;
      font-size: 16px;
      font-weight: 800;
      border: 2px solid var(--text-black);
      cursor: pointer;
    }

    .hero-box {
      width: 420px;
      min-height: 240px;
      border: 3px solid var(--text-black);
      background-color: var(--gray-light);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 24px;
      flex-shrink: 0;
    }

    /* 4대 간소화 카테고리 퀵 메뉴 */
    .quick-section {
      padding: 48px 0;
      border-bottom: 1px solid var(--border-line);
    }

    .quick-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
    }

    .quick-card {
      border: 2px solid var(--text-black);
      padding: 24px;
      background-color: var(--bg-white);
      cursor: pointer;
    }

    .quick-card.highlight,
    .quick-card:hover {
      border-color: var(--point-red);
    }

    .cat-num {
      font-size: 13px;
      font-weight: 800;
      color: var(--point-red);
      display: block;
      margin-bottom: 6px;
    }

    .quick-card h3 {
      font-size: 20px;
      font-weight: 900;
      margin-bottom: 6px;
    }

    .quick-card p {
      font-size: 14px;
      font-weight: 500;
    }

    /* 상품 목록 섹션 */
    .product-section {
      padding: 60px 0;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 28px;
      padding-bottom: 14px;
      border-bottom: 2px solid var(--text-black);
    }

    .section-title {
      font-size: 26px;
      font-weight: 900;
    }

    .section-title span {
      color: var(--point-red);
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
    }

    .product-card {
      border: 1px solid var(--border-line);
      padding: 20px;
      background-color: var(--bg-white);
    }

    .p-badge {
      display: inline-block;
      background-color: var(--text-black);
      color: var(--bg-white);
      font-size: 12px;
      font-weight: 700;
      padding: 4px 8px;
      margin-bottom: 12px;
    }

    .p-badge.red {
      background-color: var(--point-red);
    }

    .p-img {
      width: 100%;
      height: 170px;
      background-color: var(--gray-light);
      border: 1px solid var(--border-line);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      margin-bottom: 16px;
    }

    .p-title {
      font-size: 18px;
      font-weight: 800;
      margin-bottom: 10px;
    }

    .p-specs {
      list-style: none;
      font-size: 13px;
      line-height: 1.6;
      margin-bottom: 16px;
      padding: 12px;
      background-color: var(--gray-light);
    }

    .p-price-wrap {
      border-top: 1px solid var(--border-line);
      padding-top: 12px;
      margin-bottom: 14px;
    }

    .p-price-label {
      font-size: 12px;
      font-weight: 700;
    }

    .p-price {
      font-size: 22px;
      font-weight: 900;
      color: var(--point-red);
    }

    .p-actions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
    }

    .btn-sm-black {
      background-color: var(--text-black);
      color: var(--bg-white);
      border: none;
      padding: 10px 0;
      font-size: 13px;
      font-weight: 700;
      cursor: pointer;
    }

    .btn-sm-red {
      background-color: var(--point-red);
      color: var(--bg-white);
      border: none;
      padding: 10px 0;
      font-size: 13px;
      font-weight: 700;
      cursor: pointer;
    }

    /* 푸터 */
    .footer {
      border-top: 2px solid var(--text-black);
      padding: 40px 0;
      font-size: 14px;
      line-height: 1.8;
    }

    .footer
