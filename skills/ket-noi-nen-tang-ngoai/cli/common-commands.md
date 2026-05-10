# CLI Commands Phổ Biến

## GitHub CLI (`gh`)
```bash
gh repo list                          # Liệt kê repos
gh issue list --repo owner/repo       # Liệt kê issues
gh pr create --title "..." --body "..." # Tạo PR
gh pr list                            # Liệt kê PRs
```

## Google Cloud (`gcloud`)
```bash
gcloud auth login                     # Đăng nhập
gcloud projects list                  # Liệt kê projects
gcloud config set project PROJECT_ID  # Chọn project
```

## AWS CLI (`aws`)
```bash
aws configure                         # Cấu hình credentials
aws s3 ls                             # Liệt kê S3 buckets
aws ec2 describe-instances            # Liệt kê EC2
```

## Docker (`docker`)
```bash
docker ps                             # Containers đang chạy
docker images                         # Liệt kê images
docker run -it IMAGE_NAME bash        # Chạy container
docker compose up -d                  # Khởi động services
```

## npm / npx
```bash
npm install PACKAGE                   # Cài package
npx PACKAGE args                      # Chạy package không cài
npm run SCRIPT                        # Chạy script từ package.json
```
