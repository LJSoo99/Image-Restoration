<img width="500" height="408" alt="22화면 캡처 2026-01-12 201616" src="https://github.com/user-attachments/assets/05a851e1-33e4-46df-b1b4-cac8fe45ff53" />

# Image-Restoration

## Overview
본 프로젝트는 **Wiener Filtering**을 이용하여  
블러 및 Gaussian noise가 포함된 영상을 주파수 영역에서 복원하는 과제입니다.

입력 영상(`deg.png`)은 주어진 blur kernel(`ker.png`)로 degrade된 후  
Gaussian noise가 추가된 영상이며,  
단순 inverse filtering을 적용할 경우 잡음이 과도하게 증폭되는 문제가 발생합니다.

본 과제에서는 **Wiener filtering**을 직접 구현하여  
책 표지의 제목을 식별할 수 있는 수준까지 영상을 복원하는 것을 목표로 합니다.

## Background
Degradation model은 다음과 같습니다.

G(u,v) = H(u,v)F(u,v) + N(u,v)

Inverse filtering은 H(u,v)가 작은 영역에서 noise가 크게 증폭되는 단점이 있습니다.  
이를 보완하기 위해 Wiener filtering을 적용합니다.

Wiener filter 식은 다음과 같습니다.
<img width="704" height="138" alt="화면 캡처 2026-01-12 202505" src="https://github.com/user-attachments/assets/3d15cb87-82cc-41b7-99e7-edf3cee4490f" />
여기서 K는 noise-to-signal ratio를 나타내는 상수입니다.

## Implementation Details

- Language: C++
- Library: OpenCV

