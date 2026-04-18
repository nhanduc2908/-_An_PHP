# 📁 CẤU TRÚC HOÀN CHỈNH - SECURITY ASSESSMENT PLATFORM

Dưới đây là **cấu trúc file hoàn chỉnh và chi tiết nhất** của dự án Security Assessment Platform:

---

## 🗺️ SƠ ĐỒ CẤU TRÚC TỔNG THỂ

```
security-assessment-platform/
│
├── 📄 .env.example
├── 📄 .gitignore
├── 📄 docker-compose.yml
├── 📄 Makefile
├── 📄 README.md
│
├── 📁 backend/                    # 🐘 PHP Backend (Core API)
├── 📁 frontend/                   # 🎨 HTML/CSS/JS Frontend
├── 📁 realtime/                   # 🔌 Node.js WebSocket Server
├── 📁 database/                   # 🗄️ SQL Scripts
├── 📁 docs/                       # 📚 Documentation
├── 📁 scripts/                    # 🔧 Utility Scripts
├── 📁 .github/                    # 🤖 CI/CD Workflows
├── 📁 .docker/                    # 🐳 Docker Configs
└── 📁 .k8s/                       # ☸️ Kubernetes Manifests
```

---

## 📂 CHI TIẾT TỪNG THƯ MỤC

### **1. BACKEND (PHP)**

```
backend/
│
├── 📄 index.php
├── 📄 .htaccess
├── 📄 composer.json
├── 📄 artisan
│
├── 📁 api/                        # API Routes (17 files)
│   ├── 📄 v1.php
│   ├── 📄 auth.php
│   ├── 📄 users.php
│   ├── 📄 roles.php
│   ├── 📄 permissions.php
│   ├── 📄 servers.php
│   ├── 📄 categories.php
│   ├── 📄 criteria.php
│   ├── 📄 assessments.php
│   ├── 📄 vulnerabilities.php
│   ├── 📄 alerts.php
│   ├── 📄 reports.php
│   ├── 📄 dashboard.php
│   ├── 📄 backup.php
│   ├── 📄 profile.php
│   ├── 📄 audit.php
│   └── 📄 settings.php
│
├── 📁 core/                       # Core Framework (15 files)
│   ├── 📄 Autoload.php
│   ├── 📄 Router.php
│   ├── 📄 Controller.php
│   ├── 📄 Model.php
│   ├── 📄 Database.php
│   ├── 📄 JWT.php
│   ├── 📄 Middleware.php
│   ├── 📄 RBAC.php
│   ├── 📄 Validator.php
│   ├── 📄 Logger.php
│   ├── 📄 Cache.php
│   ├── 📄 Encryption.php
│   ├── 📄 Event.php
│   ├── 📄 Queue.php
│   └── 📄 Helper.php
│
├── 📁 controllers/                # Controllers (16 files)
│   ├── 📄 AuthController.php
│   ├── 📄 UserController.php
│   ├── 📄 RoleController.php
│   ├── 📄 PermissionController.php
│   ├── 📄 ServerController.php
│   ├── 📄 CategoryController.php
│   ├── 📄 CriteriaController.php
│   ├── 📄 AssessmentController.php
│   ├── 📄 VulnerabilityController.php
│   ├── 📄 AlertController.php
│   ├── 📄 ReportController.php
│   ├── 📄 DashboardController.php
│   ├── 📄 BackupController.php
│   ├── 📄 ProfileController.php
│   ├── 📄 AuditController.php
│   └── 📄 SettingController.php
│
├── 📁 models/                     # Models (16 files)
│   ├── 📄 User.php
│   ├── 📄 Role.php
│   ├── 📄 Permission.php
│   ├── 📄 Server.php
│   ├── 📄 Category.php
│   ├── 📄 Criteria.php
│   ├── 📄 AssessmentResult.php
│   ├── 📄 AssessmentReport.php
│   ├── 📄 Vulnerability.php
│   ├── 📄 Alert.php
│   ├── 📄 AuditLog.php
│   ├── 📄 Backup.php
│   ├── 📄 Setting.php
│   ├── 📄 Session.php
│   ├── 📄 Token.php
│   └── 📄 Notification.php
│
├── 📁 middleware/                 # Middleware (10 files)
│   ├── 📄 AuthMiddleware.php
│   ├── 📄 PermissionMiddleware.php
│   ├── 📄 RateLimitMiddleware.php
│   ├── 📄 CorsMiddleware.php
│   ├── 📄 SecurityHeadersMiddleware.php
│   ├── 📄 GuestMiddleware.php
│   ├── 📄 LogMiddleware.php
│   ├── 📄 CacheMiddleware.php
│   ├── 📄 MaintenanceMiddleware.php
│   └── 📄 JsonMiddleware.php
│
├── 📁 services/                   # Services (12 files)
│   ├── 📄 AuthService.php
│   ├── 📄 ScannerService.php
│   ├── 📄 ScoreCalculatorService.php
│   ├── 📄 AttackDetectorService.php
│   ├── 📄 SshConnectionService.php
│   ├── 📄 ApiCallService.php
│   ├── 📄 FileUploadService.php
│   ├── 📄 BackupService.php
│   ├── 📄 RealtimeService.php
│   ├── 📄 ReportGeneratorService.php
│   ├── 📄 NotificationService.php
│   └── 📄 ImportExportService.php
│
├── 📁 repositories/               # Repositories (6 files)
│   ├── 📄 UserRepository.php
│   ├── 📄 ServerRepository.php
│   ├── 📄 CriteriaRepository.php
│   ├── 📄 AssessmentRepository.php
│   ├── 📄 AlertRepository.php
│   └── 📄 ReportRepository.php
│
├── 📁 jobs/                       # Queue Jobs (8 files)
│   ├── 📄 ScanServerJob.php
│   ├── 📄 SendEmailJob.php
│   ├── 📄 GenerateReportJob.php
│   ├── 📄 BackupDatabaseJob.php
│   ├── 📄 CleanupLogsJob.php
│   ├── 📄 SyncServersJob.php
│   ├── 📄 CheckVulnerabilitiesJob.php
│   └── 📄 SendAlertJob.php
│
├── 📁 listeners/                  # Event Listeners (6 files)
│   ├── 📄 SendLoginNotification.php
│   ├── 📄 LogUserAction.php
│   ├── 📄 CreateAuditTrail.php
│   ├── 📄 SendAlertOnVulnerability.php
│   ├── 📄 UpdateDashboardCache.php
│   └── 📄 PushRealtimeEvent.php
│
├── 📁 exceptions/                 # Custom Exceptions (8 files)
│   ├── 📄 ValidationException.php
│   ├── 📄 AuthException.php
│   ├── 📄 PermissionException.php
│   ├── 📄 NotFoundException.php
│   ├── 📄 DatabaseException.php
│   ├── 📄 ScanException.php
│   ├── 📄 BackupException.php
│   └── 📄 ApiException.php
│
├── 📁 config/                     # Configuration (12 files)
│   ├── 📄 app.php
│   ├── 📄 database.php
│   ├── 📄 jwt.php
│   ├── 📄 rbac.php
│   ├── 📄 criteria_categories.php
│   ├── 📄 criteria_280.php
│   ├── 📄 menu.php
│   ├── 📄 mail.php
│   ├── 📄 cache.php
│   ├── 📄 queue.php
│   ├── 📄 filesystems.php
│   └── 📄 services.php
│
├── 📁 lang/                       # Language Files (3 languages x 4 files)
│   ├── 📁 en/
│   │   ├── 📄 auth.php
│   │   ├── 📄 validation.php
│   │   ├── 📄 criteria.php
│   │   └── 📄 messages.php
│   ├── 📁 vi/
│   │   ├── 📄 auth.php
│   │   ├── 📄 validation.php
│   │   ├── 📄 criteria.php
│   │   └── 📄 messages.php
│   └── 📁 ja/
│       ├── 📄 auth.php
│       ├── 📄 validation.php
│       ├── 📄 criteria.php
│       └── 📄 messages.php
│
├── 📁 storage/                    # Storage
│   ├── 📁 logs/                   # Log files (9 files)
│   │   ├── 📄 app.log
│   │   ├── 📄 auth.log
│   │   ├── 📄 scan.log
│   │   ├── 📄 error.log
│   │   ├── 📄 attack.log
│   │   ├── 📄 api.log
│   │   ├── 📄 database.log
│   │   ├── 📄 cron.log
│   │   └── 📄 debug.log
│   ├── 📁 uploads/                # Upload directories (4 folders)
│   │   ├── 📁 evidence/
│   │   ├── 📁 reports/
│   │   ├── 📁 avatars/
│   │   └── 📁 temp/
│   ├── 📁 backups/                # Backups (2 folders)
│   │   ├── 📁 database/
│   │   └── 📁 files/
│   ├── 📁 cache/
│   └── 📁 framework/
│       ├── 📁 sessions/
│       ├── 📁 cache/
│       └── 📁 views/
│
├── 📁 bootstrap/                  # Bootstrap (3 files)
│   ├── 📄 app.php
│   ├── 📄 routes.php
│   └── 📄 middleware.php
│
├── 📁 database/                   # Database
│   ├── 📁 migrations/             # 36 migration files
│   │   ├── 📄 2024_01_01_000001_create_users_table.php
│   │   ├── 📄 2024_01_01_000002_create_roles_table.php
│   │   ├── 📄 2024_01_01_000003_create_permissions_table.php
│   │   ├── 📄 2024_01_01_000004_create_role_permission_table.php
│   │   ├── 📄 2024_01_01_000005_create_categories_table.php
│   │   ├── 📄 2024_01_01_000006_create_criteria_table.php
│   │   ├── 📄 2024_01_01_000007_create_servers_table.php
│   │   ├── 📄 2024_01_01_000008_create_user_server_table.php
│   │   ├── 📄 2024_01_01_000009_create_assessment_results_table.php
│   │   ├── 📄 2024_01_01_000010_create_assessment_reports_table.php
│   │   ├── 📄 2024_01_01_000011_create_vulnerabilities_table.php
│   │   ├── 📄 2024_01_01_000012_create_vulnerability_history_table.php
│   │   ├── 📄 2024_01_01_000013_create_alerts_table.php
│   │   ├── 📄 2024_01_01_000014_create_alert_notes_table.php
│   │   ├── 📄 2024_01_01_000015_create_audit_logs_table.php
│   │   ├── 📄 2024_01_01_000016_create_login_attempts_table.php
│   │   ├── 📄 2024_01_01_000017_create_user_sessions_table.php
│   │   ├── 📄 2024_01_01_000018_create_password_resets_table.php
│   │   ├── 📄 2024_01_01_000019_create_backups_table.php
│   │   ├── 📄 2024_01_01_000020_create_system_settings_table.php
│   │   ├── 📄 2024_01_01_000021_create_notifications_table.php
│   │   ├── 📄 2024_01_01_000022_create_attack_logs_table.php
│   │   ├── 📄 2024_01_01_000023_create_blocked_ips_table.php
│   │   ├── 📄 2024_01_01_000024_create_cve_cache_table.php
│   │   ├── 📄 2024_01_01_000025_create_api_logs_table.php
│   │   ├── 📄 2024_01_01_000026_create_rate_limits_table.php
│   │   ├── 📄 2024_01_01_000027_create_report_schedules_table.php
│   │   ├── 📄 2024_01_01_000028_create_jobs_table.php
│   │   ├── 📄 2024_01_01_000029_create_failed_jobs_table.php
│   │   ├── 📄 2024_01_15_000001_add_indexes_to_users_table.php
│   │   ├── 📄 2024_01_15_000002_add_indexes_to_criteria_table.php
│   │   ├── 📄 2024_01_15_000003_add_indexes_to_assessment_results_table.php
│   │   ├── 📄 2024_01_15_000004_add_indexes_to_alerts_table.php
│   │   ├── 📄 2024_01_15_000005_add_indexes_to_audit_logs_table.php
│   │   ├── 📄 2024_01_15_000006_add_foreign_keys_table.php
│   │   ├── 📄 2024_01_20_000001_add_two_factor_fields_to_users_table.php
│   │   ├── 📄 2024_01_20_000002_add_soft_deletes_to_servers_table.php
│   │   └── 📄 2024_01_20_000003_add_status_to_assessment_reports_table.php
│   └── 📁 seeds/                   # 7 seeders
│       ├── 📄 DatabaseSeeder.php
│       ├── 📄 RoleSeeder.php
│       ├── 📄 PermissionSeeder.php
│       ├── 📄 CategorySeeder.php
│       ├── 📄 CriteriaSeeder.php
│       ├── 📄 UserSeeder.php
│       └── 📄 ServerSeeder.php
│
├── 📁 tests/                      # Tests (11 files)
│   ├── 📁 Unit/
│   │   ├── 📄 AuthTest.php
│   │   ├── 📄 RBACTest.php
│   │   ├── 📄 CriteriaTest.php
│   │   ├── 📄 ScoreCalculatorTest.php
│   │   └── 📄 ScannerTest.php
│   ├── 📁 Feature/
│   │   ├── 📄 ApiAuthTest.php
│   │   ├── 📄 ApiCriteriaTest.php
│   │   ├── 📄 ApiAssessmentTest.php
│   │   └── 📄 ApiReportTest.php
│   ├── 📁 Integration/
│   │   ├── 📄 DatabaseTest.php
│   │   └── 📄 QueueTest.php
│   ├── 📄 TestCase.php
│   └── 📄 CreatesApplication.php
│
├── 📄 phpunit.xml
└── 📄 artisan
```

---

### **2. FRONTEND (HTML/CSS/JS)**

```
frontend/
│
├── 📄 index.html
│
├── 📁 pages/                      # HTML Pages (28 files)
│   ├── 📄 login.html
│   ├── 📄 404.html
│   ├── 📄 dashboard.html
│   ├── 📄 servers.html
│   ├── 📄 servers-add.html
│   ├── 📄 servers-edit.html
│   ├── 📄 servers-detail.html
│   ├── 📄 categories.html
│   ├── 📄 criteria.html
│   ├── 📄 criteria-add.html
│   ├── 📄 criteria-edit.html
│   ├── 📄 criteria-import.html
│   ├── 📄 assessments.html
│   ├── 📄 assessment-run.html
│   ├── 📄 assessment-detail.html
│   ├── 📄 vulnerabilities.html
│   ├── 📄 alerts.html
│   ├── 📄 users.html
│   ├── 📄 users-add.html
│   ├── 📄 users-edit.html
│   ├── 📄 roles.html
│   ├── 📄 backup.html
│   ├── 📄 reports.html
│   ├── 📄 report-detail.html
│   ├── 📄 profile.html
│   └── 📄 settings.html
│
├── 📁 assets/
│   ├── 📁 css/                    # CSS Files (7 files)
│   │   ├── 📄 main.css
│   │   ├── 📄 admin.css
│   │   ├── 📄 dashboard.css
│   │   ├── 📄 criteria.css
│   │   ├── 📄 responsive.css
│   │   ├── 📄 dark-mode.css
│   │   └── 📄 print.css
│   │
│   ├── 📁 js/                     # JavaScript Files (20 files)
│   │   ├── 📄 app.js
│   │   ├── 📄 api.js
│   │   ├── 📄 auth.js
│   │   ├── 📄 rbac.js
│   │   ├── 📄 utils.js
│   │   ├── 📄 dashboard.js
│   │   ├── 📄 servers.js
│   │   ├── 📄 categories.js
│   │   ├── 📄 criteria.js
│   │   ├── 📄 assessments.js
│   │   ├── 📄 alerts.js
│   │   ├── 📄 users.js
│   │   ├── 📄 roles.js
│   │   ├── 📄 backup.js
│   │   ├── 📄 reports.js
│   │   ├── 📄 profile.js
│   │   ├── 📄 socket.js
│   │   ├── 📄 charts.js
│   │   └── 📄 datatable.js
│   │
│   ├── 📁 vendor/                 # Third-party Libraries
│   │   ├── 📁 bootstrap/
│   │   ├── 📁 jquery/
│   │   ├── 📁 chart.js/
│   │   ├── 📁 socket.io/
│   │   ├── 📁 datatables/
│   │   ├── 📁 select2/
│   │   ├── 📁 moment/
│   │   ├── 📁 exceljs/
│   │   ├── 📁 jspdf/
│   │   ├── 📁 fontawesome/
│   │   └── 📁 sweetalert/
│   │
│   └── 📁 images/                 # Images
│       ├── 📁 logo/
│       │   ├── 📄 logo.png
│       │   ├── 📄 logo-white.png
│       │   └── 📄 favicon.ico
│       ├── 📁 icons/
│       │   ├── 📄 critical.svg
│       │   ├── 📄 high.svg
│       │   ├── 📄 medium.svg
│       │   └── 📄 low.svg
│       └── 📄 loading.gif
│
└── 📁 templates/                  # Template Parts (4 files)
    ├── 📄 sidebar.php
    ├── 📄 header.php
    ├── 📄 footer.php
    └── 📄 modal.php
```

---

### **3. REALTIME (Node.js WebSocket)**

```
realtime/
│
├── 📄 server.js
├── 📄 package.json
├── 📄 .env
├── 📄 ecosystem.config.js
│
├── 📁 src/
│   ├── 📄 index.js
│   ├── 📄 app.js
│   │
│   ├── 📁 config/
│   │   ├── 📄 database.js
│   │   ├── 📄 redis.js
│   │   └── 📄 socket.js
│   │
│   ├── 📁 middleware/
│   │   ├── 📄 auth.js
│   │   ├── 📄 rateLimit.js
│   │   └── 📄 logger.js
│   │
│   ├── 📁 handlers/
│   │   ├── 📄 connection.js
│   │   ├── 📄 auth.js
│   │   ├── 📄 alert.js
│   │   ├── 📄 scan.js
│   │   ├── 📄 assessment.js
│   │   ├── 📄 metric.js
│   │   └── 📄 notification.js
│   │
│   ├── 📁 rooms/
│   │   ├── 📄 userRoom.js
│   │   ├── 📄 serverRoom.js
│   │   └── 📄 adminRoom.js
│   │
│   └── 📁 utils/
│       ├── 📄 logger.js
│       └── 📄 helpers.js
│
└── 📁 tests/
    ├── 📄 socket.test.js
    └── 📄 handler.test.js
```

---

### **4. DATABASE (SQL)**

```
database/
│
├── 📄 schema.sql
├── 📄 seed_all.sql
├── 📄 seed_categories_17.sql
├── 📄 seed_criteria_280.sql
├── 📄 seed_roles.sql
├── 📄 seed_permissions.sql
├── 📄 seed_users.sql
│
├── 📁 migrations/                 # 11 migration files
│   ├── 📄 V1__Create_users_table.sql
│   ├── 📄 V2__Create_roles_table.sql
│   ├── 📄 V3__Create_categories_table.sql
│   ├── 📄 V4__Create_criteria_table.sql
│   ├── 📄 V5__Create_servers_table.sql
│   ├── 📄 V6__Create_assessment_results_table.sql
│   ├── 📄 V7__Create_reports_table.sql
│   ├── 📄 V8__Create_alerts_table.sql
│   ├── 📄 V9__Create_vulnerabilities_table.sql
│   ├── 📄 V10__Create_audit_logs_table.sql
│   └── 📄 V11__Add_indexes.sql
│
├── 📁 procedures/                 # 4 stored procedures
│   ├── 📄 sp_calculate_score.sql
│   ├── 📄 sp_get_dashboard_stats.sql
│   ├── 📄 sp_cleanup_old_logs.sql
│   └── 📄 sp_generate_report.sql
│
├── 📁 triggers/                   # 3 triggers
│   ├── 📄 trg_audit_user_changes.sql
│   ├── 📄 trg_update_server_score.sql
│   └── 📄 trg_create_alert_on_fail.sql
│
└── 📁 views/                      # 3 views
    ├── 📄 vw_server_summary.sql
    ├── 📄 vw_compliance_status.sql
    └── 📄 vw_monthly_trend.sql
```

---

### **5. DOCUMENTATION**

```
docs/
│
├── 📄 README.md
├── 📄 INSTALLATION.md
├── 📄 DEPLOYMENT.md
│
├── 📁 api/
│   ├── 📄 authentication.md
│   ├── 📄 users.md
│   ├── 📄 criteria.md
│   ├── 📄 assessments.md
│   ├── 📄 reports.md
│   └── 📄 openapi.yaml
│
├── 📁 guides/
│   ├── 📄 user-manual.md
│   ├── 📄 admin-manual.md
│   ├── 📄 security-officer-guide.md
│   └── 📄 viewer-guide.md
│
├── 📁 references/
│   ├── 📄 280-criteria-list.md
│   ├── 📄 17-categories.md
│   ├── 📄 scoring-formula.md
│   ├── 📄 rbac-matrix.md
│   └── 📄 compliance-mapping.md
│
└── 📁 architecture/
    ├── 📄 system-architecture.png
    ├── 📄 database-er-diagram.png
    └── 📄 sequence-diagrams.md
```

---

### **6. SCRIPTS**

```
scripts/
│
├── 📄 deploy.sh
├── 📄 backup.sh
├── 📄 restore.sh
├── 📄 import_criteria.php
├── 📄 export_criteria.php
├── 📄 run_assessment.php
├── 📄 clean_logs.php
├── 📄 create_admin.php
├── 📄 reset_password.php
├── 📄 generate_report.php
├── 📄 monitor.php
└── 📄 sync_servers.php
```

---

### **7. CI/CD & DEVOPS**

```
.github/workflows/
├── 📄 deploy.yml
├── 📄 test.yml
├── 📄 backup.yml
└── 📄 security-scan.yml

.docker/
├── 📄 Dockerfile.php
├── 📄 Dockerfile.nginx
├── 📄 Dockerfile.node
└── 📄 docker-entrypoint.sh

.k8s/
├── 📄 deployment.yaml
├── 📄 service.yaml
├── 📄 ingress.yaml
├── 📄 configmap.yaml
└── 📄 secret.yaml
```

---

## 📊 THỐNG KÊ TỔNG HỢP

| Loại | Số lượng | Mô tả |
|------|----------|-------|
| **Backend Files** | ~200 | PHP core, controllers, models, services |
| **Frontend Files** | ~60 | HTML, CSS, JS, assets |
| **Realtime Files** | ~15 | Node.js WebSocket server |
| **Database Files** | ~50 | Migrations, seeders, procedures |
| **Documentation** | ~20 | API docs, user guides |
| **Scripts** | ~12 | Utility bash/php scripts |
| **Config Files** | ~15 | Environment, Docker, K8s |
| **Tests** | ~15 | Unit, feature, integration |

**TỔNG CỘNG: ~387 FILES**

---

## 🎯 TÓM TẮT

```
┌─────────────────────────────────────────────────────────────────┐
│                  CẤU TRÚC HOÀN CHỈNH                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ✅ Backend API:     17 route files, 16 controllers           │
│   ✅ Core Framework:   15 core classes                          │
│   ✅ Database:         29 tables, 36 migrations                │
│   ✅ Frontend:         28 pages, 20 JS files, 7 CSS files      │
│   ✅ Realtime:         Node.js WebSocket server                 │
│   ✅ Security:         JWT, RBAC, Middleware, Encryption       │
│   ✅ Testing:          Unit, Feature, Integration tests         │
│   ✅ DevOps:           Docker, K8s, CI/CD                       │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

**🎉 ĐÂY LÀ CẤU TRÚC HOÀN CHỈNH CỦA DỰ ÁN SECURITY ASSESSMENT PLATFORM!**
