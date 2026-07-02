# Ledger API

Backend RESTful API untuk aplikasi **General Ledger** menggunakan **Golang**, **Gin**, **GORM**, dan **MySQL**.

---

# Teknologi

* Go 1.25+
* Gin Framework
* GORM
* MySQL
* JWT Authentication
* Bcrypt
* Validator
* Viper
* Swagger (Swaggo)
* Goose Migration
* Air (Hot Reload)

---

# Persiapan

Pastikan telah menginstall:

* Go 1.25+
* Git
* MySQL
* Visual Studio Code (atau IDE favorit)

---

# Langkah 1 - Inisialisasi Go Module

```bash
go mod init github.com/teddyjuanda/ledger-api
```

---

# Langkah 2 - Install Dependency

## Gin Framework

```bash
go get github.com/gin-gonic/gin
```

## GORM

```bash
go get gorm.io/gorm
go get gorm.io/driver/mysql
```

## JWT Authentication

```bash
go get github.com/golang-jwt/jwt/v5
```

## Bcrypt

```bash
go get golang.org/x/crypto/bcrypt
```

## Validator

```bash
go get github.com/go-playground/validator/v10
```

## Viper

```bash
go get github.com/spf13/viper
```

## Swagger

```bash
go get github.com/swaggo/swag/cmd/swag
go get github.com/swaggo/gin-swagger
go get github.com/swaggo/files
```

---

# Langkah 3 - Install Tools Global

## Air (Hot Reload)

Install

```bash
go install github.com/air-verse/air@latest
```

Generate konfigurasi

```bash
air init
```

Menjalankan project

```bash
air
```

---

## Goose (Migration)

Install

```bash
go install github.com/pressly/goose/v3/cmd/goose@latest
```

---

# Struktur Project

```text
ledger-api/

├── cmd/
│   └── api/
│       └── main.go
│
├── configs/
│   └── config.go
│
├── docs/
│
├── internal/
│   ├── router/
│   ├── middleware/
│   ├── models/
│   └── controllers/
│       ├── auth/
│       ├── coa/
│       ├── cost_center/
│       ├── dashboard/
│       ├── data_indicator/
│       ├── department/
│       ├── depo/
│       ├── division/
│       ├── fiscal_period/
│       ├── journal/
│       ├── journal_source/
│       ├── ledger/
│       ├── posting_balance/
│       ├── product/
│       ├── product_mapped/
│       ├── profile/
│       ├── report/
│       ├── repository/
│       ├── sales/
│       ├── segment/
│       ├── service/
│       ├── trial_balance/
│       ├── unpost_journal/
│       └── user/
│
├── migrations/
├── pkg/
│
├── .env
├── .gitignore
├── go.mod
└── go.sum
```

---

# Membuat Struktur Folder

Jalankan perintah berikut pada PowerShell.

```powershell
mkdir `
cmd\api,`
configs,`
docs,`
internal,`
internal\router,`
internal\middleware,`
internal\models,`
internal\controllers,`
internal\controllers\auth,`
internal\controllers\coa,`
internal\controllers\cost_center,`
internal\controllers\dashboard,`
internal\controllers\data_indicator,`
internal\controllers\department,`
internal\controllers\depo,`
internal\controllers\division,`
internal\controllers\fiscal_period,`
internal\controllers\journal,`
internal\controllers\journal_source,`
internal\controllers\ledger,`
internal\controllers\posting_balance,`
internal\controllers\product,`
internal\controllers\product_mapped,`
internal\controllers\profile,`
internal\controllers\report,`
internal\controllers\repository,`
internal\controllers\sales,`
internal\controllers\segment,`
internal\controllers\service,`
internal\controllers\trial_balance,`
internal\controllers\unpost_journal,`
internal\controllers\user,`
pkg,`
migrations
```

---

# Membuat File Awal

```powershell
New-Item -ItemType File -Path `
cmd/api/main.go,`
configs/config.go,`
.env
```

---

# Menjalankan Project

```bash
air
```

atau

```bash
go run cmd/api/main.go
```

---

# Roadmap Pengembangan

Tahapan pengembangan project ini akan dilakukan secara bertahap.

1. Konfigurasi aplikasi (.env)
2. Koneksi Database MySQL
3. GORM
4. Logger
5. JWT Authentication
6. Middleware Authentication
7. Role & Permission
8. Swagger
9. CRUD User
10. Chart of Account (COA)
11. Journal
12. General Ledger
13. Trial Balance
14. Reporting
15. Deployment Production
