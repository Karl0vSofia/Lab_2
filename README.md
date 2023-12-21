# Lab_2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fortress in VR</title>
    <script src="https://threejs.org/build/three.js"></script>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
</head>
<body>
    <a-scene>
        <!-- Фортеця -->
        <a-entity position="0 1.5 -4">
             <a-cylinder height="4" radius="4" color="#c0c0c0"></a-cylinder>
<a-box position="0 1.5 -4" width="4" height="3" depth="4" color="gray"></a-box>
 <a-cylinder position="0 3 -4" radius="1" height="2" color="gray"></a-cylinder>
 <a-cone position="0 4 -4" radius-bottom="1.5" radius-top="0" height="1.5" color="gray"></a-cone>

        </a-entity>

        <!-- Прапор -->
        <a-entity position="0 3 -4" animation="property: rotation; to: 0 360 0; loop: true; dur: 5000">
            <a-plane width="2" height="1" color="red" text="value: Thank You Mario But Our Princess Is in Another Castle"></a-plane>
 <a-text value="Thank You Mario But Our Princess Is in Another Castle" color="white" wrap-count="25"></a-text>
        </a-entity>

        <!-- Анімація флагштоку -->
        <a-entity position="0 0 -4" animation="property: rotation; to: -90 0 0; loop: false; dur: 3000"></a-entity>

        <!-- Текстура фортеці -->
        <a-box position="0 1.5 -4" scale="4 3 4">
            <a-entity material="src: url(path/to/bricks-texture.jpg)" geometry="primitive: plane; width: 1; height: 1;"></a-entity>
        </a-box>
 <!-- Анімація прапора -->
      <a-animation attribute="rotation" dur="3000" to="0 360 0" repeat="indefinite"></a-animation>
      <!-- Анімація підняття прапора -->
      <a-animation attribute="position" dur="2000" to="0 6 0" repeat="1" direction="alternate" easing="ease-in-out" begin="flagAnimation"></a-animation>
    </a-nft>
  </a-scene>
        <!-- Камера та світло -->
        <a-entity camera position="0 1.6 0" look-controls></a-entity>
        <a-light type="ambient" intensity="0.5"></a-light>
    </a-scene>
</body>
</html>
