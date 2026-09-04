# Digital Twin Surveillance

## Overview

Digital Twin Surveillance is a multi-camera computer-vision system for monitoring and visualizing a physical environment as a digital twin. It processes camera streams, detects and tracks objects, maps image coordinates to a 2D plane, and synchronizes world-state data for business logic and visualization.

This public repository is a showcase only. The private source code, model weights, operational data, and deployment configuration remain in the internal repository.

## Videos

GitHub does not render repository-hosted video files as inline players inside a README. Use the links below to open GitHub's video viewer in your browser:

- [Watch the 2D video](https://github.com/tienquocbao/digital-twin-surveillance/blob/master/video_2d.webm)
- [Watch the 3D video](https://github.com/tienquocbao/digital-twin-surveillance/blob/master/video3d.mp4)

## Main capabilities

- Multi-camera video synchronization.
- Object detection, pose estimation, and Re-identification.
- Camera calibration and homography-based 2D coordinate mapping.
- World-state tracking and realtime metadata transport.
- Backend business logic and digital-twin visualization integration.

## Conceptual architecture

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

## Technology

Python, PyTorch, Ultralytics YOLO, ONNX Runtime, TensorRT, Redis, WebSocket, and Docker Compose.

## Security

The public repository contains only documentation and two demonstration videos. It does not contain private source code, secrets, model weights, databases, logs, or original camera data.
