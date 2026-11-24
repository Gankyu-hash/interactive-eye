
<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>My Interactive Eye</title>

  <style>
    * {
      box-sizing: border-box;
    }

    html, body {
      width: 100%;
      height: 100%;
      margin: 0;
      background: transparent;
      overflow: hidden;
    }

    body {
      display: grid;
      place-items: center;
    }

    #eye {
      position: relative;
      width: min(86vw, 620px);
      aspect-ratio: 1 / 1;
      line-height: 0;
      overflow: hidden;

      -webkit-mask-image: url("eye-white.png");
      mask-image: url("eye-white.png");
      -webkit-mask-size: 100% 100%;
      mask-size: 100% 100%;
      -webkit-mask-repeat: no-repeat;
      mask-repeat: no-repeat;
    }

    #eye .layer {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: fill;
      pointer-events: none;
      user-select: none;
    }

    #eye .white {
      z-index: 1;
    }

    #eye .gaze {
      position: absolute;
      inset: 0;
      z-index: 2;
      transform: translate3d(0, 0, 0);
      will-change: transform;
      pointer-events: none;
    }

    #eye .gaze img {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: fill;
      pointer-events: none;
      user-select: none;
    }

    #eye .iris { z-index: 1; }
    #eye .pupil { z-index: 2; }

    @media (prefers-reduced-motion: reduce) {
      #eye .gaze {
        will-change: auto;
      }
    }
  </style>
</head>

<body>
  <div id="eye" aria-label="Interactive eye">
    <img class="layer white" src="eye-white.png" alt="">

    <div class="gaze" id="gaze">
      <img class="iris" src="iris.png" alt="">
      <img class="pupil" src="pupil.png" alt="">
    </div>
  </div>

  <script>
    const eye = document.querySelector("#eye");
    const gaze = document.querySelector("#gaze");

    // ===== 可调整参数 =====

    const MAX_X = 0.018;
    const MAX_Y = 0.018;

    // 数值越小，追踪越慢、越柔和
    const SMOOTHING = 0.075;

    // 鼠标离开时的回归速度
    const RETURN_SPEED = 0.045;

    // ======================

    let targetX = 0;
    let targetY = 0;

    let currentX = 0;
    let currentY = 0;

    let isHovering = false;

    function moveEye(event) {
      const rect = eye.getBoundingClientRect();

      const x = ((event.clientX - rect.left) / rect.width - 0.5) * 2;
      const y = ((event.clientY - rect.top) / rect.height - 0.5) * 2;

      const limitedX = Math.max(-1, Math.min(1, x));
      const limitedY = Math.max(-1, Math.min(1, y));

      targetX = limitedX * rect.width * MAX_X;
      targetY = limitedY * rect.height * MAX_Y;

      isHovering = true;
    }

    function resetEye() {
      targetX = 0;
      targetY = 0;
      isHovering = false;
    }

    function animate() {
      const speed = isHovering ? SMOOTHING : RETURN_SPEED;

      currentX += (targetX - currentX) * speed;
      currentY += (targetY - currentY) * speed;

      gaze.style.transform =
        `translate3d(${currentX}px, ${currentY}px, 0)`;

      requestAnimationFrame(animate);
    }

    eye.addEventListener("pointerenter", () => {
      isHovering = true;
    });

    eye.addEventListener("pointermove", moveEye);
    eye.addEventListener("pointerleave", resetEye);
    eye.addEventListener("pointerup", resetEye);
    eye.addEventListener("pointercancel", resetEye);

    animate();
  </script>
</body>
</html>
