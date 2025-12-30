<!DOCTYPE html>
<html>
  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
  <body style="margin: 0px; overflow: hidden;">
    <a-scene embedded arjs>
      <assets>
        <video id="maVideo" src="votre-video.mp4" preload="auto" loop="true" crossorigin="anonymous"></video>
      </assets>

      <a-marker preset="hiro">
        <a-video src="#maVideo" width="1.6" height="0.9" position="0 0 0" rotation="-90 0 0"></a-video>
      </a-marker>

      <a-entity camera></a-entity>
    </a-scene>
    
    <script>
      // Forcer la lecture au toucher (contrainte navigateur)
      window.addEventListener('click', function () {
        document.querySelector('#maVideo').play();
      });
    </script>
  </body>
</html>
