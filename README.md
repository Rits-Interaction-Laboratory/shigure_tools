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

