# OCPP Lite Energy – PowerMesh Edition

## Overview / 概要

This repository provides an open framework for lightweight and scalable energy control based on OCPP Lite, particularly optimized for use with smart meters and gateway-integrated devices.

本リポジトリは、スマートメーターとゲートウェイ一体型デバイスを活用した、OCPP Lite に基づく軽量かつ拡張可能なエネルギー制御のためのオープンフレームワークを提供します。

---

## Objectives / 目的

- Promote international adoption of **OCPP Lite** (JSON over MQTT)
- Facilitate open-source implementations suitable for embedded devices (e.g. ESP32, STM32)
- Demonstrate use cases with **Asuka Solutions’ smart meter system**
- Provide modular integration with **cloud platforms** (AWS IoT Core, etc.)

- **OCPP Lite（JSON over MQTT）** の国際普及を推進
- 組込みデバイス（ESP32、STM32 など）向けのオープンソース実装を支援
- **あすかソリューション製スマートメーター** を活用した導入事例の提示
- **クラウド連携（AWS IoT Core 等）** に対応した拡張設計

---

## Features / 主な特徴

- 📡 Lightweight OCPP over MQTT protocol stack
- 🧩 JSON Schema-based message validation
- 🌐 Modular architecture for cloud and local edge environments
- ⚙️ Includes sample code and MQTT topic structures

- 📡 軽量な MQTT ベースの OCPP Lite プロトコル実装
- 🧩 JSON スキーマによるメッセージバリデーション
- 🌐 クラウド／エッジ環境への柔軟なモジュール設計
- ⚙️ サンプルコードや MQTT トピック構成の提供

---

## Repository Structure / リポジトリ構成

| Directory | Description / 説明 |
|----------|---------------------|
| `docs/` | System diagrams and architecture / 構成図・設計書 |
| `json_schema/` | JSON schemas for OCPP messages / OCPP用スキーマ定義 |
| `samples/` | Example scripts for MQTT publishing / MQTT送信例コード |
| `aws/` | AWS IoT Core setup guide / AWS設定手順 |
| `reports/` | Pilot project reports / 実証実験レポート |

---

## Getting Started / はじめに

1. Clone this repository
2. Set up MQTT broker (e.g., Mosquitto)
3. Try the sample JSON messages via MQTT

1. 本リポジトリをクローンします  
2. MQTTブローカー（例：Mosquitto）を設定  
3. サンプルJSONメッセージを使って送信テスト

```bash
mosquitto_pub -h <broker> -t ocpp/boot -f json_schema/BootNotification.json

