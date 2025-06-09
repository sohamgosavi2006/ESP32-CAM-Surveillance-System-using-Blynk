
DEMONSTRATION LINK -> 

This project transforms an ESP32-CAM into a WiFi-enabled smart surveillance system. It streams live video, detects and recognizes faces, and is fully controllable via the Blynk IoT app.

🔧 Features
🎥 1. Live Video Streaming
Real-time MJPEG video stream over HTTP.

Built-in compressed web interface (index_ov2640.html.gz) to view the feed from any browser.

Adjustable resolution and frame rate for performance tuning.

📸 2. Image Capture
Take snapshots via:

A browser (by hitting the /capture endpoint).

The Blynk app (using a virtual button).

Captured image is in JPEG format and can be viewed or saved directly.

🧠 3. Face Detection & Recognition
Detects faces in the camera feed using MTCNN.

Optional face recognition system to:

Greet known users: “Hello Subject [ID]”

Alert unknown users: “Intruder Alert!”

Allows enrolling up to 7 face IDs (each with 5 sample images).

🖼️ 4. Visual Feedback
Colored boxes around faces:

🟢 Green – recognized face

🔴 Red – unknown face

🟡 Yellow – detected face (not yet recognized)

On-screen text overlays show messages directly on the video stream.

📲 5. Blynk App Control
Control camera features remotely using the Blynk IoT platform:

Start/stop face detection or recognition.

Capture photos.

Adjust camera settings like brightness, quality, and resolution.

⚙️ 6. Customizable Camera Settings
Change settings in real-time:

Resolution (framesize)

Image quality

Brightness, contrast, saturation

Auto white balance (AWB), gain, exposure

📊 7. Performance Stats (Optional)
Serial monitor prints frame timing and FPS stats to help with debugging and optimization.

✅ Great for IoT beginners, hobbyists, or anyone looking to build a DIY smart camera.
