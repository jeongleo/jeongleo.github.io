# Flight Controller Configuration

## Hardware
### Flight Controller (FC)
- Matek H743 WLITH
  > [제품 페이지](https://www.mateksys.com/?portfolio=h743-wlite#tab-id-4)

## Parameters
펌웨어는 Ardupilot Plane v4.5.7 사용

- Serial
  - SERIAL7_OPTION: 3
- OSD
  - MSP_OPTIONS: 4 (Enable BTFL Fonts)
  - OSD_TYPE: 5 (msp_displayport)
  - SERIAL5_PROTOCOL: 42 (displayport)
- Servo
  - SERVOn_FUNCTION: 적절한 핀을 원하는 기능에 맞게 설정
    혹은 Mission Planner 설정 항목에서도 설정 가능