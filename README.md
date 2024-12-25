<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Camera Stream</title>
</head>
<body>
    <h1>Camera Stream from Phone</h1>
    <video id="video" width="640" height="480" autoplay></video>
    
    <script>
        async function startCamera() {
            try {
                // Mengakses kamera HP
                const stream = await navigator.mediaDevices.getUserMedia({ video: true });
                const videoElement = document.getElementById('video');
                videoElement.srcObject = stream;
            } catch (err) {
                console.error('Error accessing the camera: ', err);
            }
        }

        startCamera();
    </script>
</body>
</html>
# stream
