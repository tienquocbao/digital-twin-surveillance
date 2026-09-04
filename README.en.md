# Digital Twin Surveillance

## Overview

Digital Twin Surveillance is a multi-camera computer-vision system for monitoring and visualizing a physical environment as a digital twin. It processes camera streams, detects and tracks objects, maps image coordinates to a 2D plane, and synchronizes world-state data for business logic and visualization.

This public repository is a showcase only. The private source code, model weights, operational data, and deployment configuration remain in the internal repository.

## Videos

GitHub's repository file view does not play these video files inline because of their size. Use the dedicated [video showcase page](https://tienquocbao.github.io/digital-twin-surveillance/) to watch both videos directly in the browser.

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
