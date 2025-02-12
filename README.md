# Webアプリ自動化フレームワーク (App Automation Framework)

## 📌 概要

本プロジェクトは、Excelデータを元にWebアプリを自動操作し、処理結果をメール通知する汎用的な自動化フレームワークです。特定のアプリに依存せず、設定を変更するだけで様々な業務に適用可能です。

---

## 🚀 特徴

- **Excelからデータを取得**（`openpyxl` 使用）
- **アプリケーションのウィンドウ操作**（`pywinauto` 使用）
- **Webフォームの自動入力**（`webbrowser` 使用）
- **メール通知機能**（`smtplib` 使用）
- **設定を `config.json` で管理し、他のアプリにも適用可能**

---

## 📂 フォルダ構成

```plaintext
📁 app-automation-framework
├── automation.py       # メインスクリプト
├── config.json         # 設定ファイル
├── requirements.txt    # 依存ライブラリ
└── README.md           # ドキュメント
```

---

## 🔧 必要な環境

- **Python**（[公式サイト](https://www.python.org/)からダウンロード）
- **依存ライブラリ**（`pip install -r requirements.txt` でインストール）

---

## 📌 インストール手順

1. **Pythonをインストール**
   - [公式サイト](https://www.python.org/)から最新版をダウンロード
2. **必要なライブラリをインストール**
   ```bash
   pip install -r requirements.txt
   ```
3. **`config.json` を編集して環境を設定**

---

## ⚙️ 設定 (`config.json`)

各環境に応じた設定を `config.json` で指定します。

```json
{
  "TARGET_APP_PATH": "C:/Program Files/YourApp/app.exe",
  "LOGIN_WINDOW_TITLE": "アプリ ログイン",
  "EXCEL_PATH": "./data.xlsx",
  "SHEET_NAME": "Sheet1",
  "FORM_URL": "https://yourform.com",
  "EMAIL_SENDER": "your_email@example.com",
  "EMAIL_PASSWORD": "your_password",
  "SMTP_SERVER": "smtp.example.com",
  "SMTP_PORT": 587
}
```

---

## 🛠️ 使い方

1. **Excelにデータを入力**
   - `data.xlsx` に処理対象の情報を入力
2. **スクリプトを実行**
   ```bash
   python automation.py
   ```
3. **自動処理の流れ**
   - ✅ Excelデータを取得
   - ✅ 指定のアプリを操作
   - ✅ Webフォーム送信 or メール通知

---

## 📨 メール通知機能

処理が完了すると、設定したメールアドレスに通知が送られます。

---

## 🏆 応用例

このスクリプトを改修することで、様々な業務の自動化に活用できます。

- **SaaSアプリのデータ入力自動化**
- **社内ツールの処理自動化**
- **大量のメール送信の自動化**

---

## 📌 ライセンス

[MIT License](LICENSE)
