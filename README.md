# Shigure Tools

Shigure関連のシェルスクリプト

## Setup

---

リポジトリの取得 <br>
```bash
git clone git@github.com:Rits-Interaction-Laboratory/shigure_tools.git
```

`~/.bashrc` に追記 <br>
`shigure_tools_clone_path`には、このリポジトリをcloneしたディレクトリのパスを記述 <br>
```bash
# ROS Settings
shigure_tools_clone_path="$HOME"
if [ -f "$shigure_tools_clone_path/shigure_tools/.ros_config" ]; then
    . "$shigure_tools_clone_path/shigure_tools/.ros_config"
fi
```

## 各種コマンド

---

**ROSのパスを通すコマンド** <br>
```sh
${ros version}-setup

(example)
foxy-setup
```

**ROS_DOMAIN_IDを変更するためのコマンド** <br>
```sh
change_domain_id ${変更するROS_DOMAIN_ID}

(example)
change_domain_id 20
```

**shigureの各機能を起動するためのコマンド** <br>
shigure_coreの各ノードを個別に起動する <br>
(ただし, paramファイルが下記ディレクトリ以下に置かれていることを前提としています。) <br>
`~/ros2_ws/src/shigure_core/shigure_core/shigure_core/nodes/params` <br>

```sh
shigure ${ノード名}

(example)
shigure bg_subtraction
shigure subtraction_analysis
shigure object_detection
shigure object_tracking
shigure people_tracking
shigure contact_detection
shigure record_event
shigure pose_save
```

<br>

記録用ノードを除くshigure_coreのすべてのノードを起動する <br>
```sh
shigure launch
```

<br>

骨格情報保存の開始、終了を行う <br>
```sh
[開始]
shigure pose_start

[終了]
shigure pose_end
```

<br>

データベースへの記録用ノードを起動する <br>
```sh
shigure record
```

<br>

HoloLens向け記録情報送信用のサービスを起動する <br>
```sh
shigure service
```




