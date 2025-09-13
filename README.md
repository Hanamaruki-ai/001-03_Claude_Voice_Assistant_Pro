[Claude Voice Assistant Pro -API入手式.html](https://github.com/user-attachments/files/22309704/Claude.Voice.Assistant.Pro.-API.html)[ClaudeVoicePro_with_Summary.html](https://github.com/user-attachments/files/22306278/ClaudeVoicePro_with_Summary.html)# 001-03_Claude_Voice_Assistant_Pro

信じられないかもしれませんが、このアプリは、AIに「話しかけただけ」で生まれました。
キーボード入力という苦痛から解放され、思考の流れを止めずにAIと対話する。そんな夢のような体験を、あなたも。

---

## ✨ 特長
### 🎙️ 音声入力でスムーズな対話

マイクに話しかけるだけで、瞬時にテキストを生成。頭に浮かんだアイデアや文章を、思考を途切れさせることなく書き起こせます。

### 🤖 AIとの対話革命

マイク入力を持たないAIとの会話を劇的に効率化します。 このアプリで音声からテキストを生成し、それをClaudeやQwenなどのAIにコピー＆ペーストするだけで、キーボード入力のストレスから完全に解放されます。

### 🎨 シンプルで直感的なUI

複雑な設定は一切不要。誰でも直感的に使い始められるよう、シンプルさを追求して設計されています。

📖 開発の裏側：AIとの共創ストーリー
このアプリは、プログラミング経験のない一人のユーザーが、「キーボードじゃなくて、話しかけられたら楽なのに」とAI（Claude）に話しかけたことがきっかけで誕生しました。
AIは、その一言を逃さず、自らコードを書き始め、対話を通じて完成へと導いてくれたのです。
この対話の全記録は、書籍**『AIに話しかけたらアプリができちゃった』**として、Kindleで出版されています。

---

## ➡️ 書籍はこちらから
### AIに話しかけたらアプリができちゃった ASIN: B0FNKPFMVD
https://amzn.to/3JsBgA1?tag=hanamaruki0aid-22

### I Talked to an AI, and It Built an App ASIN: B0FNKSJRSC
https://amzn.to/4oRH1HC?tag=Hanamaruki020


この作品は、人間とAIの新しい「共創」の形であり、誰でもAIと協力してアイデアを形にできる可能性を示しています。

---

### 📝 主な使用例
書籍・原稿執筆: PCでの作業に特化することで、膨大なテキストを効率的に扱えます。『書籍が書ける v1.2 Pro』のようなAIライティングツールと組み合わせることで、執筆作業を飛躍的に効率化できます。

アイデア出し・ブレインストーミング: 思考を言葉にするだけで、次々とアイデアを記録できます。

AIとの効率的なコミュニケーション: キーボード入力が苦手な方でも、ストレスなくAIと深く対話できます。

## 💻 動作環境
PC（Windows/Mac）での利用を推奨します。

マイクを搭載したPC

最新バージョンのWebブラウザ（Google Chrome、Microsoft Edgeなどを推奨）

## Demo

---

## 📥 ダウンロード
以下のリンクから、アプリのコード、ユーザーガイド、技術仕様書をまとめたZIPファイルをダウンロードできます。

### ➡️ アプリとドキュメントをまとめてダウンロード
[Docs.zip](https://github.com/user-attachments/files/22309643/Docs.zip)
* Claude Voice Assistant Pro -API入手式.html
　 アプリ本体
* Claude Voice Assistant Pro_ユーザーガイド.md
　  アプリ仕様書
* APIキー習得マニュアル/md
　  APIキーを取得して使うときのマニュアル
* Claude Voice Assistant Pro -API入手式.html.png
　 アプリのスクリーンショット
* Claude Voice Assistant Pro - 技術仕様書.md
　 アプリ技術仕様書
* 20250912_MIT License.txt
  ライセンス内容

### 使い方がわからない場合はファイルをAiに読み込ませて使い方を聞いてみてください。

---

## 📄 ドキュメント内容
以下の内容を参考に、アプリの詳細を確認できます。

## 1. アプリ本体のコード (Claude Voice Assistant Pro -API入手式.html)
[Uploading Claude Voice Assistant Pro -API入手
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Claude Voice Assistant Pro</title>
    <style>
        /* 全体的なリセットと基本設定 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            overflow-x: hidden;
        }
        
        /* コンテナ */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* ヘッダーセクション */
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5em;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #666;
            font-size: 1.1em;
        }
        
        /* メインコンテンツレイアウト */
        .main-content {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        /* 音声パネル */
        .voice-panel {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        /* 音声コントロールボタン群 */
        .voice-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 20px;
            flex-wrap: wrap;
            align-items: center;
        }
        
        .voice-btn {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: none;
            cursor: pointer;
            font-size: 28px;
            transition: all 0.3s ease;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .voice-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }
        
        /* マイクボタンのスタイル */
        .mic-btn {
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white;
        }
        
        .mic-btn.listening {
            background: linear-gradient(45deg, #f44336, #da190b);
            animation: pulse 1.5s infinite;
        }
        
        /* その他のボタンのスタイル */
        .stop-btn {
            background: linear-gradient(45deg, #f44336, #da190b);
            color: white;
        }
        
        .copy-btn {
            background: linear-gradient(45deg, #2196F3, #1976D2);
            color: white;
        }
        
        .clear-btn {
            background: linear-gradient(45deg, #ff9800, #f57c00);
            color: white;
        }
        
        .save-btn {
            background: linear-gradient(45deg, #9c27b0, #7b1fa2);
            color: white;
        }

        /* ダウンロードボタンのスタイル */
        .download-btn {
            background: linear-gradient(45deg, #42a5f5, #1e88e5); /* 青系のグラデーション */
            color: white;
        }
        
        .voice-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none !important;
        }
        
        /* ステータス表示 */
        .status-display {
            background: linear-gradient(45deg, #f8f9fa, #e9ecef);
            border-radius: 15px;
            padding: 15px;
            margin-bottom: 20px;
            text-align: center;
            font-weight: bold;
            color: #495057;
        }
        
        .status-display.listening {
            background: linear-gradient(45deg, #d4edda, #c3e6cb);
            color: #155724;
            border: 2px solid #28a745;
        }
        
        .status-display.error {
            background: linear-gradient(45deg, #f8d7da, #f5c6cb);
            color: #721c24;
            border: 2px solid #dc3545;
        }
        
        /* テキストエリアコンテナ */
        .textarea-container {
            position: relative;
        }
        
        textarea {
            width: 100%;
            height: 300px;
            padding: 20px;
            border: 2px solid #e0e0e0;
            border-radius: 15px;
            font-size: 16px;
            line-height: 1.6;
            resize: vertical;
            font-family: inherit;
            background: #fafafa;
            transition: all 0.3s ease;
        }
        
        textarea:focus {
            outline: none;
            border-color: #667eea;
            background: white;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }
        
        /* テキストエリアツールボタン */
        .textarea-tools {
            position: absolute;
            bottom: 10px;
            right: 10px;
            display: flex;
            gap: 10px;
        }
        
        .tool-btn {
            background: rgba(255, 255, 255, 0.9);
            border: none;
            border-radius: 20px;
            padding: 8px 12px;
            font-size: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }
        
        .tool-btn:hover {
            background: white;
            transform: translateY(-1px);
        }
        
        /* サイドバーレイアウト */
        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        /* 設定パネル（details要素として再定義） */
        .settings-panel details {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .settings-panel summary {
            font-size: 1.5em; /* h3のサイズに合わせる */
            font-weight: bold;
            color: #333;
            cursor: pointer;
            margin-bottom: 15px;
            list-style: none; /* デフォルトのマーカーを非表示に */
            display: flex;
            align-items: center;
        }

        .settings-panel summary::before {
            content: '⚙️ '; /* 歯車アイコン */
            margin-right: 10px;
        }

        .settings-panel details[open] summary {
            margin-bottom: 20px; /* 開いたときにコンテンツとの間にスペース */
        }
        
        .setting-item {
            margin-bottom: 15px;
        }
        
        .setting-item label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
            color: #555;
        }
        
        .setting-item select,
        .setting-item input[type="checkbox"] {
            width: auto; /* チェックボックスの幅を自動調整 */
            margin-right: 8px; /* チェックボックスとラベルの間にスペース */
        }

        .setting-item input[type="text"],
        .setting-item input[type="password"], /* 追加 */
        .setting-item select {
            width: 100%;
            padding: 8px 12px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s ease;
        }
        
        .setting-item select:focus,
        .setting-item input[type="text"]:focus,
        .setting-item input[type="password"]:focus { /* 追加 */
            outline: none;
            border-color: #667eea;
        }

        .setting-item.checkbox-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .setting-item.checkbox-item label {
            margin-bottom: 0;
        }

        /* ファイル形式選択のスタイル */
        .download-format-options {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin-top: 10px;
        }
        .download-format-options label {
            display: flex;
            align-items: center;
            margin-bottom: 0; /* 親要素のmargin-bottomがあるのでリセット */
            font-weight: normal;
        }
        .download-format-options input[type="checkbox"] {
            margin-right: 8px;
        }

        /* リセットボタンのスタイル */
        .reset-button {
            background: linear-gradient(45deg, #ef5350, #d32f2f); /* 赤系のグラデーション */
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 15px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9em;
            width: 100%;
            margin-top: 10px;
        }
        .reset-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        .reset-group {
            margin-top: 20px;
            border-top: 1px solid #eee;
            padding-top: 15px;
        }
        
        /* テンプレートパネル */
        .templates-panel {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .template-item {
            background: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .template-item:hover {
            background: #e9ecef;
            transform: translateY(-1px);
        }
        
        .template-item h4 {
            margin-bottom: 5px;
            color: #333;
            font-size: 14px;
        }
        
        .template-item p {
            font-size: 12px;
            color: #666;
            margin: 0;
        }
        
        /* 履歴パネル */
        .history-panel {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-height: 300px; /* スクロール可能にする */
            overflow-y: auto;
        }
        
        .history-item {
            background: #f8f9fa;
            border: 1px solid #e9ecef; /* 履歴アイテムのボーダーを追加 */
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-left: 4px solid #667eea;
        }
        
        .history-item:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }
        
        .history-item-date {
            font-size: 11px;
            color: #666;
            margin-bottom: 5px;
        }
        
        .history-item-text {
            font-size: 13px;
            color: #333;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap; /* 1行で表示 */
        }
        
        /* 統計パネル */
        .stats-panel {
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 20px;
            padding: 20px;
            color: white;
            text-align: center;
        }
        
        .stats-item {
            margin-bottom: 15px;
        }
        
        .stats-number {
            font-size: 2em;
            font-weight: bold;
            display: block;
        }
        
        .stats-label {
            font-size: 0.9em;
            opacity: 0.8;
        }
        
        /* 文字数・単語数表示 */
        .word-count {
            text-align: right;
            color: #666;
            margin-top: 10px;
            font-size: 14px;
        }
        
        /* アニメーション */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* レスポンシブデザイン */
        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr; /* 1列レイアウトに変更 */
            }
            
            .voice-controls {
                gap: 10px;
            }
            
            .voice-btn {
                width: 60px;
                height: 60px;
                font-size: 24px;
            }
            
            .header h1 {
                font-size: 2em;
            }
        }

        /* マイクガイドモーダル */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            max-width: 500px;
            text-align: center;
            transform: translateY(-20px);
            transition: transform 0.3s ease;
        }

        .modal-overlay.active .modal-content {
            transform: translateY(0);
        }

        .modal-content h3 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.8em;
        }

        .modal-content p {
            margin-bottom: 15px;
            line-height: 1.6;
            color: #555;
        }

        .modal-content ul {
            list-style: none;
            padding: 0;
            margin-bottom: 20px;
            text-align: left;
            color: #666;
        }

        .modal-content ul li {
            margin-bottom: 10px;
            padding-left: 0; /* チェックマークを削除したのでパディングも不要 */
            position: relative;
        }

        /* チェックマークを削除 */
        .modal-content ul li::before {
            content: none; 
        }

        .modal-close-btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            border: none;
            border-radius: 25px;
            padding: 12px 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1.1em;
        }

        .modal-close-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎤 Claude Voice Assistant Pro</h1>
            <p>音声入力でClaude活用を最大化！プロ仕様の音声認識アシスタント</p>
        </div>
        
        <div class="main-content">
            <div class="voice-panel">
                <div class="status-display" id="statusDisplay">
                    準備完了 - マイクボタンを押して開始
                </div>
                
                <div class="voice-controls">
                    <button class="voice-btn mic-btn" id="micBtn" title="音声入力開始">
                        🎤
                    </button>
                    <button class="voice-btn stop-btn" id="stopBtn" title="録音停止" disabled>
                        ⏹️
                    </button>
                    <button class="voice-btn copy-btn" id="copyBtn" title="クリップボードにコピー">
                        📋
                    </button>
                    <button class="voice-btn clear-btn" id="clearBtn" title="テキストクリア">
                        🗑️
                    </button>
                    <button class="voice-btn save-btn" id="saveBtn" title="履歴に保存">
                        💾
                    </button>
                    <button class="voice-btn download-btn" id="downloadBtn" title="テキストをダウンロード">
                        ⬇️
                    </button>
                </div>
                
                <div class="textarea-container">
                    <textarea id="textOutput" placeholder="音声で入力されたテキストがここに表示されます。

🎯 Claude活用のコツ：
• 「〜について詳しく教えて」
• 「〜を分かりやすく説明して」
• 「〜のメリットとデメリットは？」
• 「〜を要約して」

右側のテンプレートも活用してください！"></textarea>
<!-- 要約ボタン -->
<div class="summary-container" style="text-align: right; margin-top: 10px;">
  <button id="summarizeBtn" class="tool-btn">🧠 要約する</button>
</div>

                    <div class="textarea-tools">
                        <button class="tool-btn" id="undoBtn">↶ 元に戻す</button>
                        <button class="tool-btn" id="redoBtn">↷ やり直し</button>
                    </div>
                </div>
                
                <div class="word-count">
                    文字数: <span id="charCount">0</span> | 単語数: <span id="wordCount">0</span>
                </div>
            </div>
            
            <div class="sidebar">
                <div class="settings-panel">
                    <details open> <!-- open属性でデフォルトで開く -->
                        <summary>設定</summary>
                        <div class="setting-item">
                            <label for="openaiApiKey">OpenAI APIキー</label>
                            <input type="password" id="openaiApiKey" placeholder="sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx">
                            <p style="font-size: 0.8em; color: #888; margin-top: 5px;">
                                ※個人で取得したAPIキーを入力してください。<br>
                                OpenAIアカウント: <a href="https://platform.openai.com/api-keys" target="_blank" rel="noopener noreferrer">platform.openai.com/api-keys</a>
                            </p>
                        </div>
                        <div class="setting-item">
                            <label for="language">言語</label>
                            <select id="language">
                                <option value="ja-JP">🇯🇵 日本語</option>
                                <option value="en-US">🇺🇸 English</option>
                                <option value="en-GB">🇬🇧 English (UK)</option>
                                <option value="zh-CN">🇨  中文</option>
                                <option value="ko-KR">🇰🇷 한국어</option>
                            </select>
                        </div>
                        <div class="setting-item checkbox-item">
                            <label for="autoSave">自動保存</label>
                            <input type="checkbox" id="autoSave" checked>
                        </div>
                        <div class="setting-item checkbox-item">
                            <label for="showMicrophoneGuide">マイク設定ガイドを表示</label>
                            <input type="checkbox" id="showMicrophoneGuide" checked>
                        </div>
                        <div class="setting-item">
                            <label for="theme">テーマ</label>
                            <select id="theme">
                                <option value="default">デフォルト</option>
                                <option value="dark">ダーク</option>
                                <option value="minimal">ミニマル</option>
                            </select>
                        </div>

                        <div class="setting-item">
                            <label>ダウンロード形式</label>
                            <div class="download-format-options" id="downloadFormatOptions">
                                <label><input type="checkbox" id="downloadFormat_txt" value="txt" data-mime-type="text/plain;charset=utf-8" data-extension="txt" checked> 📄 テキスト (.txt)</label>
                                <label><input type="checkbox" id="downloadFormat_md" value="md" data-mime-type="text/markdown;charset=utf-8" data-extension="md"> 📝 マークダウン (.md)</label>
                                <label><input type="checkbox" id="downloadFormat_html" value="html" data-mime-type="text/html;charset=utf-8" data-extension="html"> 🌐 HTML (.html)</label>
                                <label><input type="checkbox" id="downloadFormat_json" value="json" data-mime-type="application/json;charset=utf-8" data-extension="json"> 💻 JSON (.json)</label>
                                <label><input type="checkbox" id="downloadFormat_csv" value="csv" data-mime-type="text/csv;charset=utf-8" data-extension="csv"> 📊 CSV (.csv)</label>
                            </div>
                        </div>

                        <div class="reset-group">
                            <button class="reset-button" id="resetHistoryBtn">📚 履歴をリセット</button>
                            <button class="reset-button" id="resetStatsBtn">📊 統計をリセット</button>
                        </div>
                    </details>
                </div>
                
                <div class="templates-panel">
                    <h3>📝 テンプレート</h3>
                    <div class="template-item" data-template="について詳しく教えてください。特に以下の点を含めて説明してください：">
                        <h4>詳細説明</h4>
                        <p>トピックについて詳しく説明してもらう</p>
                    </div>
                    <div class="template-item" data-template="を分かりやすく要約してください。要点を箇条書きで教えてください：">
                        <h4>要約・整理</h4>
                        <p>内容を整理して要約してもらう</p>
                    </div>
                    <div class="template-item" data-template="のメリットとデメリットを教えてください。比較表があると助かります：">
                        <h4>比較分析</h4>
                        <p>メリット・デメリットを比較分析</p>
                    </div>
                    <div class="template-item" data-template="について初心者にも分かるように説明してください。具体例も含めて：">
                        <h4>初心者向け</h4>
                        <p>専門用語を使わず分かりやすく説明</p>
                    </div>
                </div>
                
                <div class="history-panel">
                    <h3>📚 履歴</h3>
                    <div id="historyList">
                        <!-- 履歴がここに表示されます -->
                    </div>
                </div>
                
                <div class="stats-panel">
                    <h3>📊 統計</h3>
                    <div class="stats-item">
                        <span class="stats-number" id="totalSessions">0</span>
                        <span class="stats-label">セッション数</span>
                    </div>
                    <div class="stats-item">
                        <span class="stats-number" id="totalWords">0</span>
                        <span class="stats-label">総単語数</span>
                    </div>
                    <div class="stats-item">
                        <span class="stats-number" id="totalTime">0</span>
                        <span class="stats-label">総利用時間(分)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- マイクガイドモーダル -->
    <div class="modal-overlay" id="microphoneGuideModal">
        <div class="modal-content">
            <h3>マイク設定のお願い</h3>
            <p>このアプリは音声入力を使用します。マイクが有効になっていない場合、以下の手順で設定をご確認ください。</p>
            <ul>
                <li>ブラウザのアドレスバーに表示されるマイクアイコン（または南京錠アイコン）をクリックしてください。</li>
                <li>「マイクへのアクセス」または「サイトの設定」で、このサイトのマイク使用を「許可」に設定してください。</li>
                <li>もしブラウザの設定で許可できない場合は、お使いのOS（Windows/macOS/Android/iOS）のシステム設定でブラウザアプリのマイクアクセスを許可してください。</li>
            </ul>
            <button class="modal-close-btn" id="closeMicrophoneGuideModal">OK、理解しました</button>
        </div>
    </div>

    <script>
        class VoiceAssistantPro {
            constructor() {
                this.recognition = null;
                this.isListening = false;
                this.finalTranscript = '';
                this.undoStack = [];
                this.redoStack = [];
                this.sessionStartTime = null;
                this.stats = this.loadStats();
                this.history = this.loadHistory();
                this.showMicrophoneGuideOnStartup = this.loadMicrophoneGuideSetting(); // マイクガイド設定をロード
                this.hasRequestedMicrophonePermission = false; // マイク許可を一度でも要求したかどうかのフラグ
                this.downloadFormats = this.loadDownloadFormatSettings(); // ダウンロード形式設定をロード
                this.openaiApiKey = this.loadOpenAIApiKey(); // OpenAI APIキーをロード

                this.initElements();
                this.initSpeechRecognition();
                this.bindEvents();
                this.updateCharCount();
                this.updateStats();
                this.loadHistoryDisplay();
                this.applyDownloadFormatSettings(); // ダウンロード形式設定を適用
                this.checkMicrophonePermissionAndShowGuide(); // マイク許可をチェックし、必要ならガイドを表示

                // 初期ロード時にAPIキー入力欄に値を設定
                if (this.openaiApiKeyInput) {
                    this.openaiApiKeyInput.value = this.openaiApiKey;
                }
            }
            
            initElements() {
                this.micBtn = document.getElementById('micBtn');
                this.stopBtn = document.getElementById('stopBtn');
                this.copyBtn = document.getElementById('copyBtn');
                this.clearBtn = document.getElementById('clearBtn');
                this.saveBtn = document.getElementById('saveBtn');
                this.downloadBtn = document.getElementById('downloadBtn');
                this.downloadFormatCheckboxes = document.querySelectorAll('#downloadFormatOptions input[type="checkbox"]'); // 変更
                this.undoBtn = document.getElementById('undoBtn');
                this.redoBtn = document.getElementById('redoBtn');
                this.summarizeBtn = document.getElementById('summarizeBtn'); // 追加

                this.statusDisplay = document.getElementById('statusDisplay');
                this.textOutput = document.getElementById('textOutput');
                this.languageSelect = document.getElementById('language');
                this.charCount = document.getElementById('charCount');
                this.wordCount = document.getElementById('wordCount');
                
                this.totalSessions = document.getElementById('totalSessions');
                this.totalWords = document.getElementById('totalWords');
                this.totalTime = document.getElementById('totalTime');
                this.historyList = document.getElementById('historyList');
                
                this.templateItems = document.querySelectorAll('.template-item');

                // 新しいリセットボタン
                this.resetHistoryBtn = document.getElementById('resetHistoryBtn');
                this.resetStatsBtn = document.getElementById('resetStatsBtn');

                // マイクガイドモーダル関連要素
                this.microphoneGuideModal = document.getElementById('microphoneGuideModal');
                this.closeMicrophoneGuideModalBtn = document.getElementById('closeMicrophoneGuideModal');
                this.showMicrophoneGuideCheckbox = document.getElementById('showMicrophoneGuide');

                // OpenAI APIキー入力欄
                this.openaiApiKeyInput = document.getElementById('openaiApiKey'); // 追加

                // チェックボックスの初期状態を設定
                this.showMicrophoneGuideCheckbox.checked = this.showMicrophoneGuideOnStartup;
            }
            
            initSpeechRecognition() {
                // ブラウザが音声認識APIをサポートしているか確認
                if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) {
                    this.updateStatus('音声認識非対応ブラウザです', 'error');
                    this.micBtn.disabled = true;
                    return;
                }
                
                // SpeechRecognitionオブジェクトの初期化
                const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
                this.recognition = new SpeechRecognition();
                
                // 継続的な認識と中間結果の取得を有効にする
                this.recognition.continuous = true;
                this.recognition.interimResults = true;
                // 選択された言語を設定
                this.recognition.lang = this.languageSelect.value;
                
                // 認識開始時のイベントハンドラ
                this.recognition.onstart = () => {
                    this.isListening = true;
                    this.sessionStartTime = Date.now(); // セッション開始時間を記録
                    this.micBtn.classList.add('listening'); // マイクボタンにリスニング中のスタイルを適用
                    this.micBtn.disabled = true; // マイクボタンを無効化
                    this.stopBtn.disabled = false; // 停止ボタンを有効化
                    this.updateStatus('聞いています... 話してください', 'listening');
                };
                
                // 認識結果が得られた時のイベントハンドラ
                this.recognition.onresult = (event) => {
                    let interimTranscript = ''; // 中間結果を格納する変数
                    
                    // すべての認識結果をループ
                    for (let i = event.resultIndex; i < event.results.length; i++) {
                        const transcript = event.results[i][0].transcript;
                        
                        // 最終結果と中間結果を分離
                        if (event.results[i].isFinal) {
                            this.finalTranscript += transcript + ' '; // 最終結果に追加
                        } else {
                            interimTranscript += transcript; // 中間結果に追加
                        }
                    }
                    
                    // テキストエリアに最終結果と中間結果を表示
                    this.textOutput.value = this.finalTranscript + interimTranscript;
                    this.updateCharCount(); // 文字数・単語数を更新
                };
                
                // エラー発生時のイベントハンドラ
                this.recognition.onerror = (event) => {
                    console.error('音声認識エラー:', event.error);
                    this.updateStatus(`エラー: ${event.error}`, 'error');
                    this.resetButtons(); // ボタンの状態をリセット

                    // マイク許可エラーの場合、ガイドを表示
                    if (event.error === 'not-allowed' || event.error === 'permission-denied') {
                        this.showMicrophoneGuideModal();
                    }
                };
                
                // 認識終了時のイベントハンドラ
                this.recognition.onend = () => {
                    this.isListening = false;
                    this.updateSessionStats(); // セッション統計を更新
                    
                    // マイク許可が既に要求されており、かつガイド表示設定がONの場合に補足メッセージを追加
                    if (this.hasRequestedMicrophonePermission && this.showMicrophoneGuideOnStartup) {
                        this.updateStatus('認識完了 - 再度開始するにはマイクボタンを押してください。※ブラウザの仕様により、再度許可を求められる場合があります。');
                    } else {
                        this.updateStatus('認識完了 - 再度開始するにはマイクボタンを押してください');
                    }
                    this.resetButtons(); // ボタンの状態をリセット
                };
            }
            
            // イベントリスナーのバインド
            bindEvents() {
                this.micBtn.addEventListener('click', () => this.startRecognition());
                this.stopBtn.addEventListener('click', () => this.stopRecognition());
                this.copyBtn.addEventListener('click', () => this.copyText());
                this.clearBtn.addEventListener('click', () => this.clearText());
                this.saveBtn.addEventListener('click', () => this.saveToHistory());
                this.downloadBtn.addEventListener('click', () => this.downloadTextsInSelectedFormats()); // 変更
                this.undoBtn.addEventListener('click', () => this.undo());
                this.redoBtn.addEventListener('click', () => this.redo());
                this.summarizeBtn.addEventListener('click', () => this.summarizeText()); // 追加
                
                // ダウンロード形式チェックボックスの変更イベント
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    checkbox.addEventListener('change', () => this.saveDownloadFormatSettings());
                });

                // リセットボタンのイベント
                this.resetHistoryBtn.addEventListener('click', () => this.resetHistory());
                this.resetStatsBtn.addEventListener('click', () => this.resetStats());
                
                // 言語選択が変更されたら認識言語を更新
                this.languageSelect.addEventListener('change', () => {
                    if (this.recognition) {
                        this.recognition.lang = this.languageSelect.value;
                    }
                });
                
                // テキストエリアの入力時にアンドゥスタックを更新し、文字数・単語数を更新
                this.textOutput.addEventListener('input', () => {
                    this.saveToUndoStack();
                    this.updateCharCount();
                });
                
                // テンプレートアイテムのクリックイベント
                this.templateItems.forEach(item => {
                    item.addEventListener('click', () => {
                        const template = item.dataset.template;
                        this.insertTemplate(template);
                    });
                });
                
                // マイクガイドモーダルの閉じるボタン
                this.closeMicrophoneGuideModalBtn.addEventListener('click', () => {
                    this.hideMicrophoneGuideModal();
                });

                // マイクガイド表示設定の変更
                this.showMicrophoneGuideCheckbox.addEventListener('change', (e) => {
                    this.showMicrophoneGuideOnStartup = e.target.checked;
                    this.saveMicrophoneGuideSetting();
                });

                // OpenAI APIキー入力欄の変更イベントリスナーを追加
                this.openaiApiKeyInput.addEventListener('input', (e) => {
                    this.openaiApiKey = e.target.value.trim();
                    this.saveOpenAIApiKey(this.openaiApiKey);
                    this.updateStatus('APIキーを更新しました。');
                });

                // キーボードショートカット
                document.addEventListener('keydown', (e) => {
                    if (e.ctrlKey || e.metaKey) { // CtrlキーまたはCmdキーが押されている場合
                        switch(e.key) {
                            case 'm': // Ctrl/Cmd + M で録音開始/停止
                                e.preventDefault();
                                if (!this.isListening) {
                                    this.startRecognition();
                                } else {
                                    this.stopRecognition();
                                }
                                break;
                            case 'z': // Ctrl/Cmd + Z で元に戻す, Ctrl/Cmd + Shift + Z でやり直し
                                if (e.shiftKey) {
                                    e.preventDefault();
                                    this.redo();
                                } else {
                                    e.preventDefault();
                                    this.undo();
                                }
                                break;
                            case 's': // Ctrl/Cmd + S で履歴に保存
                                e.preventDefault();
                                this.saveToHistory();
                                break;
                            case 'd': // Ctrl/Cmd + D でダウンロード
                                e.preventDefault();
                                this.downloadTextsInSelectedFormats();
                                break;
                            case 'y': // Ctrl/Cmd + Y で要約
                                e.preventDefault();
                                this.summarizeText();
                                break;
                        }
                    }
                });
            }
            
            // 音声認識を開始
            startRecognition() {
                if (!this.recognition) return;
                
                this.saveToUndoStack(); // 現在のテキストをアンドゥスタックに保存
                
                try {
                    this.recognition.start();
                } catch (error) {
                    console.error('録音開始エラー:', error);
                    this.updateStatus('録音開始に失敗しました', 'error');
                    // エラーがマイク許可関連の場合、ガイドを表示
                    if (error.name === 'NotAllowedError' || error.name === 'PermissionDeniedError') {
                        this.showMicrophoneGuideModal();
                    }
                }
            }
            
            // 音声認識を停止
            stopRecognition() {
                if (this.recognition && this.isListening) {
                    this.recognition.stop();
                }
            }
            
            // テキストエリアの内容をクリア
            clearText() {
                this.saveToUndoStack(); // クリア前のテキストをアンドゥスタックに保存
                this.textOutput.value = '';
                this.finalTranscript = '';
                this.updateCharCount();
                this.updateStatus('テキストをクリアしました');
            }
            
            // テキストをクリップボードにコピー
            async copyText() {
                const text = this.textOutput.value;
                if (!text.trim()) {
                    this.updateStatus('コピーするテキストがありません', 'error');
                    return;
                }
                
                try {
                    await navigator.clipboard.writeText(text);
                    this.updateStatus('クリップボードにコピーしました！');
                } catch (error) {
                    console.error('コピーエラー:', error);
                    this.textOutput.select();
                    this.updateStatus('テキストを選択しました（手動でコピーしてください）', 'error');
                }
            }

            // ダウンロード形式に応じたテキスト生成とMIMEタイプ・拡張子の取得
            getFormattedDownloadData(originalText, format) {
                let content = originalText;
                let mimeType = '';
                let extension = '';

                switch (format) {
                    case 'txt':
                        mimeType = 'text/plain;charset=utf-8';
                        extension = 'txt';
                        break;
                    case 'md':
                        mimeType = 'text/markdown;charset=utf-8';
                        extension = 'md';
                        break;
                    case 'html':
                        const escapedText = originalText.replace(/&/g, '&amp;')
                                                      .replace(/</g, '&lt;')
                                                      .replace(/>/g, '&gt;')
                                                      .replace(/"/g, '&quot;')
                                                      .replace(/'/g, '&#039;');
                        content = `<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Claude Voice Assistant Output</title>
</head>
<body>
    <pre>${escapedText}</pre>
</body>
</html>`;
                        mimeType = 'text/html;charset=utf-8';
                        extension = 'html';
                        break;
                    case 'json':
                        content = JSON.stringify({
                            title: `Claude Voice Assistant Output`,
                            content: originalText,
                            timestamp: new Date().toISOString()
                        }, null, 2); // 2スペースインデントで整形
                        mimeType = 'application/json;charset=utf-8';
                        extension = 'json';
                        break;
                    case 'csv':
                        const csvEscapedText = originalText.replace(/"/g, '""');
                        content = `"${csvEscapedText}"`; // 全体を1つのセルとして保存
                        mimeType = 'text/csv;charset=utf-8';
                        extension = 'csv';
                        break;
                    default:
                        mimeType = 'text/plain;charset=utf-8';
                        extension = 'txt';
                        break;
                }
                return { content, mimeType, extension };
            }

            // 選択された全ての形式でテキストをダウンロード
            downloadTextsInSelectedFormats() {
                const originalText = this.textOutput.value;
                if (!originalText.trim()) {
                    this.updateStatus('ダウンロードするテキストがありません', 'error');
                    return;
                }

                const checkedFormats = Array.from(this.downloadFormatCheckboxes)
                                            .filter(cb => cb.checked)
                                            .map(cb => ({
                                                format: cb.value,
                                                mimeType: cb.dataset.mimeType,
                                                extension: cb.dataset.extension
                                            }));

                if (checkedFormats.length === 0) {
                    this.updateStatus('ダウンロード形式が選択されていません。設定から選んでください。', 'error');
                    return;
                }

                // ファイル名の日付部分を生成 (YYYYMMDD_HH-MM)
                const now = new Date();
                const year = now.getFullYear();
                const month = (now.getMonth() + 1).toString().padStart(2, '0');
                const day = now.getDate().toString().padStart(2, '0');
                const hours = now.getHours().toString().padStart(2, '0');
                const minutes = now.getMinutes().toString().padStart(2, '0');
                const datetimePrefix = `${year}${month}${day}_${hours}-${minutes}`;

                let downloadedCount = 0;

                checkedFormats.forEach(({ format, mimeType, extension }) => {
                    const { content, mimeType: finalMimeType, extension: finalExtension } = this.getFormattedDownloadData(originalText, format);
                    const filename = `${datetimePrefix}.${finalExtension}`;

                    const blob = new Blob([content], { type: finalMimeType });
                    const a = document.createElement('a');
                    a.href = URL.createObjectURL(blob);
                    a.download = filename;
                    
                    // ダウンロードをトリガー
                    document.body.appendChild(a);
                    a.click();
                    document.body.removeChild(a);
                    URL.revokeObjectURL(a.href);
                    downloadedCount++;
                });

                this.updateStatus(`${downloadedCount}個のファイルをダウンロードしました！`);
            }
            
            // テキストを履歴に保存
            saveToHistory() {
                const text = this.textOutput.value;
                if (!text.trim()) {
                    this.updateStatus('保存するテキストがありません', 'error');
                    return;
                }
                
                const historyItem = {
                    id: Date.now(), // ユニークなID
                    text: text,
                    date: new Date().toLocaleString('ja-JP'), // 日本語ロケールで日付をフォーマット
                    wordCount: this.countWords(text)
                };
                
                this.history.unshift(historyItem); // 配列の先頭に追加
                
                // 最大100件まで保存し、古いものから削除
                if (this.history.length > 100) {
                    this.history = this.history.slice(0, 100);
                }
                
                this.saveHistory(); // ローカルストレージに保存
                this.loadHistoryDisplay(); // 履歴表示を更新
                this.updateStatus('履歴に保存しました');
            }

            // 履歴のリセット
            resetHistory() {
                if (confirm('全ての履歴をリセットしてもよろしいですか？')) {
                    this.history = [];
                    this.saveHistory();
                    this.loadHistoryDisplay();
                    this.updateStatus('履歴をリセットしました');
                }
            }

            // 統計のリセット
            resetStats() {
                if (confirm('全ての統計データをリセットしてもよろしいですか？')) {
                    this.stats = { totalSessions: 0, totalWords: 0, totalTime: 0 };
                    this.saveStats();
                    this.updateStats();
                    this.updateStatus('統計データをリセットしました');
                }
            }
            
            // テンプレートをテキストエリアに挿入
            insertTemplate(template) {
                this.saveToUndoStack(); // 挿入前のテキストをアンドゥスタックに保存
                const cursorPos = this.textOutput.selectionStart; // 現在のカーソル位置
                const textBefore = this.textOutput.value.substring(0, cursorPos);
                const textAfter = this.textOutput.value.substring(cursorPos);
                
                this.textOutput.value = textBefore + template + textAfter; // テンプレートを挿入
                this.textOutput.focus(); // テキストエリアにフォーカス
                // カーソル位置をテンプレートの末尾に移動
                this.textOutput.selectionStart = this.textOutput.selectionEnd = cursorPos + template.length;
                
                this.updateCharCount();
                this.updateStatus('テンプレートを挿入しました');
            }
            
            // 現在のテキストをアンドゥスタックに保存
            saveToUndoStack() {
                // 現在のテキストがスタックの最後と同じ場合は保存しない（連続入力による重複を防ぐ）
                if (this.undoStack.length > 0 && this.undoStack[this.undoStack.length - 1] === this.textOutput.value) {
                    return;
                }
                this.undoStack.push(this.textOutput.value);
                this.redoStack = []; // アンドゥした場合はリドゥスタックをクリア
                
                // 最大50件まで保存し、古いものから削除
                if (this.undoStack.length > 50) {
                    this.undoStack.shift();
                }
            }
            
            // 元に戻す (Undo)
            undo() {
                if (this.undoStack.length === 0) return;
                
                this.redoStack.push(this.textOutput.value); // 現在のテキストをリドゥスタックに保存
                this.textOutput.value = this.undoStack.pop(); // スタックから一つ前のテキストを取得
                this.updateCharCount();
                this.updateStatus('元に戻しました');
            }
            
            // やり直し (Redo)
            redo() {
                if (this.redoStack.length === 0) return;
                
                this.undoStack.push(this.textOutput.value); // 現在のテキストをアンドゥスタックに保存
                this.textOutput.value = this.redoStack.pop(); // スタックから一つ後のテキストを取得
                this.updateCharCount();
                this.updateStatus('やり直しました');
            }
            
            // ボタンの状態をリセット
            resetButtons() {
                this.micBtn.classList.remove('listening');
                this.micBtn.disabled = false;
                this.stopBtn.disabled = true;
            }
            
            // 文字数と単語数を更新
            updateCharCount() {
                const text = this.textOutput.value;
                const charCount = text.length;
                const wordCount = this.countWords(text);
                
                this.charCount.textContent = charCount.toLocaleString();
                this.wordCount.textContent = wordCount.toLocaleString();
            }
            
            // テキストの単語数をカウント (日本語と英語で異なるロジック)
            countWords(text) {
                if (!text.trim()) return 0;
                
                // 日本語の文字が含まれている場合は文字数（空白なし）を返す
                if (/[\u3400-\u9FBF\u3040-\u309F\u30A0-\u30FF]/.test(text)) { // UnicodeのCJK統合漢字、ひらがな、カタカナの範囲をチェック
                    return text.replace(/\s+/g, '').length;
                } else {
                    // 英語の場合はスペースで区切られた単語数を返す
                    return text.trim().split(/\s+/).length;
                }
            }

            // セッション統計を更新
            updateSessionStats() {
                if (this.sessionStartTime) {
                    const sessionDuration = (Date.now() - this.sessionStartTime) / (1000 * 60); // ミリ秒から分に変換
                    this.stats.totalTime += sessionDuration;
                    this.stats.totalSessions++;
                    this.stats.totalWords += this.countWords(this.finalTranscript);
                    this.saveStats(); // 統計を保存
                    this.updateStats(); // 統計表示を更新
                    this.sessionStartTime = null; // セッション開始時間をリセット
                }
            }

            // 統計データをローカルストレージから読み込む
            loadStats() {
                try {
                    const stats = JSON.parse(localStorage.getItem('voiceAssistantStats')) || { totalSessions: 0, totalWords: 0, totalTime: 0 };
                    return stats;
                } catch (e) {
                    console.error("Failed to load stats:", e);
                    return { totalSessions: 0, totalWords: 0, totalTime: 0 };
                }
            }

            // 統計データをローカルストレージに保存する
            saveStats() {
                try {
                    localStorage.setItem('voiceAssistantStats', JSON.stringify(this.stats));
                } catch (e) {
                    console.error("Failed to save stats:", e);
                    this.updateStatus('統計データの保存に失敗しました。ブラウザのストレージがいっぱいかもしれません。', 'error');
                }
            }

            // 履歴データをローカルストレージから読み込む
            loadHistory() {
                try {
                    const history = JSON.parse(localStorage.getItem('voiceAssistantHistory')) || [];
                    return history;
                } catch (e) {
                    console.error("Failed to load history:", e);
                    return [];
                }
            }

            // 履歴データをローカルストレージに保存する
            saveHistory() {
                try {
                    localStorage.setItem('voiceAssistantHistory', JSON.stringify(this.history));
                } catch (e) {
                    console.error("Failed to save history:", e);
                    this.updateStatus('履歴の保存に失敗しました。ブラウザのストレージがいっぱいかもしれません。', 'error');
                }
            }

            // 履歴リストを表示に反映
            loadHistoryDisplay() {
                this.historyList.innerHTML = ''; // 既存のリストをクリア
                if (this.history.length === 0) {
                    this.historyList.innerHTML = '<p style="text-align: center; color: #999;">まだ履歴はありません。</p>';
                    return;
                }
                this.history.forEach(item => {
                    const div = document.createElement('div');
                    div.className = 'history-item';
                    // XSS対策: textContentを使用
                    div.innerHTML = `
                        <div class="history-item-date">${item.date}</div>
                        <div class="history-item-text"></div>
                    `;
                    div.querySelector('.history-item-text').textContent = item.text;
                    
                    // 履歴アイテムをクリックするとテキストエリアに内容をロード
                    div.addEventListener('click', () => {
                        this.textOutput.value = item.text;
                        this.updateCharCount();
                        this.updateStatus('履歴をロードしました');
                    });
                    this.historyList.appendChild(div);
                });
            }

            // マイク許可をチェックし、必要に応じてガイドモーダルを表示
            async checkMicrophonePermissionAndShowGuide() {
                if (!this.showMicrophoneGuideOnStartup) {
                    return; // ガイド表示設定がオフの場合は何もしない
                }

                try {
                    const permissionStatus = await navigator.permissions.query({ name: 'microphone' });

                    if (permissionStatus.state === 'granted') {
                        // マイクが既に許可されている場合はモーダルを表示しない
                        this.hasRequestedMicrophonePermission = true; // 許可されている場合もフラグを立てる
                        return;
                    } else if (permissionStatus.state === 'denied') {
                        // 許可が拒否されている場合
                        this.showMicrophoneGuideModal();
                    } else if (permissionStatus.state === 'prompt') {
                        // 許可を求められる状態の場合
                        // アプリ起動時に一度もマイク許可を要求していなければ、ここで要求する
                        if (!this.hasRequestedMicrophonePermission) {
                            try {
                                // recognition.start() を呼び出すことで、ブラウザのマイク許可プロンプトが表示される
                                // ただし、ここでは実際に録音を開始せず、許可プロンプトのトリガーのみを目的とする
                                // そのため、すぐに recognition.abort() を呼び出す
                                this.recognition.start();
                                this.recognition.abort(); // 許可プロンプト表示後すぐに停止
                            } catch (e) {
                                console.warn("Failed to trigger microphone permission prompt:", e);
                                // エラーが発生した場合も、ユーザーにガイドを表示する
                                this.showMicrophoneGuideModal();
                            }
                            this.hasRequestedMicrophonePermission = true; // 要求フラグを立てる
                        }
                    }
                } catch (error) {
                    console.error('マイク許可の確認中にエラーが発生しました:', error);
                    // エラーが発生した場合もガイドを表示する
                    this.showMicrophoneGuideModal();
                }
            }

            // マイクガイドモーダルを表示
            showMicrophoneGuideModal() {
                this.microphoneGuideModal.classList.add('active');
            }

            // マイクガイドモーダルを非表示
            hideMicrophoneGuideModal() {
                this.microphoneGuideModal.classList.remove('active');
            }

            // マイクガイド表示設定をローカルストレージに保存
            saveMicrophoneGuideSetting() {
                try {
                    localStorage.setItem('showMicrophoneGuide', JSON.stringify(this.showMicrophoneGuideOnStartup));
                } catch (e) {
                    console.error("Failed to save microphone guide setting:", e);
                    this.updateStatus('マイクガイド設定の保存に失敗しました。', 'error');
                }
            }

            // マイクガイド表示設定をローカルストレージからロード
            loadMicrophoneGuideSetting() {
                try {
                    const setting = localStorage.getItem('showMicrophoneGuide');
                    // デフォルトはtrue（表示する）
                    return setting === null ? true : JSON.parse(setting);
                } catch (e) {
                    console.error("Failed to load microphone guide setting:", e);
                    return true; // エラー時はデフォルトで表示する
                }
            }

            // ダウンロード形式設定をローカルストレージからロード
            loadDownloadFormatSettings() {
                try {
                    const settings = JSON.parse(localStorage.getItem('downloadFormatSettings')) || {};
                    // デフォルトはtxtのみtrue
                    if (Object.keys(settings).length === 0) {
                        return { txt: true, md: false, html: false, json: false, csv: false };
                    }
                    return settings;
                } catch (e) {
                    console.error("Failed to load download format settings:", e);
                    return { txt: true, md: false, html: false, json: false, csv: false };
                }
            }

            // ダウンロード形式設定をローカルストレージに保存
            saveDownloadFormatSettings() {
                const settings = {};
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    settings[checkbox.value] = checkbox.checked;
                });
                try {
                    localStorage.setItem('downloadFormatSettings', JSON.stringify(settings));
                } catch (e) {
                    console.error("Failed to save download format settings:", e);
                    this.updateStatus('ダウンロード形式設定の保存に失敗しました。', 'error');
                }
            }

            // ダウンロード形式設定をUIに適用
            applyDownloadFormatSettings() {
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    checkbox.checked = this.downloadFormats[checkbox.value] || false;
                });
            }

            // OpenAI APIキーをローカルストレージからロード
            loadOpenAIApiKey() {
                try {
                    return localStorage.getItem('openaiApiKey') || '';
                } catch (e) {
                    console.error("Failed to load OpenAI API key:", e);
                    return '';
                }
            }

            // OpenAI APIキーをローカルストレージに保存
            saveOpenAIApiKey(key) {
                try {
                    localStorage.setItem('openaiApiKey', key);
                } catch (e) {
                    console.error("Failed to save OpenAI API key:", e);
                    this.updateStatus('APIキーの保存に失敗しました。ブラウザのストレージがいっぱいかもしれません。', 'error');
                }
            }

            // ステータス表示を更新する汎用メソッド
            updateStatus(message, type = 'info', duration = 3000) {
                this.statusDisplay.textContent = message;
                this.statusDisplay.className = `status-display ${type === 'error' ? 'error' : type === 'listening' ? 'listening' : ''}`;

                // 一時的なメッセージの場合、一定時間後にリセット
                if (duration > 0 && type !== 'listening') {
                    clearTimeout(this.statusTimeout); // 既存のタイムアウトがあればクリア
                    this.statusTimeout = setTimeout(() => {
                        this.statusDisplay.textContent = '準備完了 - マイクボタンを押して開始';
                        this.statusDisplay.className = 'status-display';
                    }, duration);
                }
            }

            // テキストを要約するメソッド
            async summarizeText() {
                const originalText = this.textOutput.value.trim();
                if (!originalText) {
                    this.updateStatus("要約するテキストがありません", "error");
                    return;
                }

                if (!this.openaiApiKey) {
                    this.updateStatus("OpenAI APIキーが設定されていません。設定パネルで入力してください。", "error");
                    return;
                }

                this.updateStatus("要約中...", "listening");

                try {
                    const response = await fetch("https://api.openai.com/v1/chat/completions", {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                            "Authorization": `Bearer ${this.openaiApiKey}`
                        },
                        body: JSON.stringify({
                            model: "gpt-3.5-turbo",
                            messages: [
                                { role: "system", content: "以下のテキストを要点だけ5行以内でまとめてください。" },
                                { role: "user", content: originalText }
                            ],
                            temperature: 0.5
                        })
                    });

                    if (!response.ok) {
                        const errorData = await response.json();
                        throw new Error(errorData.error?.message || `APIエラー: ${response.status} ${response.statusText}`);
                    }

                    const data = await response.json();
                    const summary = data.choices?.[0]?.message?.content?.trim();
                    if (summary) {
                        this.saveToUndoStack(); // 要約追加前にアンドゥスタックに保存
                        this.textOutput.value += "\n\n---\n🧠 要約:\n" + summary;
                        this.updateStatus("要約が完了しました");
                        this.updateCharCount();
                    } else {
                        throw new Error("要約結果が取得できませんでした");
                    }
                } catch (err) {
                    console.error("要約エラー:", err);
                    this.updateStatus("要約に失敗しました: " + err.message, "error");
                }
            }
        }

        // DOMContentLoadedイベントでVoiceAssistantProクラスを初期化
        document.addEventListener('DOMContentLoaded', () => {
            new VoiceAssistantPro();
        });
    </script>
</body>
</html>
```
0.1秒
上矢印キーと下矢印キーを使用してターンを選択し、Enter キーでそのターンにジャンプし、Escape キーでチャットに戻ります。
プロンプトを入力し始める式.html…]()

---

---

## 2. ユーザーガイド (Claude Voice Assistant Proユーザーガイド.md)
[Claude Voice Assistant Pro_ユーザーガイド.md](https://github.com/user-attachments/files/22306285/Claude.Voice.Assistant.Pro_.md)
## 1. GitHub用 README.md (初心者向けマニュアル)

このドキュメントは、GitHubに公開する際に利用できる形式で作成しています。
プロジェクトの概要、使い方、主要機能などを初心者の方にも分かりやすく説明します。

---

# Claude Voice Assistant Pro 🎤

Claude Voice Assistant Pro は、あなたの声をテキストに変換し、AIアシスタント「Claude」との対話をよりスムーズにするための革新的なツールです。直感的なボタン操作で、話すだけでテキスト入力が可能になり、Claudeの活用を最大化できます。

## ✨ 主な機能 - ボタンで直感的に操作！

このアプリは、視覚的に分かりやすいボタンを使って、誰でも簡単に操作できます。

*   **🎤 音声入力の開始/停止:** マイクボタンを押すだけで、あなたの声が瞬時にテキストに変換され始めます。もう一度押すか、⏹️ボタンで停止します。
*   **📋 テキストのコピー:** 生成されたテキストをワンクリックでクリップボードにコピーできます。
*   **🗑️ テキストのクリア:** 現在のテキストエリアの内容を簡単に消去できます。
*   **💾 履歴への保存:** 重要な会話やメモは、ワンクリックで履歴として保存できます。後でいつでも見返したり、再利用したりできます。
*   **⬇️ テキストのダウンロード:**
    *   現在のテキストを様々な形式（`.txt`, `.md`, `.html`, `.json`, `.csv`）でダウンロードできます。
    *   ダウンロードされたファイルは、**お使いのブラウザのデフォルトのダウンロードフォルダ**に自動的に保存されます。
*   **🧠 AI要約機能 (NEW!):**
    *   入力したテキストをAI（OpenAI）が**自動で要約**してくれます。長い文章もすぐにポイントを把握できます！
    *   _※ この機能を利用するには、コード内にご自身のOpenAI APIキーを設定する必要があります。_
*   **↶ 元に戻す / ↷ やり直し:** 入力ミスや変更も、ボタン一つで簡単に取り消したり、元に戻したりできます。
*   **🇯🇵 言語選択:** 日本語だけでなく、英語など複数の言語での音声認識に対応しています。
*   **📝 テンプレート:** よく使うフレーズや質問をテンプレートとして用意。クリック一つでテキストエリアに挿入し、Claudeへの指示を効率化できます。
*   **📚 履歴表示:** 過去の音声入力内容を一覧で確認し、クリックで再ロードできます。
*   **📊 利用統計:** セッション数、総単語数、総利用時間など、あなたのClaude活用状況を数値で確認できます。

## 🚀 使い方 - たったこれだけ！

1.  **ファイルをブラウザで開く:**
    `ClaudeVoicepro_with_Summary.html` ファイルをウェブブラウザ（Google Chrome, Microsoft Edgeなど）で開きます。
    *   _ヒント: ファイルをブラウザのアイコンにドラッグ＆ドロップするか、ファイルを右クリックして「プログラムから開く」→「ウェブブラウザ」を選択してください。_
2.  **マイクの許可:**
    初めて利用する際、ブラウザからマイクの使用許可を求められる場合があります。「許可」をクリックしてください。
    *   _もし「許可」が出ない場合やエラーになる場合は、画面右上の「設定」パネル内にある「マイク設定ガイドを表示」をご確認ください。_
3.  **音声入力の開始:**
    画面中央にある大きなマイクボタン（🎤）をクリックします。ステータス表示が「聞いています... 話してください」に変わったら、話し始めてください。
4.  **テキストの確認:**
    話した内容がリアルタイムでテキストエリアに表示されます。
5.  **操作の実行:**
    必要に応じて、コピー（📋）、クリア（🗑️）、保存（💾）、ダウンロード（⬇️）、AI要約（🧠）などのボタンをクリックして操作します。
6.  **テンプレートの活用:**
    右側の「テンプレート」パネルをクリックすると、テキストエリアに便利なフレーズが挿入されます。

## 💡 重要事項

*   **OpenAI APIキーの設定について:**
    AI要約機能を利用するには、JavaScriptコード内の以下の行を、ご自身のOpenAI APIキーに置き換える必要があります。
    `const OPENAI_API_KEY = "YOUR_API_KEY_HERE";`
    _このキーが設定されていない場合、要約機能は動作しません。_
    APIキーは他人に知られないよう、慎重に管理してください。
*   **マイクのアクセス許可:**
    本アプリはWeb Speech APIを使用するため、ブラウザやOSのマイクアクセス許可が必要です。初回起動時にプロンプトが表示されますので、「許可」してください。
*   **ローカルファイルとして動作:**
    このアプリはHTMLファイルとしてダウンロードされ、インターネット接続がなくても音声認識機能（OpenAI要約機能を除く）は動作します。

---

## 💻 動作環境

*   最新のWebブラウザ (Google Chrome, Microsoft Edge, Firefoxなど)
*   マイクデバイス
*   OpenAI要約機能を利用する場合はインターネット接続とOpenAI APIキー

---

## 📄 ライセンス

---

### MITライセンス

著作権表示

Copyright (c) 2025 Hanamaruki

ここに、本ソフトウェアとそれに関連するドキュメントファイル（以下「本ソフトウェア」）の複製物を受け取るすべての人に対し、無料で利用を許可します。
この許可には、本ソフトウェアを制限なく取り扱う権利が含まれます。
具体的には、使用、複製、変更、結合、出版、配布、サブライセンスの付与、および販売を行う権利、また、本ソフトウェアが提供される相手に対して、これらの行為を許可する権利を意味します。
ただし、以下の条件に従うものとします。

上記に記載された著作権表示と、本許可表示は、本ソフトウェアのすべての複製物、または実質的な部分に含まれなければならないものとします。

本ソフトウェアは「現状のまま」提供され、商品性、特定の目的への適合性、および非侵害性に対する保証を含む、明示的または黙示的ないかなる種類の保証もありません。
いかなる場合も、著者または著作権者は、本ソフトウェアの使用またはその他の取り扱いから生じる、契約、不法行為、またはその他の行為にかかわらず、いかなる請求、損害、またはその他の責任に対しても責任を負わないものとします。

---

### MIT License

Copyright (c) 2025 Hanamaruki

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 3. 技術仕様書 (Claude Voice Assistant Pro - 技術仕様書.md)
[ClaudeVoicePro_with_Summary.html](https://github.com/user-attachments/files/22306287/ClaudeVoicePro_with_Summary.html)
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Claude Voice Assistant Pro</title>
    <style>
        /* 全体的なリセットと基本設定 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            overflow-x: hidden;
        }
        
        /* コンテナ */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* ヘッダーセクション */
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5em;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #666;
            font-size: 1.1em;
        }
        
        /* メインコンテンツレイアウト */
        .main-content {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        /* 音声パネル */
        .voice-panel {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        /* 音声コントロールボタン群 */
        .voice-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 20px;
            flex-wrap: wrap;
            align-items: center;
        }
        
        .voice-btn {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            border: none;
            cursor: pointer;
            font-size: 28px;
            transition: all 0.3s ease;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .voice-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }
        
        /* マイクボタンのスタイル */
        .mic-btn {
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white;
        }
        
        .mic-btn.listening {
            background: linear-gradient(45deg, #f44336, #da190b);
            animation: pulse 1.5s infinite;
        }
        
        /* その他のボタンのスタイル */
        .stop-btn {
            background: linear-gradient(45deg, #f44336, #da190b);
            color: white;
        }
        
        .copy-btn {
            background: linear-gradient(45deg, #2196F3, #1976D2);
            color: white;
        }
        
        .clear-btn {
            background: linear-gradient(45deg, #ff9800, #f57c00);
            color: white;
        }
        
        .save-btn {
            background: linear-gradient(45deg, #9c27b0, #7b1fa2);
            color: white;
        }

        /* ダウンロードボタンのスタイル */
        .download-btn {
            background: linear-gradient(45deg, #42a5f5, #1e88e5); /* 青系のグラデーション */
            color: white;
        }
        
        .voice-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none !important;
        }
        
        /* ステータス表示 */
        .status-display {
            background: linear-gradient(45deg, #f8f9fa, #e9ecef);
            border-radius: 15px;
            padding: 15px;
            margin-bottom: 20px;
            text-align: center;
            font-weight: bold;
            color: #495057;
        }
        
        .status-display.listening {
            background: linear-gradient(45deg, #d4edda, #c3e6cb);
            color: #155724;
            border: 2px solid #28a745;
        }
        
        .status-display.error {
            background: linear-gradient(45deg, #f8d7da, #f5c6cb);
            color: #721c24;
            border: 2px solid #dc3545;
        }
        
        /* テキストエリアコンテナ */
        .textarea-container {
            position: relative;
        }
        
        textarea {
            width: 100%;
            height: 300px;
            padding: 20px;
            border: 2px solid #e0e0e0;
            border-radius: 15px;
            font-size: 16px;
            line-height: 1.6;
            resize: vertical;
            font-family: inherit;
            background: #fafafa;
            transition: all 0.3s ease;
        }
        
        textarea:focus {
            outline: none;
            border-color: #667eea;
            background: white;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }
        
        /* テキストエリアツールボタン */
        .textarea-tools {
            position: absolute;
            bottom: 10px;
            right: 10px;
            display: flex;
            gap: 10px;
        }
        
        .tool-btn {
            background: rgba(255, 255, 255, 0.9);
            border: none;
            border-radius: 20px;
            padding: 8px 12px;
            font-size: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }
        
        .tool-btn:hover {
            background: white;
            transform: translateY(-1px);
        }
        
        /* サイドバーレイアウト */
        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        /* 設定パネル（details要素として再定義） */
        .settings-panel details {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .settings-panel summary {
            font-size: 1.5em; /* h3のサイズに合わせる */
            font-weight: bold;
            color: #333;
            cursor: pointer;
            margin-bottom: 15px;
            list-style: none; /* デフォルトのマーカーを非表示に */
            display: flex;
            align-items: center;
        }

        .settings-panel summary::before {
            content: '⚙️ '; /* 歯車アイコン */
            margin-right: 10px;
        }

        .settings-panel details[open] summary {
            margin-bottom: 20px; /* 開いたときにコンテンツとの間にスペース */
        }
        
        .setting-item {
            margin-bottom: 15px;
        }
        
        .setting-item label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
            color: #555;
        }
        
        .setting-item select,
        .setting-item input[type="checkbox"] {
            width: auto; /* チェックボックスの幅を自動調整 */
            margin-right: 8px; /* チェックボックスとラベルの間にスペース */
        }

        .setting-item input[type="text"],
        .setting-item select {
            width: 100%;
            padding: 8px 12px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s ease;
        }
        
        .setting-item select:focus,
        .setting-item input[type="text"]:focus {
            outline: none;
            border-color: #667eea;
        }

        .setting-item.checkbox-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .setting-item.checkbox-item label {
            margin-bottom: 0;
        }

        /* ファイル形式選択のスタイル */
        .download-format-options {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin-top: 10px;
        }
        .download-format-options label {
            display: flex;
            align-items: center;
            margin-bottom: 0; /* 親要素のmargin-bottomがあるのでリセット */
            font-weight: normal;
        }
        .download-format-options input[type="checkbox"] {
            margin-right: 8px;
        }

        /* リセットボタンのスタイル */
        .reset-button {
            background: linear-gradient(45deg, #ef5350, #d32f2f); /* 赤系のグラデーション */
            color: white;
            border: none;
            border-radius: 8px;
            padding: 10px 15px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9em;
            width: 100%;
            margin-top: 10px;
        }
        .reset-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        .reset-group {
            margin-top: 20px;
            border-top: 1px solid #eee;
            padding-top: 15px;
        }
        
        /* テンプレートパネル */
        .templates-panel {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .template-item {
            background: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .template-item:hover {
            background: #e9ecef;
            transform: translateY(-1px);
        }
        
        .template-item h4 {
            margin-bottom: 5px;
            color: #333;
            font-size: 14px;
        }
        
        .template-item p {
            font-size: 12px;
            color: #666;
            margin: 0;
        }
        
        /* 履歴パネル */
        .history-panel {
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-height: 300px; /* スクロール可能にする */
            overflow-y: auto;
        }
        
        .history-item {
            background: #f8f9fa;
            border: 1px solid #e9ecef; /* 履歴アイテムのボーダーを追加 */
            border-radius: 8px;
            padding: 10px;
            margin-bottom: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-left: 4px solid #667eea;
        }
        
        .history-item:hover {
            background: #e9ecef;
            transform: translateX(5px);
        }
        
        .history-item-date {
            font-size: 11px;
            color: #666;
            margin-bottom: 5px;
        }
        
        .history-item-text {
            font-size: 13px;
            color: #333;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap; /* 1行で表示 */
        }
        
        /* 統計パネル */
        .stats-panel {
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 20px;
            padding: 20px;
            color: white;
            text-align: center;
        }
        
        .stats-item {
            margin-bottom: 15px;
        }
        
        .stats-number {
            font-size: 2em;
            font-weight: bold;
            display: block;
        }
        
        .stats-label {
            font-size: 0.9em;
            opacity: 0.8;
        }
        
        /* 文字数・単語数表示 */
        .word-count {
            text-align: right;
            color: #666;
            margin-top: 10px;
            font-size: 14px;
        }
        
        /* アニメーション */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* レスポンシブデザイン */
        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr; /* 1列レイアウトに変更 */
            }
            
            .voice-controls {
                gap: 10px;
            }
            
            .voice-btn {
                width: 60px;
                height: 60px;
                font-size: 24px;
            }
            
            .header h1 {
                font-size: 2em;
            }
        }

        /* マイクガイドモーダル */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            max-width: 500px;
            text-align: center;
            transform: translateY(-20px);
            transition: transform 0.3s ease;
        }

        .modal-overlay.active .modal-content {
            transform: translateY(0);
        }

        .modal-content h3 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.8em;
        }

        .modal-content p {
            margin-bottom: 15px;
            line-height: 1.6;
            color: #555;
        }

        .modal-content ul {
            list-style: none;
            padding: 0;
            margin-bottom: 20px;
            text-align: left;
            color: #666;
        }

        .modal-content ul li {
            margin-bottom: 10px;
            padding-left: 0; /* チェックマークを削除したのでパディングも不要 */
            position: relative;
        }

        /* チェックマークを削除 */
        .modal-content ul li::before {
            content: none; 
        }

        .modal-close-btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            border: none;
            border-radius: 25px;
            padding: 12px 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1.1em;
        }

        .modal-close-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎤 Claude Voice Assistant Pro</h1>
            <p>音声入力でClaude活用を最大化！プロ仕様の音声認識アシスタント</p>
        </div>
        
        <div class="main-content">
            <div class="voice-panel">
                <div class="status-display" id="statusDisplay">
                    準備完了 - マイクボタンを押して開始
                </div>
                
                <div class="voice-controls">
                    <button class="voice-btn mic-btn" id="micBtn" title="音声入力開始">
                        🎤
                    </button>
                    <button class="voice-btn stop-btn" id="stopBtn" title="録音停止" disabled>
                        ⏹️
                    </button>
                    <button class="voice-btn copy-btn" id="copyBtn" title="クリップボードにコピー">
                        📋
                    </button>
                    <button class="voice-btn clear-btn" id="clearBtn" title="テキストクリア">
                        🗑️
                    </button>
                    <button class="voice-btn save-btn" id="saveBtn" title="履歴に保存">
                        💾
                    </button>
                    <button class="voice-btn download-btn" id="downloadBtn" title="テキストをダウンロード">
                        ⬇️
                    </button>
                </div>
                
                <div class="textarea-container">
                    <textarea id="textOutput" placeholder="音声で入力されたテキストがここに表示されます。

🎯 Claude活用のコツ：
• 「〜について詳しく教えて」
• 「〜を分かりやすく説明して」
• 「〜のメリットとデメリットは？」
• 「〜を要約して」

右側のテンプレートも活用してください！"></textarea>
<!-- 要約ボタン -->
<div class="summary-container" style="text-align: right; margin-top: 10px;">
  <button id="summarizeBtn" class="tool-btn">🧠 要約する</button>
</div>

                    <div class="textarea-tools">
                        <button class="tool-btn" id="undoBtn">↶ 元に戻す</button>
                        <button class="tool-btn" id="redoBtn">↷ やり直し</button>
                    </div>
                </div>
                
                <div class="word-count">
                    文字数: <span id="charCount">0</span> | 単語数: <span id="wordCount">0</span>
                </div>
            </div>
            
            <div class="sidebar">
                <div class="settings-panel">
                    <details open> <!-- open属性でデフォルトで開く -->
                        <summary>設定</summary>
                        <div class="setting-item">
                            <label for="language">言語</label>
                            <select id="language">
                                <option value="ja-JP">🇯🇵 日本語</option>
                                <option value="en-US">🇺🇸 English</option>
                                <option value="en-GB">🇬🇧 English (UK)</option>
                                <option value="zh-CN">🇨  中文</option>
                                <option value="ko-KR">🇰🇷 한국어</option>
                            </select>
                        </div>
                        <div class="setting-item checkbox-item">
                            <label for="autoSave">自動保存</label>
                            <input type="checkbox" id="autoSave" checked>
                        </div>
                        <div class="setting-item checkbox-item">
                            <label for="showMicrophoneGuide">マイク設定ガイドを表示</label>
                            <input type="checkbox" id="showMicrophoneGuide" checked>
                        </div>
                        <div class="setting-item">
                            <label for="theme">テーマ</label>
                            <select id="theme">
                                <option value="default">デフォルト</option>
                                <option value="dark">ダーク</option>
                                <option value="minimal">ミニマル</option>
                            </select>
                        </div>

                        <div class="setting-item">
                            <label>ダウンロード形式</label>
                            <div class="download-format-options" id="downloadFormatOptions">
                                <label><input type="checkbox" id="downloadFormat_txt" value="txt" data-mime-type="text/plain;charset=utf-8" data-extension="txt" checked> 📄 テキスト (.txt)</label>
                                <label><input type="checkbox" id="downloadFormat_md" value="md" data-mime-type="text/markdown;charset=utf-8" data-extension="md"> 📝 マークダウン (.md)</label>
                                <label><input type="checkbox" id="downloadFormat_html" value="html" data-mime-type="text/html;charset=utf-8" data-extension="html"> 🌐 HTML (.html)</label>
                                <label><input type="checkbox" id="downloadFormat_json" value="json" data-mime-type="application/json;charset=utf-8" data-extension="json"> 💻 JSON (.json)</label>
                                <label><input type="checkbox" id="downloadFormat_csv" value="csv" data-mime-type="text/csv;charset=utf-8" data-extension="csv"> 📊 CSV (.csv)</label>
                            </div>
                        </div>

                        <div class="reset-group">
                            <button class="reset-button" id="resetHistoryBtn">📚 履歴をリセット</button>
                            <button class="reset-button" id="resetStatsBtn">📊 統計をリセット</button>
                        </div>
                    </details>
                </div>
                
                <div class="templates-panel">
                    <h3>📝 テンプレート</h3>
                    <div class="template-item" data-template="について詳しく教えてください。特に以下の点を含めて説明してください：">
                        <h4>詳細説明</h4>
                        <p>トピックについて詳しく説明してもらう</p>
                    </div>
                    <div class="template-item" data-template="を分かりやすく要約してください。要点を箇条書きで教えてください：">
                        <h4>要約・整理</h4>
                        <p>内容を整理して要約してもらう</p>
                    </div>
                    <div class="template-item" data-template="のメリットとデメリットを教えてください。比較表があると助かります：">
                        <h4>比較分析</h4>
                        <p>メリット・デメリットを比較分析</p>
                    </div>
                    <div class="template-item" data-template="について初心者にも分かるように説明してください。具体例も含めて：">
                        <h4>初心者向け</h4>
                        <p>専門用語を使わず分かりやすく説明</p>
                    </div>
                </div>
                
                <div class="history-panel">
                    <h3>📚 履歴</h3>
                    <div id="historyList">
                        <!-- 履歴がここに表示されます -->
                    </div>
                </div>
                
                <div class="stats-panel">
                    <h3>📊 統計</h3>
                    <div class="stats-item">
                        <span class="stats-number" id="totalSessions">0</span>
                        <span class="stats-label">セッション数</span>
                    </div>
                    <div class="stats-item">
                        <span class="stats-number" id="totalWords">0</span>
                        <span class="stats-label">総単語数</span>
                    </div>
                    <div class="stats-item">
                        <span class="stats-number" id="totalTime">0</span>
                        <span class="stats-label">総利用時間(分)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- マイクガイドモーダル -->
    <div class="modal-overlay" id="microphoneGuideModal">
        <div class="modal-content">
            <h3>マイク設定のお願い</h3>
            <p>このアプリは音声入力を使用します。マイクが有効になっていない場合、以下の手順で設定をご確認ください。</p>
            <ul>
                <li>ブラウザのアドレスバーに表示されるマイクアイコン（または南京錠アイコン）をクリックしてください。</li>
                <li>「マイクへのアクセス」または「サイトの設定」で、このサイトのマイク使用を「許可」に設定してください。</li>
                <li>もしブラウザの設定で許可できない場合は、お使いのOS（Windows/macOS/Android/iOS）のシステム設定でブラウザアプリのマイクアクセスを許可してください。</li>
            </ul>
            <button class="modal-close-btn" id="closeMicrophoneGuideModal">OK、理解しました</button>
        </div>
    </div>

    <script>
        class VoiceAssistantPro {
            constructor() {
                this.recognition = null;
                this.isListening = false;
                this.finalTranscript = '';
                this.undoStack = [];
                this.redoStack = [];
                this.sessionStartTime = null;
                this.stats = this.loadStats();
                this.history = this.loadHistory();
                this.showMicrophoneGuideOnStartup = this.loadMicrophoneGuideSetting(); // マイクガイド設定をロード
                this.hasRequestedMicrophonePermission = false; // マイク許可を一度でも要求したかどうかのフラグ
                this.downloadFormats = this.loadDownloadFormatSettings(); // ダウンロード形式設定をロード

                this.initElements();
                this.initSpeechRecognition();
                this.bindEvents();
                this.updateCharCount();
                this.updateStats();
                this.loadHistoryDisplay();
                this.applyDownloadFormatSettings(); // ダウンロード形式設定を適用
                this.checkMicrophonePermissionAndShowGuide(); // マイク許可をチェックし、必要ならガイドを表示
            }
            
            initElements() {
                this.micBtn = document.getElementById('micBtn');
                this.stopBtn = document.getElementById('stopBtn');
                this.copyBtn = document.getElementById('copyBtn');
                this.clearBtn = document.getElementById('clearBtn');
                this.saveBtn = document.getElementById('saveBtn');
                this.downloadBtn = document.getElementById('downloadBtn');
                this.downloadFormatCheckboxes = document.querySelectorAll('#downloadFormatOptions input[type="checkbox"]'); // 変更
                this.undoBtn = document.getElementById('undoBtn');
                this.redoBtn = document.getElementById('redoBtn');
                
                this.statusDisplay = document.getElementById('statusDisplay');
                this.textOutput = document.getElementById('textOutput');
                this.languageSelect = document.getElementById('language');
                this.charCount = document.getElementById('charCount');
                this.wordCount = document.getElementById('wordCount');
                
                this.totalSessions = document.getElementById('totalSessions');
                this.totalWords = document.getElementById('totalWords');
                this.totalTime = document.getElementById('totalTime');
                this.historyList = document.getElementById('historyList');
                
                this.templateItems = document.querySelectorAll('.template-item');

                // 新しいリセットボタン
                this.resetHistoryBtn = document.getElementById('resetHistoryBtn');
                this.resetStatsBtn = document.getElementById('resetStatsBtn');

                // マイクガイドモーダル関連要素
                this.microphoneGuideModal = document.getElementById('microphoneGuideModal');
                this.closeMicrophoneGuideModalBtn = document.getElementById('closeMicrophoneGuideModal');
                this.showMicrophoneGuideCheckbox = document.getElementById('showMicrophoneGuide');

                // チェックボックスの初期状態を設定
                this.showMicrophoneGuideCheckbox.checked = this.showMicrophoneGuideOnStartup;
            }
            
            initSpeechRecognition() {
                // ブラウザが音声認識APIをサポートしているか確認
                if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) {
                    this.statusDisplay.textContent = '音声認識非対応ブラウザです';
                    this.statusDisplay.className = 'status-display error';
                    this.micBtn.disabled = true;
                    return;
                }
                
                // SpeechRecognitionオブジェクトの初期化
                const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
                this.recognition = new SpeechRecognition();
                
                // 継続的な認識と中間結果の取得を有効にする
                this.recognition.continuous = true;
                this.recognition.interimResults = true;
                // 選択された言語を設定
                this.recognition.lang = this.languageSelect.value;
                
                // 認識開始時のイベントハンドラ
                this.recognition.onstart = () => {
                    this.isListening = true;
                    this.sessionStartTime = Date.now(); // セッション開始時間を記録
                    this.micBtn.classList.add('listening'); // マイクボタンにリスニング中のスタイルを適用
                    this.micBtn.disabled = true; // マイクボタンを無効化
                    this.stopBtn.disabled = false; // 停止ボタンを有効化
                    this.statusDisplay.textContent = '聞いています... 話してください';
                    this.statusDisplay.className = 'status-display listening'; // ステータス表示を更新
                };
                
                // 認識結果が得られた時のイベントハンドラ
                this.recognition.onresult = (event) => {
                    let interimTranscript = ''; // 中間結果を格納する変数
                    
                    // すべての認識結果をループ
                    for (let i = event.resultIndex; i < event.results.length; i++) {
                        const transcript = event.results[i][0].transcript;
                        
                        // 最終結果と中間結果を分離
                        if (event.results[i].isFinal) {
                            this.finalTranscript += transcript + ' '; // 最終結果に追加
                        } else {
                            interimTranscript += transcript; // 中間結果に追加
                        }
                    }
                    
                    // テキストエリアに最終結果と中間結果を表示
                    this.textOutput.value = this.finalTranscript + interimTranscript;
                    this.updateCharCount(); // 文字数・単語数を更新
                };
                
                // エラー発生時のイベントハンドラ
                this.recognition.onerror = (event) => {
                    console.error('音声認識エラー:', event.error);
                    this.statusDisplay.textContent = `エラー: ${event.error}`;
                    this.statusDisplay.className = 'status-display error';
                    this.resetButtons(); // ボタンの状態をリセット

                    // マイク許可エラーの場合、ガイドを表示
                    if (event.error === 'not-allowed' || event.error === 'permission-denied') {
                        this.showMicrophoneGuideModal();
                    }
                };
                
                // 認識終了時のイベントハンドラ
                this.recognition.onend = () => {
                    this.isListening = false;
                    this.updateSessionStats(); // セッション統計を更新
                    
                    // マイク許可が既に要求されており、かつガイド表示設定がONの場合に補足メッセージを追加
                    if (this.hasRequestedMicrophonePermission && this.showMicrophoneGuideOnStartup) {
                        this.statusDisplay.textContent = '認識完了 - 再度開始するにはマイクボタンを押してください。※ブラウザの仕様により、再度許可を求められる場合があります。';
                    } else {
                        this.statusDisplay.textContent = '認識完了 - 再度開始するにはマイクボタンを押してください';
                    }
                    this.statusDisplay.className = 'status-display';
                    this.resetButtons(); // ボタンの状態をリセット
                };
            }
            
            // イベントリスナーのバインド
            bindEvents() {
                this.micBtn.addEventListener('click', () => this.startRecognition());
                this.stopBtn.addEventListener('click', () => this.stopRecognition());
                this.copyBtn.addEventListener('click', () => this.copyText());
                this.clearBtn.addEventListener('click', () => this.clearText());
                this.saveBtn.addEventListener('click', () => this.saveToHistory());
                this.downloadBtn.addEventListener('click', () => this.downloadTextsInSelectedFormats()); // 変更
                this.undoBtn.addEventListener('click', () => this.undo());
                this.redoBtn.addEventListener('click', () => this.redo());

                // ダウンロード形式チェックボックスの変更イベント
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    checkbox.addEventListener('change', () => this.saveDownloadFormatSettings());
                });

                // リセットボタンのイベント
                this.resetHistoryBtn.addEventListener('click', () => this.resetHistory());
                this.resetStatsBtn.addEventListener('click', () => this.resetStats());
                
                // 言語選択が変更されたら認識言語を更新
                this.languageSelect.addEventListener('change', () => {
                    if (this.recognition) {
                        this.recognition.lang = this.languageSelect.value;
                    }
                });
                
                // テキストエリアの入力時にアンドゥスタックを更新し、文字数・単語数を更新
                this.textOutput.addEventListener('input', () => {
                    this.saveToUndoStack();
                    this.updateCharCount();
                });
                
                // テンプレートアイテムのクリックイベント
                this.templateItems.forEach(item => {
                    item.addEventListener('click', () => {
                        const template = item.dataset.template;
                        this.insertTemplate(template);
                    });
                });
                
                // マイクガイドモーダルの閉じるボタン
                this.closeMicrophoneGuideModalBtn.addEventListener('click', () => {
                    this.hideMicrophoneGuideModal();
                });

                // マイクガイド表示設定の変更
                this.showMicrophoneGuideCheckbox.addEventListener('change', (e) => {
                    this.showMicrophoneGuideOnStartup = e.target.checked;
                    this.saveMicrophoneGuideSetting();
                });

                // キーボードショートカット
                document.addEventListener('keydown', (e) => {
                    if (e.ctrlKey || e.metaKey) { // CtrlキーまたはCmdキーが押されている場合
                        switch(e.key) {
                            case 'm': // Ctrl/Cmd + M で録音開始/停止
                                e.preventDefault();
                                if (!this.isListening) {
                                    this.startRecognition();
                                } else {
                                    this.stopRecognition();
                                }
                                break;
                            case 'z': // Ctrl/Cmd + Z で元に戻す, Ctrl/Cmd + Shift + Z でやり直し
                                if (e.shiftKey) {
                                    e.preventDefault();
                                    this.redo();
                                } else {
                                    e.preventDefault();
                                    this.undo();
                                }
                                break;
                            case 's': // Ctrl/Cmd + S で履歴に保存
                                e.preventDefault();
                                this.saveToHistory();
                                break;
                            case 'd': // Ctrl/Cmd + D でダウンロード
                                e.preventDefault();
                                this.downloadTextsInSelectedFormats();
                                break;
                        }
                    }
                });
            }
            
            // 音声認識を開始
            startRecognition() {
                if (!this.recognition) return;
                
                this.saveToUndoStack(); // 現在のテキストをアンドゥスタックに保存
                
                try {
                    this.recognition.start();
                } catch (error) {
                    console.error('録音開始エラー:', error);
                    this.statusDisplay.textContent = '録音開始に失敗しました';
                    this.statusDisplay.className = 'status-display error';
                    // エラーがマイク許可関連の場合、ガイドを表示
                    if (error.name === 'NotAllowedError' || error.name === 'PermissionDeniedError') {
                        this.showMicrophoneGuideModal();
                    }
                }
            }
            
            // 音声認識を停止
            stopRecognition() {
                if (this.recognition && this.isListening) {
                    this.recognition.stop();
                }
            }
            
            // テキストエリアの内容をクリア
            clearText() {
                this.saveToUndoStack(); // クリア前のテキストをアンドゥスタックに保存
                this.textOutput.value = '';
                this.finalTranscript = '';
                this.updateCharCount();
                this.statusDisplay.textContent = 'テキストをクリアしました';
            }
            
            // テキストをクリップボードにコピー
            async copyText() {
                const text = this.textOutput.value;
                if (!text.trim()) {
                    this.statusDisplay.textContent = 'コピーするテキストがありません';
                    this.statusDisplay.className = 'status-display error';
                    return;
                }
                
                try {
                    await navigator.clipboard.writeText(text);
                    this.statusDisplay.textContent = 'クリップボードにコピーしました！';
                    this.statusDisplay.className = 'status-display';
                } catch (error) {
                    console.error('コピーエラー:', error);
                    this.textOutput.select();
                    this.statusDisplay.textContent = 'テキストを選択しました（手動でコピーしてください）';
                }
            }

            // ダウンロード形式に応じたテキスト生成とMIMEタイプ・拡張子の取得
            getFormattedDownloadData(originalText, format) {
                let content = originalText;
                let mimeType = '';
                let extension = '';

                switch (format) {
                    case 'txt':
                        mimeType = 'text/plain;charset=utf-8';
                        extension = 'txt';
                        break;
                    case 'md':
                        mimeType = 'text/markdown;charset=utf-8';
                        extension = 'md';
                        break;
                    case 'html':
                        const escapedText = originalText.replace(/&/g, '&amp;')
                                                      .replace(/</g, '&lt;')
                                                      .replace(/>/g, '&gt;')
                                                      .replace(/"/g, '&quot;')
                                                      .replace(/'/g, '&#039;');
                        content = `<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Claude Voice Assistant Output</title>
</head>
<body>
    <pre>${escapedText}</pre>
</body>
</html>`;
                        mimeType = 'text/html;charset=utf-8';
                        extension = 'html';
                        break;
                    case 'json':
                        content = JSON.stringify({
                            title: `Claude Voice Assistant Output`,
                            content: originalText,
                            timestamp: new Date().toISOString()
                        }, null, 2); // 2スペースインデントで整形
                        mimeType = 'application/json;charset=utf-8';
                        extension = 'json';
                        break;
                    case 'csv':
                        const csvEscapedText = originalText.replace(/"/g, '""');
                        content = `"${csvEscapedText}"`; // 全体を1つのセルとして保存
                        mimeType = 'text/csv;charset=utf-8';
                        extension = 'csv';
                        break;
                    default:
                        mimeType = 'text/plain;charset=utf-8';
                        extension = 'txt';
                        break;
                }
                return { content, mimeType, extension };
            }

            // 選択された全ての形式でテキストをダウンロード
            downloadTextsInSelectedFormats() {
                const originalText = this.textOutput.value;
                if (!originalText.trim()) {
                    this.statusDisplay.textContent = 'ダウンロードするテキストがありません';
                    this.statusDisplay.className = 'status-display error';
                    return;
                }

                const checkedFormats = Array.from(this.downloadFormatCheckboxes)
                                            .filter(cb => cb.checked)
                                            .map(cb => ({
                                                format: cb.value,
                                                mimeType: cb.dataset.mimeType,
                                                extension: cb.dataset.extension
                                            }));

                if (checkedFormats.length === 0) {
                    this.statusDisplay.textContent = 'ダウンロード形式が選択されていません。設定から選んでください。';
                    this.statusDisplay.className = 'status-display error';
                    return;
                }

                // ファイル名の日付部分を生成 (YYYYMMDD_HH-MM)
                const now = new Date();
                const year = now.getFullYear();
                const month = (now.getMonth() + 1).toString().padStart(2, '0');
                const day = now.getDate().toString().padStart(2, '0');
                const hours = now.getHours().toString().padStart(2, '0');
                const minutes = now.getMinutes().toString().padStart(2, '0');
                const datetimePrefix = `${year}${month}${day}_${hours}-${minutes}`;

                let downloadedCount = 0;

                checkedFormats.forEach(({ format, mimeType, extension }) => {
                    const { content, mimeType: finalMimeType, extension: finalExtension } = this.getFormattedDownloadData(originalText, format);
                    const filename = `${datetimePrefix}.${finalExtension}`;

                    const blob = new Blob([content], { type: finalMimeType });
                    const a = document.createElement('a');
                    a.href = URL.createObjectURL(blob);
                    a.download = filename;
                    
                    // ダウンロードをトリガー
                    document.body.appendChild(a);
                    a.click();
                    document.body.removeChild(a);
                    URL.revokeObjectURL(a.href);
                    downloadedCount++;
                });

                this.statusDisplay.textContent = `${downloadedCount}個のファイルをダウンロードしました！`;
                this.statusDisplay.className = 'status-display';
            }
            
            // テキストを履歴に保存
            saveToHistory() {
                const text = this.textOutput.value;
                if (!text.trim()) {
                    this.statusDisplay.textContent = '保存するテキストがありません';
                    this.statusDisplay.className = 'status-display error';
                    return;
                }
                
                const historyItem = {
                    id: Date.now(), // ユニークなID
                    text: text,
                    date: new Date().toLocaleString('ja-JP'), // 日本語ロケールで日付をフォーマット
                    wordCount: this.countWords(text)
                };
                
                this.history.unshift(historyItem); // 配列の先頭に追加
                
                // 最大100件まで保存し、古いものから削除
                if (this.history.length > 100) {
                    this.history = this.history.slice(0, 100);
                }
                
                this.saveHistory(); // ローカルストレージに保存
                this.loadHistoryDisplay(); // 履歴表示を更新
                this.statusDisplay.textContent = '履歴に保存しました';
            }

            // 履歴のリセット
            resetHistory() {
                if (confirm('全ての履歴をリセットしてもよろしいですか？')) {
                    this.history = [];
                    this.saveHistory();
                    this.loadHistoryDisplay();
                    this.statusDisplay.textContent = '履歴をリセットしました';
                    this.statusDisplay.className = 'status-display';
                }
            }

            // 統計のリセット
            resetStats() {
                if (confirm('全ての統計データをリセットしてもよろしいですか？')) {
                    this.stats = { totalSessions: 0, totalWords: 0, totalTime: 0 };
                    this.saveStats();
                    this.updateStats();
                    this.statusDisplay.textContent = '統計データをリセットしました';
                    this.statusDisplay.className = 'status-display';
                }
            }
            
            // テンプレートをテキストエリアに挿入
            insertTemplate(template) {
                this.saveToUndoStack(); // 挿入前のテキストをアンドゥスタックに保存
                const cursorPos = this.textOutput.selectionStart; // 現在のカーソル位置
                const textBefore = this.textOutput.value.substring(0, cursorPos);
                const textAfter = this.textOutput.value.substring(cursorPos);
                
                this.textOutput.value = textBefore + template + textAfter; // テンプレートを挿入
                this.textOutput.focus(); // テキストエリアにフォーカス
                // カーソル位置をテンプレートの末尾に移動
                this.textOutput.selectionStart = this.textOutput.selectionEnd = cursorPos + template.length;
                
                this.updateCharCount();
                this.statusDisplay.textContent = 'テンプレートを挿入しました';
            }
            
            // 現在のテキストをアンドゥスタックに保存
            saveToUndoStack() {
                // 現在のテキストがスタックの最後と同じ場合は保存しない（連続入力による重複を防ぐ）
                if (this.undoStack.length > 0 && this.undoStack[this.undoStack.length - 1] === this.textOutput.value) {
                    return;
                }
                this.undoStack.push(this.textOutput.value);
                this.redoStack = []; // アンドゥした場合はリドゥスタックをクリア
                
                // 最大50件まで保存し、古いものから削除
                if (this.undoStack.length > 50) {
                    this.undoStack.shift();
                }
            }
            
            // 元に戻す (Undo)
            undo() {
                if (this.undoStack.length === 0) return;
                
                this.redoStack.push(this.textOutput.value); // 現在のテキストをリドゥスタックに保存
                this.textOutput.value = this.undoStack.pop(); // スタックから一つ前のテキストを取得
                this.updateCharCount();
                this.statusDisplay.textContent = '元に戻しました';
            }
            
            // やり直し (Redo)
            redo() {
                if (this.redoStack.length === 0) return;
                
                this.undoStack.push(this.textOutput.value); // 現在のテキストをアンドゥスタックに保存
                this.textOutput.value = this.redoStack.pop(); // スタックから一つ後のテキストを取得
                this.updateCharCount();
                this.statusDisplay.textContent = 'やり直しました';
            }
            
            // ボタンの状態をリセット
            resetButtons() {
                this.micBtn.classList.remove('listening');
                this.micBtn.disabled = false;
                this.stopBtn.disabled = true;
            }
            
            // 文字数と単語数を更新
            updateCharCount() {
                const text = this.textOutput.value;
                const charCount = text.length;
                const wordCount = this.countWords(text);
                
                this.charCount.textContent = charCount.toLocaleString();
                this.wordCount.textContent = wordCount.toLocaleString();
            }
            
            // テキストの単語数をカウント (日本語と英語で異なるロジック)
            countWords(text) {
                if (!text.trim()) return 0;
                
                // 日本語の文字が含まれている場合は文字数（空白なし）を返す
                if (/[\u3400-\u9FBF]/.test(text)) { // UnicodeのCJK統合漢字の範囲をチェック
                    return text.replace(/\s+/g, '').length;
                } else {
                    // 英語の場合はスペースで区切られた単語数を返す
                    return text.trim().split(/\s+/).length;
                }
            }

            // セッション統計を更新
            updateSessionStats() {
                if (this.sessionStartTime) {
                    const sessionDuration = (Date.now() - this.sessionStartTime) / (1000 * 60); // ミリ秒から分に変換
                    this.stats.totalTime += sessionDuration;
                    this.stats.totalSessions++;
                    this.stats.totalWords += this.countWords(this.finalTranscript);
                    this.saveStats(); // 統計を保存
                    this.updateStats(); // 統計表示を更新
                    this.sessionStartTime = null; // セッション開始時間をリセット
                }
            }

            // 統計データをローカルストレージから読み込む
            loadStats() {
                try {
                    const stats = JSON.parse(localStorage.getItem('voiceAssistantStats')) || { totalSessions: 0, totalWords: 0, totalTime: 0 };
                    return stats;
                } catch (e) {
                    console.error("Failed to load stats:", e);
                    return { totalSessions: 0, totalWords: 0, totalTime: 0 };
                }
            }

            // 統計データをローカルストレージに保存する
            saveStats() {
                localStorage.setItem('voiceAssistantStats', JSON.stringify(this.stats));
            }

            // 統計表示を更新
            updateStats() {
                this.totalSessions.textContent = this.stats.totalSessions.toLocaleString();
                this.totalWords.textContent = this.stats.totalWords.toLocaleString();
                this.totalTime.textContent = this.stats.totalTime.toFixed(1); // 小数点以下1桁で表示
            }

            // 履歴データをローカルストレージから読み込む
            loadHistory() {
                try {
                    const history = JSON.parse(localStorage.getItem('voiceAssistantHistory')) || [];
                    return history;
                } catch (e) {
                    console.error("Failed to load history:", e);
                    return [];
                }
            }

            // 履歴データをローカルストレージに保存する
            saveHistory() {
                localStorage.setItem('voiceAssistantHistory', JSON.stringify(this.history));
            }

            // 履歴リストを表示に反映
            loadHistoryDisplay() {
                this.historyList.innerHTML = ''; // 既存のリストをクリア
                if (this.history.length === 0) {
                    this.historyList.innerHTML = '<p style="text-align: center; color: #999;">まだ履歴はありません。</p>';
                    return;
                }
                this.history.forEach(item => {
                    const div = document.createElement('div');
                    div.className = 'history-item';
                    div.innerHTML = `
                        <div class="history-item-date">${item.date}</div>
                        <div class="history-item-text">${item.text}</div>
                    `;
                    // 履歴アイテムをクリックするとテキストエリアに内容をロード
                    div.addEventListener('click', () => {
                        this.textOutput.value = item.text;
                        this.updateCharCount();
                        this.statusDisplay.textContent = '履歴をロードしました';
                    });
                    this.historyList.appendChild(div);
                });
            }

            // マイク許可をチェックし、必要に応じてガイドモーダルを表示
            async checkMicrophonePermissionAndShowGuide() {
                if (!this.showMicrophoneGuideOnStartup) {
                    return; // ガイド表示設定がオフの場合は何もしない
                }

                try {
                    const permissionStatus = await navigator.permissions.query({ name: 'microphone' });

                    if (permissionStatus.state === 'granted') {
                        // マイクが既に許可されている場合はモーダルを表示しない
                        this.hasRequestedMicrophonePermission = true; // 許可されている場合もフラグを立てる
                        return;
                    } else if (permissionStatus.state === 'denied') {
                        // 許可が拒否されている場合
                        this.showMicrophoneGuideModal();
                    } else if (permissionStatus.state === 'prompt') {
                        // 許可を求められる状態の場合
                        // アプリ起動時に一度もマイク許可を要求していなければ、ここで要求する
                        if (!this.hasRequestedMicrophonePermission) {
                            try {
                                // recognition.start() を呼び出すことで、ブラウザのマイク許可プロンプトが表示される
                                // ただし、ここでは実際に録音を開始せず、許可プロンプトのトリガーのみを目的とする
                                // そのため、すぐに recognition.abort() を呼び出す
                                this.recognition.start();
                                this.recognition.abort(); // 許可プロンプト表示後すぐに停止
                            } catch (e) {
                                console.warn("Failed to trigger microphone permission prompt:", e);
                                // エラーが発生した場合も、ユーザーにガイドを表示する
                                this.showMicrophoneGuideModal();
                            }
                            this.hasRequestedMicrophonePermission = true; // 要求フラグを立てる
                        }
                    }
                } catch (error) {
                    console.error('マイク許可の確認中にエラーが発生しました:', error);
                    // エラーが発生した場合もガイドを表示する
                    this.showMicrophoneGuideModal();
                }
            }

            // マイクガイドモーダルを表示
            showMicrophoneGuideModal() {
                this.microphoneGuideModal.classList.add('active');
            }

            // マイクガイドモーダルを非表示
            hideMicrophoneGuideModal() {
                this.microphoneGuideModal.classList.remove('active');
            }

            // マイクガイド表示設定をローカルストレージに保存
            saveMicrophoneGuideSetting() {
                localStorage.setItem('showMicrophoneGuide', JSON.stringify(this.showMicrophoneGuideOnStartup));
            }

            // マイクガイド表示設定をローカルストレージからロード
            loadMicrophoneGuideSetting() {
                try {
                    const setting = localStorage.getItem('showMicrophoneGuide');
                    // デフォルトはtrue（表示する）
                    return setting === null ? true : JSON.parse(setting);
                } catch (e) {
                    console.error("Failed to load microphone guide setting:", e);
                    return true; // エラー時はデフォルトで表示する
                }
            }

            // ダウンロード形式設定をローカルストレージからロード
            loadDownloadFormatSettings() {
                try {
                    const settings = JSON.parse(localStorage.getItem('downloadFormatSettings')) || {};
                    // デフォルトはtxtのみtrue
                    if (Object.keys(settings).length === 0) {
                        return { txt: true, md: false, html: false, json: false, csv: false };
                    }
                    return settings;
                } catch (e) {
                    console.error("Failed to load download format settings:", e);
                    return { txt: true, md: false, html: false, json: false, csv: false };
                }
            }

            // ダウンロード形式設定をローカルストレージに保存
            saveDownloadFormatSettings() {
                const settings = {};
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    settings[checkbox.value] = checkbox.checked;
                });
                localStorage.setItem('downloadFormatSettings', JSON.stringify(settings));
            }

            // ダウンロード形式設定をUIに適用
            applyDownloadFormatSettings() {
                this.downloadFormatCheckboxes.forEach(checkbox => {
                    checkbox.checked = this.downloadFormats[checkbox.value] || false;
                });
            }
        }

        // DOMContentLoadedイベントでVoiceAssistantProクラスを初期化
        document.addEventListener('DOMContentLoaded', () => {
    const OPENAI_API_KEY = "YOUR_API_KEY_HERE"; // ←ここにAPIキーを入力してください

    const summarizeBtn = document.getElementById("summarizeBtn");
    const textOutput = document.getElementById("textOutput"); 
    const statusDisplay = document.getElementById("statusDisplay"); 

    summarizeBtn.addEventListener("click", async () => {
      const originalText = textOutput.value.trim();
      if (!originalText) {
        statusDisplay.textContent = "要約するテキストがありません";
        statusDisplay.className = "status-display error";
        return;
      }

      statusDisplay.textContent = "要約中...";
      statusDisplay.className = "status-display listening";

      try {
        const response = await fetch("https://api.openai.com/v1/chat/completions", {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
            "Authorization": `Bearer ${OPENAI_API_KEY}`
          },
          body: JSON.stringify({
            model: "gpt-3.5-turbo",
            messages: [
              { role: "system", content: "以下のテキストを要点だけ5行以内でまとめてください。" },
              { role: "user", content: originalText }
            ],
            temperature: 0.5
          })
        });

        const data = await response.json();
        const summary = data.choices?.[0]?.message?.content?.trim();
        if (summary) {
          textOutput.value += "\n\n---\n🧠 要約:\n" + summary;
          statusDisplay.textContent = "要約が完了しました";
          statusDisplay.className = "status-display";
        } else {
          throw new Error("要約結果が取得できませんでした");
        }
      } catch (err) {
        console.error("要約エラー:", err);
        statusDisplay.textContent = "要約に失敗しました: " + err.message;
        statusDisplay.className = "status-display error";
      }
    });

            new VoiceAssistantPro();
        });
    </script>
</body>
</html>
```

---
