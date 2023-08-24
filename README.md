<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Responsive Layout Example</title>
<style>
  * {
    box-sizing: border-box;
  }
  
  body {
    margin: 0;
    font-family: Arial, sans-serif;
  }
  
  .menu-title {
    text-align: center;
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
  }
  
  .section {
    border: 1px solid black;
    padding: 20px;
    margin-bottom: 20px;
  }
  
  .section-title {
    position: absolute;
    top: 10px;
    right: 10px;
    padding: 5px 10px;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
  }

  /* Desktop view */
  @media (min-width: 992px) {
    .container {
      display: flex;
      justify-content: space-between;
    }

    .section {
      width: calc(33.33% - 20px);
    }
  }

  /* Tablet view */
  @media (min-width: 768px) and (max-width: 991px) {
    .container {
      flex-direction: column;
    }

    .section {
      width: 100%;
    }

    .section:nth-child(3) {
      margin-top: 20px;
    }
  }

  /* Mobile view */
  @media (max-width: 767px) {
    .section {
      width: 100%;
    }

    .section-title {
      position: relative;
      top: 0;
      right: 0;
      width: 100%;
      text-align: center;
    }
  }
</style>
</head>
<body>
<div class="menu-title">Our Menu</div>
  <div class="container">
    <div class="section">
      <div class="section-title">Chicken</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commondo consequat.</p>
    </div>
    <div class="section">
      <div class="section-title">Beef</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commondo consequat.</p>
    </div>
    <div class="section">
      <div class="section-title">Sushi</div>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commondo consequat.</p>
    </div>
  </div>
</body>
</html>

