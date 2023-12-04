
# Debugger Asset
Unityでの開発で利用できるデバッグ機能を提供します。
MITライセンスにて公開しています。
ライセンスの範囲で自由にご活用ください。

## 導入方法
以下の２つの方法での導入をサポートしています。

### Unity Package Managerで追加
プロジェクトフォルダ > `Packages` > `manifest.json` の`dependencies` に以下を追加します。<br>
※　元から書いてある行は削除しない

```
{
  "dependencies": {
    ・
    ・[書いてある行は消さない]
    ・↓この行を追記する
    "jp.dump.debugger":"git@github.com:SekikawaHayato/OpenDebuggerAsset.git"
  }
}
```

### Unitypackageで追加
[こちら](https://drive.google.com/file/d/1uQKIEbEhPFlocvv5pEvN_QM3ZEU7Cpcj/view?usp=sharing)から最新のunitypackageをダウンロードしてください。
ダウンロードしたパッケージをご自身のプロジェクトへインポートすることで利用できます。


## 使い方
### Debugger
Debuggerは [Editor上のみ] / [DEVELOP環境でのみ]コンソールへ出力したい場合に利用します。
各種 `Log` / `LogWarning` / `LogError` の３つの出力を準備しています。

使用例）Logの出力
- Editor上のみ<br>

`Debug.Log()`を記述している場所を以下のように書き換えることでUnityEditor上でのみ出力されるLogになります。
```
Debugger.UnityOnlyLog("出力するオブジェクト");
```

- DEVELOP環境のみ<br>

`Project Settings` > `Player` > `OtherSettings` > `Scripting Define Symbols` に`DEVELOP` を追加します。

<img src="https://github.com/SekikawaHayato/DebuggerAsset/assets/48428983/f2278e42-d9b8-4724-bb99-49e550cf8d11">


<br>

`Debug.Log()`を記述している場所を以下のように書き換えることでUnityEditor上でのみ出力されるLogになります。
```
Debugger.DevelopmentOnlyLog("出力するオブジェクト");
```
---

### DebugPanel
以下のプレハブをシーンに配置してください。<br>
`DebuggerAsset` > `Runtime` > `Prefabs` > `DebugPanel`

<br>
 Inspectorで指定したシーンを表示する機能とConsole出力を確認できる機能を提供しています。

![Debugger](https://github.com/SekikawaHayato/DebuggerAsset/assets/48428983/647c5f00-798b-47b1-9529-e8a65b8d48ce)




