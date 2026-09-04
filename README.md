# Digital Twin Surveillance

## English

Digital Twin Surveillance is a multi-camera computer-vision system for monitoring and visualizing a physical environment as a digital twin. It processes camera streams, detects and tracks objects, maps image coordinates to a 2D plane, and synchronizes world-state data for business logic and visualization.

This public repository is a project showcase only. The private source code, model weights, operational data, and deployment configuration remain in the internal repository.

### Videos

#### 2D view

<video controls preload="metadata" width="100%" src="https://raw.githubusercontent.com/tienquocbao/digital-twin-surveillance/master/video_2d.webm"></video>

#### 3D view

<video controls preload="metadata" width="100%" src="https://raw.githubusercontent.com/tienquocbao/digital-twin-surveillance/master/video3d.mp4"></video>

If the embedded player is unavailable in your GitHub client, open [video_2d.webm](./video_2d.webm) or [video3d.mp4](./video3d.mp4).

### Main capabilities

- Multi-camera video synchronization.
- Object detection, pose estimation, and Re-identification.
- Camera calibration and homography-based 2D coordinate mapping.
- World-state tracking and realtime metadata transport.
- Backend business logic and digital-twin visualization integration.

### Conceptual architecture

```text
Camera / Video
      |
      v
AI perception: detection -> pose -> ReID
      |
      v
World state & coordinate mapping
      |
      +--> Backend business logic
      |
      +--> WebSocket / visualization client
```

### Technology

Python, PyTorch, Ultralytics YOLO, ONNX Runtime, TensorRT, Redis, WebSocket, and Docker Compose.

### Security note

The public repository intentionally contains only this README and two demonstration videos. It does not contain private source code, `.env` files, secrets, model weights, databases, logs, or original camera data.

## Tiếng Việt

Digital Twin Surveillance là hệ thống computer vision đa camera dùng để giám sát và trực quan hóa một không gian thực dưới dạng digital twin. Hệ thống xử lý luồng camera, phát hiện và theo dõi đối tượng, ánh xạ tọa độ ảnh sang mặt phẳng 2D, đồng bộ world state và cung cấp dữ liệu cho logic nghiệp vụ cũng như lớp hiển thị.

Repository public này chỉ dùng để giới thiệu dự án. Source code private, model weights, dữ liệu vận hành và cấu hình triển khai vẫn được giữ trong repository nội bộ.

### Video

- Video 2D được phát trực tiếp ở phần **2D view** phía trên.
- Video 3D được phát trực tiếp ở phần **3D view** phía trên.

### Chức năng chính

- Đồng bộ video từ nhiều camera.
- Phát hiện đối tượng, pose estimation và Re-identification.
- Hiệu chỉnh camera và ánh xạ tọa độ 2D bằng homography.
- Theo dõi world state và truyền metadata realtime.
- Kết nối backend nghiệp vụ với lớp hiển thị digital twin.

### Lưu ý bảo mật

Repository public chỉ chứa README và hai video demo. Source code private, file `.env`, secret, model weights, database, log và dữ liệu camera gốc không được công khai.
