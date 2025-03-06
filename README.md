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
- Pylance

## 安裝Python
安裝最新(https://www.python.org/downloads/)  
要注意記得勾選安裝環境變數  
會連同pip一起安裝  
安裝完畢後開啟cmd`搜尋那邊打cmd`  
``` 
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
如何使用venv建立virtual environments  
首先，創建一個資料夾(存放Venv的地方)  
然後在那個資料夾路徑下開啟cmd(在資料夾上方搜尋的地方輸入cmd按enter)  
在cmd輸入以下程式碼  
```
python -m venv 自定義名稱
```

![cmd-venv](https://github.com/rgatsai/Python-VS-Code-/blob/main/image/cmd-venv.png)
### 啟動virtual environments
activate.bat存放於scripts\activate.bat
```
test\scripts\activate.bat
```
但我們會用VS Code來開啟虛擬環境，  
所以這個學會就好。
## VS Code架設環境
隨便新增一個python的檔案  
這邊以test.py為例  
**很重要，以下都要用.py檔案作測試**
打開VS Code，先去安裝延伸模組，總共要裝以下套件(如果不會安裝再提問)
- Pylint
- Python Debugger
- Ruff
- Pylance

如果有成功安裝Pylint，你的程式碼會出現毛毛蟲(因為python排版較嚴謹)，代表安裝成功  
如果有成功安裝Python Debugger 就可以下中斷點偵錯  
安裝完畢後，左下角齒輪點開-設定，右上角開啟設定json編輯    
這是Preferences: Open User Settings可以設置環境的地方  
請設置的跟我一樣，[setting.json](https://github.com/rgatsai/Python-VScode/blob/main/settings.json)  

"github.copilot.advanced": {  
"authProvider": "github"  
},(這段不要)  

"python.venvPath": "D:\\python_venv\\test",記得使用自己的路徑  

![vscode-setting](https://github.com/rgatsai/Python-VScode/blob/main/image/vscode-setting.png)

儲存重開VS Code    
然後快捷鍵`ctrl+shift+p`，輸入python select interpreter 找到我們剛剛創建的虛擬環境裡的python  
(選後面藍字是venv的)  
手動設定這一次就好，設定完後重啟終端機(你的終端機會有黃色驚嘆號，跟著提示重啟)

![select interpreter](https://github.com/rgatsai/Python-VScode/blob/main/image/vscode-select-interpreter.jpg)

如何確認環境設定成功?  
執行print("Hello World")後，確認終端機的環境是在venv的路徑下剛剛建置的環境   
例:test/scripts/python

![vscode-setting2](https://github.com/rgatsai/Python-VScode/blob/main/image/vscode-setting2.png)

記得剛剛設置的Ruff嗎?這邊輸入很醜的程式碼如下:  
```
a= 1
b =2
c=a+b
```
`ctrl+s`儲存後能夠自動排版代表Ruff執行成功  
若之後需要使用不同版本的python，再教各位如何切換多個虛擬環境 :nerd_face:
