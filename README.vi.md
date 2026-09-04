# Digital Twin Surveillance

## Tổng quan

Digital Twin Surveillance là hệ thống computer vision đa camera dùng để giám sát và trực quan hóa một không gian thực dưới dạng digital twin. Hệ thống xử lý luồng camera, phát hiện và theo dõi đối tượng, ánh xạ tọa độ ảnh sang mặt phẳng 2D, đồng bộ world state và cung cấp dữ liệu cho logic nghiệp vụ cũng như lớp hiển thị.

Repository public này chỉ dùng để giới thiệu dự án. Source code private, model weights, dữ liệu vận hành và cấu hình triển khai vẫn được giữ trong repository nội bộ.

## Video

GitHub không hiển thị file video trong repository thành trình phát trực tiếp bên trong README. Dùng các link dưới đây để mở trình xem video của GitHub trên trình duyệt:

- [Xem video 2D](https://github.com/tienquocbao/digital-twin-surveillance/blob/master/video_2d.webm)
- [Xem video 3D](https://github.com/tienquocbao/digital-twin-surveillance/blob/master/video3d.mp4)

## Chức năng chính

- Đồng bộ video từ nhiều camera.
- Phát hiện đối tượng, pose estimation và Re-identification.
- Hiệu chỉnh camera và ánh xạ tọa độ 2D bằng homography.
- Theo dõi world state và truyền metadata realtime.
- Kết nối backend nghiệp vụ với lớp hiển thị digital twin.

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

## Công nghệ

Python, PyTorch, Ultralytics YOLO, ONNX Runtime, TensorRT, Redis, WebSocket và Docker Compose.

## Bảo mật

Repository public chỉ chứa tài liệu và hai video demo. Source code private, secret, model weights, database, log và dữ liệu camera gốc không được công khai.
