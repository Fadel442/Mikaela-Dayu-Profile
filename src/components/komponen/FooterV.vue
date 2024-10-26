<template>
    <footer class="footer">
      <div class="footer-content">
        <p>&copy; 2024 Mikaela Dayu. All rights reserved.</p>
      </div>
    </footer>
  </template>
  
  <style scoped>
  .footer {
    background-color: #FB9AD1;
    /* color: #fff; */
    text-align: center;
    padding: 20px 0;
    position: relative;
    bottom: 0;
    width: 100%;
  }
  
  .footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  
  .footer-links a:hover {
    text-decoration: underline;
  }
  p {
    color: white;
  }
  
  @media (max-width: 768px) {
    .footer-content {
      font-size: 15px;
    }
  }
  
  @media (max-width: 400px) {
    .footer-content {
      font-size: 10px;
    }
  }

  /* 480 */
  @media (max-width: 480px) {
    .footer-content {
      font-size: 15px;
    }
  }
  </style>