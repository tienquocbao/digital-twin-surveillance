# Digital Twin Surveillance

Hệ thống digital twin cho giám sát không gian bằng computer vision đa camera. Hệ thống nhận hình ảnh/video từ camera, phát hiện và theo dõi đối tượng, ánh xạ vị trí từ mặt phẳng ảnh sang không gian 2D, sau đó đồng bộ trạng thái để phục vụ hiển thị và logic nghiệp vụ.

Đây là repository giới thiệu dự án. Source code, model weights, dữ liệu vận hành và cấu hình triển khai được giữ private trong repository nội bộ.

## Demo

- [Video demo 2D](./video_2d.webm)
- [Video demo 3D](./video3d.mp4)

Hai video minh họa các lớp hiển thị 2D và 3D của hệ thống digital twin.

## Tổng quan khả năng

- Phát hiện người/vật thể bằng mô hình computer vision.
- Pose estimation và Re-identification để duy trì identity giữa các frame/camera.
- Đồng bộ video nhiều camera.
- Hiệu chỉnh camera và homography để chuyển tọa độ pixel sang mặt phẳng 2D.
- Theo dõi world state và truyền metadata qua Redis/WebSocket.
- Kết nối backend nghiệp vụ và lớp hiển thị digital twin.

## Kiến trúc khái niệm

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

## Công nghệ chính

- Python
- PyTorch, Ultralytics YOLO, ONNX Runtime và TensorRT
- Redis cho state/message transport
- WebSocket cho giao tiếp realtime
- Docker Compose cho các service phụ trợ

## Lưu ý bảo mật

Repository này chỉ công khai tài liệu giới thiệu và video demo. Không đưa lên public repository các nội dung sau:

- Source code private.
- File `.env`, secret hoặc credential.
- Model weights và engine binaries.
- Database, log và dữ liệu camera gốc.

## Trạng thái

Dự án đang được phát triển nội bộ; video trong repository là bản minh họa cho năng lực xử lý hiện tại.
