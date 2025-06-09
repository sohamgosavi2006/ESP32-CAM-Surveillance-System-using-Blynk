
DEMONSTRATION LINK -> 

This project transforms an ESP32-CAM into a WiFi-enabled smart surveillance system. It streams live video, detects and recognizes faces, and is fully controllable via the Blynk IoT app and uses Arduino for development of features.

🔧 Features
🎥 1. Live Camera Feed
📡 HTTP MJPEG Video Streaming

Real-time low-latency video feed via ESP32's onboard HTTP server.

Accessible from local IP through any browser.

🌐 Compressed Web UI (index_ov2640.html.gz)

Clean interface to view the feed and control settings.

Fully embedded in firmware for fast load times.

📷 2. Image Capture
🖼️ On-Demand Snapshot

Captures image at /capture endpoint.

Outputs JPEG format with adjustable quality.

🧠 Capture via Blynk App

One-tap virtual button to trigger capture.

Can optionally send notification with image to Blynk.

🧠 3. Face Detection & Recognition
👁️ Real-Time Face Detection

Uses MTCNN to detect human faces in frame.

Detects multiple faces simultaneously.

🧑‍💼 Face Recognition

Compares detected faces against enrolled database.

If matched: ✅ “Hello Subject [ID]”

If unmatched: 🚨 “Intruder Alert!”

🧠 Face ID Enrollment Mode

Stores up to 7 unique faces.

Requires 5 sample images per face ID for accuracy.

Uses visual + serial feedback during enrollment.

🎨 4. Visual Overlays
🟥 🟩 Bounding Boxes

Red: Unrecognized face

Green: Matched face ID

Yellow: Generic detection

🖋️ On-Frame Text Feedback

Shows face ID or warning directly on video stream.

Rendered using fb_gfx drawing functions.

🎛️ 5. Adjustable Camera Settings
Easily tune camera performance from the Blynk app or web UI:

Setting	Description
framesize	Image resolution
quality	JPEG compression level
brightness	Brightness adjustment
contrast	Contrast balance
saturation	Color saturation
awb, agc	Auto white balance / gain control
gainceiling	Gain ceiling for light handling
colorbar	Enable test color bars

✅ Changes take effect in real-time.

📱 6. Blynk IoT Integration
📲 Remote Monitoring

Live status and control from mobile Blynk dashboard.

🕹️ Virtual Controls

Toggle face detection/recognition

Trigger snapshots

Adjust camera settings via sliders/switches

🔔 Optional Alerts

Add notifications when face is recognized or unknown person is detected.

⚙️ 7. Performance & Debugging
📈 FPS & Performance Stats

Console shows per-frame timing and FPS:

yaml
Copy
Edit
MJPG: 23545B 132ms (7.6fps), AVG: 143ms (6.9fps)
🧠 Rolling Average Filter

Smoothes out frame time variation.

🧰 8. Fail-Safe Handling
❌ Automatic 500 error response on:
Camera buffer failure
Image processing/memory issues
🛑 Frees all buffers after use to prevent crashes.

✅ Summary Table
Feature	Availability
Live Video Streaming	
Image Capture	
Face Detection	
Face Recognition	
Blynk App Integration	
Remote Camera Control	
Visual Feedback Overlays	
Web UI (Gzipped HTML)	
Error Recovery	



✅ Great for IoT beginners, hobbyists, or anyone looking to build a DIY smart camera.
