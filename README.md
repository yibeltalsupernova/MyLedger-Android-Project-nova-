# MyLedger — ማህረቤ

## GitHub-ready Android finance app

MyLedger is a local-first Ethiopian personal finance manager built with Kotlin, Jetpack Compose and Room.

### Included in this build

- Dashboard with balance, income and expense totals
- Manual income, expense and transfer transactions
- Room local database
- Search
- Automatic vendor categorization
- CBE / Telebirr / M-Pesa SMS parsing framework
- Duplicate SMS protection
- Monthly budgets
- Category spending insights
- CSV export/share (Excel-compatible CSV)
- Dark-mode setting foundation
- DataStore settings foundation for PIN/onboarding
- Android SMS receiver
- GitHub Actions debug APK workflow
- GitHub Actions signed-release workflow
- Unit-test foundation
- Amharic-ready project naming/UI

### Important honesty about V1.2

The architecture contains foundations for PIN, onboarding and settings, but these are not yet a complete security lock screen. The provider SMS parsers are templates and must be validated against current, anonymized provider messages before production use. CSV is Excel-compatible; native `.xlsx` export is a later module.

### GitHub build

Push this repository to GitHub. GitHub Actions will run:

`Actions → MyLedger Android CI → Run workflow`

The result is uploaded as:

`MyLedger-debug-apk`

### Signed release

The repository includes `release-apk.yml`. Before running it, create these GitHub Actions secrets:

- `MYLEDGER_KEYSTORE_B64`
- `MYLEDGER_KEYSTORE_PASSWORD`
- `MYLEDGER_KEY_ALIAS`
- `MYLEDGER_KEY_PASSWORD`

The release workflow expects the Android signing keystore encoded with base64.

### Local build

Open the repository in Android Studio with JDK 17, sync Gradle, and run the app.

### Roadmap

Next production modules: full transaction editing, recurring transaction scheduler, category CRUD, real PIN/biometric lock, onboarding wizard, native XLSX export, backup/restore, richer charts, notification budget alerts, tested provider-specific SMS templates, and Play Store release configuration.
