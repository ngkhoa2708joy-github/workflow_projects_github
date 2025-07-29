# Bước 1: Tạo virtual environment
Bước 1: 
python -m venv venv

Bước 2: Kích hoạt venv
Windows (PowerShell)
```
venv\Scripts\activate
```
Linux / MacOS
```
source venv/bin/activate
```

Bước 3: Cài thư viện
pip install -r requirements.txt

Bước 4: Thoát venv khi xong
deactivate

# 2. Ghi dependency vào requirements.txt
Khi cài thêm thư viện mới (ví dụ Flask):
```yami
pip install flask
pip freeze > requirements.txt
```

# 3. Thiết lập venv trong VS Code
Cài Python Extension trong VS Code.
```
Nhấn Ctrl + Shift + P → Python: Select Interpreter → chọn ./venv
```
Mỗi khi mở project, VS Code sẽ tự động sử dụng venv.

# 4. Cập nhật .gitignore
Để không push venv lên Git:
```
# .gitignore
venv/
__pycache__/
*.pyc
```
# 📂 Ví dụ cấu trúc thư mục đầy đủ
```
project-name/
├── .vscode/              
├── docs/                 
├── src/                  
├── tests/                
├── venv/                 # virtual environment (bị ignore trong git)
├── .gitignore            
├── requirements.txt      
├── README.md             
└── CONTRIBUTING.md
```
