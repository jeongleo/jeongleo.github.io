---
title: Build RC Airplane
layout: default
parent: RC Plane
nav_order: 1
---
<!-- 목차 --->
Contents

1. TOC
{:toc}

# Hardware
## Aircraft
알리발 Skysurfer 레플리카

## RC Transmitter and Receiver
Radiomaster Boxer Crush & Radiomaster ER6

## Telemetry
Holybro Sik Telemetry 915MHz 500mW

## Flight Controller
Matek H743 WLITE  
Firmware: Ardupilot Plane


## Video Transmission System
DJI O3 & DJI Goggle 3

## Head tracking

헤드 트래커는 아래의 오픈 소스를 사용하였다.

> Head Tracker v2.2  
> [https://headtracker.gitbook.io/head-tracker-v2.2](https://headtracker.gitbook.io/head-tracker-v2.2)


이 오픈소스는 Arduino Nano 33 BLE 보드를 기반으로 하는 헤드 트래커이다.  
보드에 내장된 IMU 센서로 현재 자세를 인식하고, PPM 신호를 출력한다.  
해당 신호를 조종기에서 Trainer mode로 읽은 후 기체로 조종 신호를 전송하는 방식이다.  

헤드트래커 하드웨어나 짐벌을 제품으로 파는 것도 있었지만, 가능한 직접 만들고자 하였다.

본인은 Arduino Nano 33 BLE Rev2 를 사용하였는데,  
하필 이 보드용 펌웨어에 문제가 있다고 한다.  
[https://github.com/dlktdr/HeadTracker/issues/178](https://github.com/dlktdr/HeadTracker/issues/178)

별도의 개발 버전을 사용하랜다.  
알려주는 펌웨어와 GUI를 다운받고 절차에 따라 수행하니 잘 된다.

