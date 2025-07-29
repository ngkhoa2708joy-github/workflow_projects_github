# workflow_projects_github
Workflow for team project using github 

## 1. Chuẩn bị môi trường
- Tạo repo Git
- Cấu trúc thư mục:
project-name/
├── .vscode/
├── docs/
├── src/
├── tests/
├── .gitignore
├── requirements.txt / package.json
├── README.md
└── CONTRIBUTING.md


## 2. Git Workflow
Nhánh chính:
- main → code ổn định
Tạo nhánh mới theo format:
- develop → code đang phát triển
- feature/<tính-năng>
- bugfix/<tên-lỗi>

## 3. Quy tắc code
- Sử dụng formatter/linter
- Extensions: GitLens, Prettier, ESLint/Flake8, Live Share

## 4. Testing
- Thư mục `tests/`
- Dùng pytest / jest
- CI/CD kiểm tra test tự động

## 5. CI/CD
Ví dụ GitHub Actions cho Python:
```yaml
name: Python CI
on: [push, pull_request]
jobs:
build:
  runs-on: ubuntu-latest
  steps:
    - uses: actions/checkout@v3
    - uses: actions/setup-python@v4
      with:
        python-version: '3.11'
    - run: pip install -r requirements.txt
    - run: pytest
```

## 6. Triển khai
Mời team vào repo
Vào GitHub → Settings → Collaborators
Add email hoặc username GitHub của từng thành viên.
