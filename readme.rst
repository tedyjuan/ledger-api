
Langkah 1: Inisialisasi Module & Instal Dependensi
# 1. Inisialisasi Go Module
go mod init github.com/teddyjuanda/ledger-api

# 2. Instal Gin (Framework HTTP)
go get -u github.com/gin-gonic/gin

# 3. Instal GORM (ORM) dan Driver MySQL
go get -u gorm.io/gorm
go get -u gorm.io/driver/mysql

# 4. Instal JWT, Bcrypt, Validator, dan Viper (Config)
go get -u github.com/golang-jwt/jwt/v5
xl/crypto/bcrypt # (Bcrypt bawaan dari golang.org/x/crypto/bcrypt)
go get -u golang.org/x/crypto/bcrypt
go get -u github.com/go-playground/validator/v10
go get -u github.com/spf13/viper

# 5. Instal Swaggo (Swagger) untuk dokumentasi API
go get -u github.com/swaggo/swag/cmd/swag
go get -u github.com/swaggo/gin-swagger
go get -u github.com/swaggo/files

Langkah 2: Instal Alat Global (Goose & Air)
go install github.com/air-verse/air@latest
air init
go install github.com/pressly/goose/v3/cmd/goose@latest

struktur project folder 
ledger-api/

├── cmd/
│   └── api/
│       └── main.go
│
├── config/
├── docs/
├── internal/
│   ├── auth/
│   ├── middleware/
│   ├── user/
│   ├── repository/
│   ├── service/
│   └── handler/
│
├── pkg/
├── migrations/
├── .env
├── .gitignore
├── go.mod
└── go.sum