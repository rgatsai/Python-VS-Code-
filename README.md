# Python-VS-Code
如何安裝Python和創建虛擬環境，使用VS Code開發，跟一些延伸模組。
## 說明
簡單Python使用VS Code開發的環境建置，需要安裝以下項目
- VS Code
- Python
- Venv
  
Vscode套件:
- Pylint
- Python Debugger
- Ruff
## 安裝Python
安裝最新(https://www.python.org/downloads/)  
要注意記得勾選安裝環境變數  
會連同pip一起安裝  
安裝完畢後開啟cmd`搜尋那邊打cmd`  
```cmd 
python
```
會顯示目前安裝的Python版本
```
pip --version
``` 
會顯示目前安裝的版本號  
確認有無安裝成功

![cmd-python](https://github.com/rgatsai/Python-VS-Code-/blob/main/image/cmd-python-pip.png)

## Venv
如何只用venv建立virtual environments  
首先，創建一個資料夾(存放Venv的地方)  
然後在那個資料夾路徑下開啟cmd(在資料夾上方搜尋的地方輸入cmd按enter)  
在cmd輸入以下程式碼  
```
python -m venv 自定義名稱
```
![cmd-venv](https://github.com/rgatsai/Python-VS-Code-/blob/main/image/cmd-venv.png)
