# Pólya SDLC Coder 📐⚡
<!-- markdownlint-disable -->

> **Cara Matematikawan Memecahkan Masalah + Clean Architecture ala Uncle Bob, untuk AI Coding Agent**  
> Terinspirasi dari buku legendaris George Pólya *How to Solve It* (1945), buku *Clean Architecture* & *Clean Code* karya Robert C. Martin, serta *Skills for Real Engineers* karya Matt Pocock.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub](https://img.shields.io/badge/GitHub-polya--sdlc--coder-181717?logo=github)](https://github.com/GulajavaMinistudio/polya-sdlc-coder)
[![Documentation](https://img.shields.io/badge/Documentation-Live%20Web-0ea5e9?logo=googlechrome&logoColor=white)](https://gulajavaministudio.github.io/polya-sdlc-coder/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/GulajavaMinistudio/polya-sdlc-coder/pulls)
[![Platforms](https://img.shields.io/badge/Platforms-Copilot%20%7C%20Antigravity%20%7C%20Cursor%20%7C%20Claude%20%7C%20Codex%20%7C%20Pi-blueviolet)](#-platform-yang-didukung)

<p align="center">
  <img src="polya-sdlc-cats-compressed.jpg" alt="Pólya SDLC Coder Banner" width="760">
</p>

---

## 💡 Kenapa Pólya SDLC Coder?

Kebanyakan AI coding agent gagal bukan karena tidak bisa menulis kode, tetapi karena **terlalu cepat mulai menulis kode**.

Saat diberi perintah yang kurang jelas, agent cenderung menebak-nebak asumsi, melewatkan kasus-kasus pinggir (*edge case*), membuat tambalan yang berantakan, merusak batas-batas arsitektur yang sudah ada, dan menghasilkan kode yang sulit dirawat.

**Pólya SDLC Coder** membekali AI coding agent kamu dengan sistem kerja yang disiplin dan sudah teruji:

1. **Pahami Masalahnya Dulu (`/to-spec`)**: Uraikan *apa yang dicari* (*The Unknown*), *data apa yang tersedia* (*The Data*), dan *syarat apa yang harus dipenuhi* (*The Condition*). Tentukan kontrak data dan batas-batas Clean Architecture sebelum menulis satu baris kode aplikasi pun.
2. **Diskusi Kritis & Uji Ketahanan Desain (`/to-grill-me`)**: Uji asumsi, telusuri skenario gagal (*sad path*), dan paksa pengambilan keputusan teknis yang konkret (pilihan A atau B) lewat sesi tanya-jawab bergiliran, lengkap dengan rekomendasi senior.
3. **Audit Syarat & Kesiapan (`/to-clarify`)**: Bongkar hal-hal yang masih ambigu dengan pemeriksaan 5 sisi, lalu beri nilai kesiapan yang objektif (*Readiness Score* 0–100) sebelum mulai implementasi.
4. **Susun Rencana yang Modular (`/to-plan`)**: Pecah fitur menjadi potongan vertikal (*tracer bullet*) dari database sampai UI, lengkap dengan rencana cadangan (*Plan B*).
5. **🛑 Gerbang The Pause Rule**: Agent **WAJIB** berhenti dan menunggu persetujuan eksplisit dari kamu sebelum menulis kode fungsional.
6. **Jalankan Rencananya (`/to-code`)**: Terapkan Clean Code ala Uncle Bob, *Boy Scout Rule* (tinggalkan kode lebih bersih dari sebelumnya), dan aturan pengujian dua lapis, tanpa toleransi untuk "akal-akalan" atau menonaktifkan peringatan.
7. **Tinjau Kembali (`/to-review` & `/to-docs`)**: Audit 5 prinsip SOLID, uji batas-batas *invariant*, dan tulis dokumentasi yang terstruktur dengan kerangka Diátaxis.

---

## 🌐 Dokumentasi Web Interaktif

Lebih suka panduan visual yang interaktif? Kunjungi dokumentasi web resmi beserta katalog skill-nya:

<p align="center">
  <a href="https://gulajavaministudio.github.io/polya-sdlc-coder/">
    <img src="https://img.shields.io/badge/Live%20Web%20Docs-gulajavaministudio.github.io%2Fpolya--sdlc--coder-0ea5e9?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Web Documentation">
  </a>
</p>

🔗 **Alamat:** [https://gulajavaministudio.github.io/polya-sdlc-coder/](https://gulajavaministudio.github.io/polya-sdlc-coder/)

### 🌟 Apa Saja Isi Dokumentasi Web-nya?
- **🗂️ Katalog Interaktif 15 Skill**: Penjelasan mendalam semua 15 skill di 6 fase SDLC, lengkap dengan contoh prompt nyata, kontrak input/output, dan dokumentasi Diátaxis.
- **⚡ Konfigurator Instalasi Siap Salin**: Skrip sekali klik dan perintah `npx skills` untuk macOS, Linux, dan Windows yang bisa langsung disalin ke clipboard.
- **📐 Visualisasi Siklus 6 Fase**: Peta visual prinsip heuristik George Pólya (1945) yang dipadukan dengan batas-batas Clean Architecture ala Uncle Bob dan **🛑 Gerbang The Pause Rule**.
- **📱 Tampilan Bergaya Apple HIG & Ramah Ponsel**: Tipografi mode gelap, animasi halus, dan tampilan responsif di desktop, tablet, maupun smartphone.

---

## 📚 Latar Belakang: Kenapa George Pólya?

<p align="center">
  <img src="polya-books-cats.jpg" alt="George Pólya - How to Solve It" width="680">
</p>

### Kelemahan Mendasar AI Coding Saat Ini

Large Language Model (LLM), pada dasarnya, adalah **mesin penghasil kata yang "rakus"**: ia langsung menulis begitu diberi perintah. Ketika diminta *"Buatkan layanan autentikasi dengan Redis"*, AI agent akan langsung menuliskan baris demi baris kode.

Ia langsung masuk ke detail implementasi tanpa berhenti sejenak untuk bertanya:
- *Apa saja aturan baku (invariant) dan batasan dari masalah ini?*
- *Model data apa yang sudah ada di codebase?*
- *Kasus pinggir apa yang bisa menyebabkan kegagalan diam-diam di production?*

Hasilnya sudah sangat akrab bagi siapa pun yang memakai asisten AI: library yang ternyata tidak ada (halusinasi), kode yang ditulis terlalu dini secara berlapis-lapis, batas arsitektur yang rusak, dan tambalan rapuh yang langsung ambruk di kasus pinggir pertama. **Lebih dari 90% bug dari kode buatan AI bukan berasal dari salah ketik atau salah sintaks, melainkan dari implementasi yang terburu-buru di atas kebutuhan yang belum dipahami dengan benar.**

### Temuan George Pólya Tahun 1945 (*How to Solve It*)

Pada tahun 1945, matematikawan Hungaria **George Pólya** (1887–1985) menerbitkan *How to Solve It*, buku dasar tentang heuristik (cara berpikir untuk menemukan solusi) dan pemecahan masalah matematika yang terjual lebih dari satu juta eksemplar di seluruh dunia.

Pólya menunjukkan bahwa terobosan dalam matematika dan rekayasa tidak lahir dari buru-buru menghitung atau coba-coba tanpa arah. Terobosan butuh kerangka berpikir yang disiplin, terdiri dari **Empat Tahap Tetap**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                  TAHAP HEURISTIK GEORGE PÓLYA (1945)                   │
├────────────────────────────────────────────────────────────────────────┤
│ 1. MEMAHAMI MASALAH        ➔  Apa yang dicari? Data apa yang ada?      │
│                               Apa syaratnya? Bisakah dipenuhi?         │
│ 2. MENYUSUN RENCANA        ➔  Hubungkan data dengan yang dicari.       │
│                               Pecah jadi sub-masalah. Rumuskan ulang.  │
│ 3. MENJALANKAN RENCANA     ➔  Periksa setiap langkah.                  │
│                               Pastikan tiap langkah benar & terbukti.  │
│ 4. MENINJAU KEMBALI        ➔  Cek hasilnya. Coba dengan cara lain.     │
│                               Simpan pola yang bisa dipakai ulang.     │
└────────────────────────────────────────────────────────────────────────┘
```

> *"Bodoh rasanya menjawab pertanyaan yang tidak kita pahami. Menyedihkan rasanya bekerja untuk tujuan yang tidak kita inginkan."*  
> — **George Pólya**, *How to Solve It (1945)*

### Menjembatani Matematika, Clean Architecture ala Uncle Bob & AI Agent

**Pólya SDLC Coder** lahir dari satu kesadaran sederhana: **AI coding agent justru lebih membutuhkan disiplin berpikir Pólya dibanding developer manusia.**

Dengan memetakan kerangka matematika Pólya langsung ke **Clean Architecture karya Robert C. Martin ("Uncle Bob")** dan skill agent yang modular, asisten AI yang tadinya sulit ditebak berubah menjadi rekan kerja yang disiplin selevel *principal engineer*:

| Heuristik George Pólya (1945) | Praktik Rekayasa Perangkat Lunak | Skill Agent Pólya SDLC |
| :--- | :--- | :--- |
| **"Memahami Masalah"** | Batas domain, DTO & kontrak data | [`/to-spec`](skills/to-spec) & [`/to-explore`](skills/to-explore) |
| **"Diskusi Kritis & Menggugat Premis"** | Wawancara desain yang menantang & pilihan A/B | [`/to-grill-me`](skills/to-grill-me) |
| **"Menginterogasi Syarat"** | Invariant kasus pinggir & audit asumsi | [`/to-clarify`](skills/to-clarify) |
| **"Menyusun Rencana & Sub-Masalah"** | Tracer bullet vertikal & Plan B | [`/to-plan`](skills/to-plan) |
| **"Jeda Sebelum Menghitung"** | Gerbang persetujuan eksplisit dari manusia | **🛑 Gerbang The Pause Rule** |
| **"Menjalankan Rencana"** | Clean Code ala Uncle Bob & Micro-TDD | [`/to-code`](skills/to-code) & [`/to-quick-fix`](skills/to-quick-fix) |
| **"Meninjau Kembali & Memeriksa Hasil"** | Audit 5 prinsip SOLID & dokumentasi Diátaxis | [`/to-review`](skills/to-review) & [`/to-docs`](skills/to-docs) |
| **"Dua Pertanyaan Emas (Memori)"** | Pengetahuan arsitektur lintas sesi | [`/to-memory`](skills/to-memory) |

Sistem ini mencegah agent menulis satu baris kode aplikasi pun sampai masalahnya benar-benar diurai, asumsinya sudah diverifikasi, dan kamu sendiri sudah memberi persetujuan eksplisit di **The Pause Rule**.

---

## 🚀 Mulai Cepat & Instalasi

> [!TIP]
> **Coba Konfigurator Web Interaktif**: Kamu juga bisa memakai [Konfigurator Instalasi Web](https://gulajavaministudio.github.io/polya-sdlc-coder/#install) untuk berganti sistem operasi dengan mudah dan menyalin skrip terminal dengan sekali klik.

Kamu bisa memasang **Pólya SDLC Coder** ke proyekmu dengan salah satu dari tiga cara berikut:

### Cara 1: Instalasi via `npx skills` (Direkomendasikan)

Cara modern tanpa perlu package manager tambahan untuk memasang skill AI agent di berbagai tool (GitHub Copilot, Google Antigravity, Cursor, Claude Code, dan lainnya).

> [!NOTE]
> `npx skills` otomatis memeriksa folder [`skills/`](skills) di repository ini untuk menemukan dan menarik skill agent ke proyekmu.

#### Opsi A: Pasang Skill Bootstrapper (`to-init`) Saja

Pasang skill bootstrapper saja agar folder skill tetap ringan:

```bash
# Add to-init via GitHub shorthand
npx skills add GulajavaMinistudio/polya-sdlc-coder/skills/to-init
```

Lalu di jendela chat AI Assistant kamu, jalankan:

```text
/to-init setup this project
```

Bootstrapper akan otomatis menyiapkan aturan proyek (`AGENTS.md`), aturan orkestrator (`.agents/rules/PolyaOrchestrator.md`), standar, instruksi, dan semua sub-skill ke dalam repository kamu.

#### Opsi B: Pasang Semua Skill Sekaligus

Kalau kamu ingin langsung memasang seluruh 15 skill ke proyekmu:

```bash
# Add all skills from this repository
npx skills add GulajavaMinistudio/polya-sdlc-coder
```

Setelah terpasang, jalankan `/to-init` di jendela chat untuk membuat file `AGENTS.md` di root proyek beserta file-file aturan proyek lainnya.

---

### Cara 2: Skrip Interaktif Otomatis (Satu Baris Perintah)

Jalankan installer interaktif dari terminal di folder root proyek tujuan. Skrip ini akan mencadangkan file memori yang sudah ada dengan aman dan membiarkan kamu memilih platform tujuan (`.agents/`, `.claude/`, atau `.cursor/`):

#### 🪟 Windows (PowerShell)

```powershell
irm https://raw.githubusercontent.com/GulajavaMinistudio/polya-sdlc-coder/main/install.ps1 | iex
```

#### 🐧 Linux / macOS (Bash & Zsh)

```bash
curl -fsSL https://raw.githubusercontent.com/GulajavaMinistudio/polya-sdlc-coder/main/install.sh | bash
```

Skrip interaktif ini akan:
1. Meng-clone atau mengunduh rilis terbaru `polya-sdlc-coder`.
2. Meminta kamu memilih folder platform tujuan (`.agents/`, `.claude/`, atau `.cursor/`).
3. Mempertahankan dan menggabungkan `AGENTS.md` atau `memory.instructions.md` yang sudah ada dengan aman.

---

### Cara 3: Instalasi Manual

Kalau kamu ingin kendali penuh secara manual:

```bash
# 1. Clone the repository
git clone https://github.com/GulajavaMinistudio/polya-sdlc-coder.git

# 2. Copy the configuration to your project
# For standard platforms (Copilot, Antigravity, Codex, Pi, OpenCode):
cp -r polya-sdlc-coder/.agents /path/to/your/project/
cp polya-sdlc-coder/AGENTS.md /path/to/your/project/

# For Claude Code:
cp -r polya-sdlc-coder/.agents /path/to/your/project/.claude
cp polya-sdlc-coder/AGENTS.md /path/to/your/project/

# For Cursor:
cp -r polya-sdlc-coder/.agents /path/to/your/project/.cursor
cp polya-sdlc-coder/AGENTS.md /path/to/your/project/
```

---

## 🔄 Alur Utama: Dari Ide sampai Rilis

Pólya SDLC mengikuti alur kerja yang ketat dan disiplin, dirancang untuk menghilangkan ambiguitas dan mencegah kode yang berantakan karena bolak-balik revisi:

```text
====================================================================================================
               ALUR LENGKAP POLYA-SDLC: DISCOVERY ➔ SPEC ➔ PLAN ➔ CODE ➔ REVIEW ➔ DOCS
====================================================================================================

[ Fase 0: DISCOVERY & EKSPLORASI ] (Pólya Fase 0: Mengenal Masalah)
      │
      ▼
┌───────────────────────────────┐
│ /to-explore                   │ ──▶ [ docs/discovery/ ] ──▶ ( Kritik Struktur Repo, Trade-Off, Spike )
└───────────────────────────────┘
      │
      ├─────────────────────────────────────────────────┐
      │ (Jalur A: Kebutuhan Bisnis, opsional)           │ (Jalur B: Langsung ke Arsitektur Teknis)
      ▼                                                 │
┌───────────────────────────────┐                       │
│ /to-prd                       │ ──▶ [ docs/prd/ ]     │
└───────────────────────────────┘                       │
      │                                                 │
      └─────────────────────────┬───────────────────────┘
                                │
                                ▼
[ Fase 1: SPESIFIKASI ] (Pólya Fase 1: Memahami Masalah)
      │
      ▼
┌───────────────────────────────┐
│ /to-spec                      │ ──▶ [ docs/spec/ & docs/adr/ ] ──▶ ( Cek Kewajaran & Pemetaan Persamaan )
└───────────────────────────────┘
      │
      ├─────────────────────────────────────────────────┐
      │ (Sparring desain tanya-jawab)                   │ (Cek kewajaran syarat secara formal)
      ▼                                                 ▼
┌───────────────────────────────┐               ┌───────────────────────────────┐
│ /to-grill-me                  │               │ /to-clarify                   │ ──▶ [ docs/audit/ ]
└───────────────────────────────┘               └───────────────────────────────┘
      │ (Log Keputusan & ADR)                           │ (Skor Kesiapan >= 80)
      └─────────────────────────┬───────────────────────┘
                                │
                                ▼
[ Fase 2: PERENCANAAN ] (Pólya Fase 2: Menyusun Rencana)
      │
      ▼
┌───────────────────────────────┐
│ /to-plan                      │ ──▶ [ docs/plan/ ] ──▶ ( Land & Expand / Tracer Bullet )
└───────────────────────────────┘
      │
      ├─────────────────────────────────────────────────┐
      │ (Uji ketahanan rencana & Plan B)                │ (Gerbang kesiapan rencana)
      ▼                                                 ▼
┌───────────────────────────────┐               ┌───────────────────────────────┐
│ /to-grill-me                  │               │ /to-clarify                   │
└───────────────────────────────┘               └───────────────────────────────┘
      │                                                 │
      └─────────────────────────┬───────────────────────┘
                                │
                                ▼
🛑 GERBANG WAJIB: THE PAUSE RULE
(Berhenti! Tunggu persetujuan eksplisit dari user sebelum menulis kode fungsional)
      │
      ▼ [Disetujui]
[ Fase 3: IMPLEMENTASI ] (Pólya Fase 3: Menjalankan Rencana)
      │
      ▼
┌───────────────────────────────┐
│ /to-code                      │ ──▶ ( Clean Code, Respice Finem, Boy Scout Rule, Edit Presisi )
└───────────────────────────────┘
      │
      ▼
[ Fase 4: REVIEW & AUDIT ] (Pólya Fase 4: Meninjau Kembali)
      │
      ├───────────────────────────────┐
      │ (Jika lolos & disetujui)      │ (Jika ada cacat / invariant dilanggar)
      ▼                               ▼
┌───────────────────────────────┐   ┌───────────────────────────────┐
│ /to-docs                      │   │ /to-fix                       │ ──▶ ( Kembali ke Prinsip Dasar, Lacak Seam yang Rusak )
└───────────────────────────────┘   └───────────────────────────────┘
      │ [docs/{tutorials,how-to,reference,explanation}/]
      ▼
[ Fase 6: DOKUMENTASI TEKNIS ] (Transfer Pengetahuan & Kerangka Diátaxis)

════════════════════════════════════════════════════════════════════════════
[ PUSAT TRIASE OTOMATIS ]       ──▶ /to-ask-help   (Analisis maksud & diagnosis otomatis)
[ SPARRING SOKRATIK ]           ──▶ /to-grill-me   (Wawancara desain bergiliran & uji ketahanan)
[ JALUR CEPAT ]                 ──▶ /to-quick-fix  (Perbaikan rutin, ukuran XS/S, sekali jalan)
[ PETA ARSITEKTUR ]             ──▶ /to-map        (Telusuri struktur, Seam, docs/ARCHITECTURE.md)
[ MEMORI PERSISTEN ]            ──▶ /to-memory     (Simpan checkpoint ke memory.instructions.md)
[ INISIALISASI PROYEK ]         ──▶ /to-init       (Siapkan AGENTS.md & paket .agents/)
════════════════════════════════════════════════════════════════════════════
```

---

## 🧰 Katalog Skill

> [!TIP]
> Jelajahi, cari, dan periksa katalog lengkap 15 skill beserta contoh prompt yang bisa disalin di [Katalog Skill Web Interaktif](https://gulajavaministudio.github.io/polya-sdlc-coder/#skills).

Setiap skill di Pólya SDLC bersifat modular, bisa berdiri sendiri, dan fokus pada satu tanggung jawab:

| Slash Command | Folder Skill | Fase / Peran | Deskripsi & Fokus Heuristik Pólya | Hasil Utama |
| :--- | :--- | :--- | :--- | :--- |
| **`/to-ask-help`** | [`to-ask-help`](skills/to-ask-help) | **Pusat & Triase** | Menelusuri codebase secara otomatis, mengenali maksud permintaan, dan mendiagnosis lewat 3 pertanyaan Sokratik. | Triage Card & Arahan Skill |
| **`/to-explore`** | [`to-explore`](skills/to-explore) | **Fase 0: Discovery** | Membingkai masalah, mengkritisi struktur repository, menimbang trade-off arsitektur (*Inventor's Paradox*), dan melakukan *spike* (percobaan kecil). | `docs/discovery/{slug}-discovery.md` |
| **`/to-prd`** | [`to-prd`](skills/to-prd) | **Fase 0.5: PRD** | Membingkai masalah bisnis, menyusun user story yang SMART, dan batasan penerimaan (*cabang opsional*). | `docs/prd/{slug}-prd.md` |
| **`/to-spec`** | [`to-spec`](skills/to-spec) | **Fase 1: Spec** | Mengurai *Yang Dicari, Data, Syarat*, menyusun "persamaan" berupa DTO, dan memetakan batas Clean Architecture. | `docs/spec/{slug}-spec.md` + `docs/adr/` |
| **`/to-grill-me`** | [`to-grill-me`](skills/to-grill-me) | **Sparring: Wawancara Sokratik** | Wawancara desain bergiliran, berperan sebagai *Devil's Advocate*, satu pertanyaan A/B per giliran, dan uji ketahanan desain. | Log Keputusan & Usulan ADR |
| **`/to-clarify`** | [`to-clarify`](skills/to-clarify) | **Checkpoint: Klarifikasi** | Membongkar ambiguitas, tag `[ASSUMPTION]`, cek kewajaran syarat, dan Skor Kesiapan (0–100). | `docs/audit/{slug}-clarification.md` |
| **`/to-plan`** | [`to-plan`](skills/to-plan) | **Fase 2: Plan** | *Berpikir mundur dari tujuan*, *sub-masalah bantu*, Land & Expand (tracer bullet), Plan B, dan **The Pause Rule**. | `docs/plan/{slug}-plan.md` |
| **`/to-code`** | [`to-code`](skills/to-code) | **Fase 3: Implementasi** | Menulis kode dengan Clean Code, fungsi kecil bertanggung jawab tunggal, dan patuh pada *Boy Scout Rule*. | Kode Production & Test |
| **`/to-review`** | [`to-review`](skills/to-review) | **Fase 4: Review** | Review kode/PR berbasis tingkat risiko (`Quick`/`Standard`/`Deep`), 5 prinsip SOLID, 14 vektor keamanan defensif, penyaringan temuan `[Important]`/`[Nit]`/`[Pre-existing]`, penyisiran `Bug Class`, konvergensi 3 putaran, dan gerbang rilis `GO/NO-GO`. Mendukung `/to-review security`. | `docs/reviews/{slug}-review.md` |
| **`/to-fix`** | [`to-fix`](skills/to-fix) | **Fase 5: Perbaikan Bug** | Berhenti menambal secara asal, kembali ke prinsip dasar, melacak seam yang rusak, dan membuat test yang mereproduksi bug. | `docs/bug-reports/{slug}-bugfix.md` |
| **`/to-docs`** | [`to-docs`](skills/to-docs) | **Fase 6: Dokumentasi** | Menulis dokumentasi terstruktur berdasarkan 4 kuadran Diátaxis (Tutorial, How-To, Referensi, Penjelasan). | `docs/{quadrant}/{slug}.md` |
| **`/to-quick-fix`** | [`to-quick-fix`](skills/to-quick-fix) | **Jalur Cepat** | Masalah rutin, perbaikan presisi sekali jalan, dan refactor kecil (*Pedantry vs Mastery*, *The Excavator Rule*). | Diff File Presisi ($\le 2$ file) |
| **`/to-map`** | [`to-map`](skills/to-map) | **Utilitas: Peta Struktur** | Menelusuri struktur folder, memetakan batas Clean Architecture, dan membuat `docs/ARCHITECTURE.md`. | `docs/ARCHITECTURE.md` |
| **`/to-memory`** | [`to-memory`](skills/to-memory) | **Utilitas: Memori** | Membaca, menulis, dan meringkas konteks sesi ke/dari `memory.instructions.md`. | `memory.instructions.md` |
| **`/to-init`** | [`to-init`](skills/to-init) | **Utilitas: Scaffolding** | Menyiapkan arsitektur dan aturan proyek secara otomatis. | `AGENTS.md` + `.agents/` |

---

## 📖 Cara Pakai: Contoh Alur Kerja

### 1. Arahkan Permintaanmu (Navigator Sokratik)

Bingung harus mulai dari fase mana? Cukup tanyakan:

```text
/to-ask-help Add real-time order tracking using WebSockets and Redis
```

Navigator akan menelusuri codebase kamu secara otomatis, menimbang *Yang Dicari* vs *Data* vs *Syarat*, lalu menampilkan **Pólya Triage Card**:

```text
+-----------------------------------------------------------------------+
|                         POLYA TRIAGE CARD                             |
+-----------------------------------------------------------------------+
| Yang Dicari   : Stream pelacakan pesanan real-time via WebSocket      |
| Data          : Entity Order, adapter Redis Pub/Sub, hook React UI    |
| Syarat        : Latensi < 100ms, auto-reconnect, autentikasi JWT      |
| Seam Ditemukan: Domain (Order), Adapter (RedisStream), UI (Hook)      |
| Rekomendasi   : /to-explore atau /to-spec @docs/spec/...              |
+-----------------------------------------------------------------------+
```

---

### 2. Eksplorasi Masalah & Percobaan Arsitektur (`/to-explore`)

Sebelum mengunci skema atau menulis kode, jelajahi dulu kelayakan, trade-off teknologi, dan struktur repository:

```text
/to-explore Investigate architecture options for real-time order tracking (WebSockets vs SSE vs Polling)
```

Agent akan menelusuri codebase, membandingkan pilihan-pilihan dengan dependensi yang sudah ada, lalu menghasilkan `docs/discovery/order-tracking-discovery.md`:
- **Kritik Struktur Repository**: Menilai manajemen state, lapisan HTTP, dan message bus yang sudah ada.
- **Analisis Trade-Off (*The Inventor's Paradox*)**: Menimbang WebSocket vs SSE vs Long-Polling dari sisi kompleksitas, latensi, dan biaya infrastruktur.
- **Spike Arsitektur**: Merancang verifikasi prototipe minimal tanpa mengotori kode production.

---

### 3. (Opsional) Tentukan Kebutuhan Bisnis & User Story (`/to-prd`)

Dipakai ketika sebuah fitur butuh keselarasan produk yang mendalam, user story, dan kriteria penerimaan bisnis:

```text
/to-prd @docs/discovery/order-tracking-discovery.md
```

Agent akan menyusun sudut pandang bisnis dan menghasilkan `docs/prd/order-tracking-prd.md`:
- **Persona & User Story**: Contohnya, *Sebagai pelanggan, saya ingin melacak kurir pengantar secara real-time...*
- **Kriteria Penerimaan yang SMART**: Menetapkan ukuran yang bisa diamati (misalnya, pembaruan lokasi tiba dalam $\le 2$ detik).
- **Hal yang Tidak Dikerjakan (Non-Goals)**: Menetapkan batas yang tegas (misalnya, fitur chat dengan kurir tidak termasuk di versi 1).

---

### 4. Tulis Spesifikasi & Petakan Batas Arsitektur (`/to-spec`)

Ubah kebutuhan produk atau hasil eksplorasi menjadi cetak biru teknis yang formal:

```text
/to-spec @docs/prd/order-tracking-prd.md
```
*(Atau langsung dari hasil discovery: `/to-spec @docs/discovery/order-tracking-discovery.md`)*

Agent akan membuat `docs/spec/order-tracking-spec.md` yang mendefinisikan:
- **Batas Clean Architecture**: Entities ➔ Use Cases ➔ Interface Adapters ➔ Infrastructure.
- **DTO & Discriminated Union**: Skema payload yang lengkap.
- **Invariant & Kriteria Penerimaan**: Diberi ID berurutan (`REQ-001`, `AC-001`).
- **Penandaan Asumsi**: Ditandai secara eksplisit dengan `> [!WARNING] [ASSUMPTION-001]`.

---

### 5. Sparring Sokratik & Wawancara Desain (`/to-grill-me`)

Sebelum mengunci rencana, atau saat menghadapi pilihan arsitektur yang sulit, uji desainmu lewat wawancara desain bergiliran yang sengaja menantang:

```text
/to-grill-me spec @docs/spec/order-tracking-spec.md
```

Agent akan berperan sebagai **Pólya Socratic Sparring Partner (si Devil's Advocate)**:
- **Aturan Satu Pertanyaan:** Tidak pernah membanjirimu dengan banyak pertanyaan; hanya **SATU** pertanyaan tajam per giliran.
- **Agent yang Bekerja Keras:** Mengusulkan 2–3 pilihan konkret yang berdasar secara teknis (Pilihan A vs Pilihan B), digali dari repository kamu.
- **Rekomendasi Senior yang Tegas:** Selalu merekomendasikan pilihan arsitektur paling bersih beserta alasan praktisnya.
- **Bisa Dipakai di Fase Mana Saja:** Bisa dipanggil untuk ide mentah (`/to-grill-me "idea"`), PRD (`/to-grill-me prd`), Spec (`/to-grill-me spec`), atau rencana eksekusi (`/to-grill-me plan`).
- **Log Keputusan:** Merangkum keputusan yang sudah disepakati menjadi perubahan dokumen yang siap diterapkan, atau membuat ADR di `docs/adr/`.

---

### 6. Audit Syarat & Gerbang Kesiapan (`/to-clarify`)

Setelah spesifikasi selesai disusun dan perdebatan desain terselesaikan, lakukan audit kualitas secara formal:

```text
/to-clarify @docs/spec/order-tracking-spec.md
```

Agent akan berperan sebagai **Pólya Clarification Analyst** yang teliti tanpa kompromi:
- **Cek Kewajaran 5 Sisi:** Memeriksa Tujuan/Premis, Alur Pengguna & 5 Kondisi UI, Skenario Gagal, Seam, dan Batas Cakupan.
- **Keraguan yang Sehat (Epistemic Doubt):** Mengevaluasi tag `> [!WARNING] [ASSUMPTION-XXX]` dan memburu kasus pinggir yang belum ditangani.
- **Skor Kesiapan (0–100):** Menilai Kelengkapan (40%), Kejelasan (30%), dan Keselarasan (30%). Jika skornya $< 80$, fitur belum boleh lanjut ke tahap perencanaan.

---

### 7. Buat Tracer Bullet Vertikal (`/to-plan`)

```text
/to-plan @docs/spec/order-tracking-spec.md
```

Agent akan membuat `docs/plan/order-tracking-plan.md` yang memecah implementasi menjadi potongan vertikal (*tracer bullet*) yang bisa didemokan:
- **Task 1 (Tracer Bullet 1)**: Domain Event + port Redis Pub/Sub + test dengan mock.
- **Task 2 (Tracer Bullet 2)**: Gateway WebSocket + adapter autentikasi JWT.
- **Task 3 (Tracer Bullet 3)**: Hook frontend + indikator status koneksi di UI.
- **Rencana Cadangan (Plan B)**: Beralih ke polling jika WebSocket gagal.

---

### 8. 🛑 Gerbang The Pause Rule

> [!CAUTION]
> **The Pause Rule**: Agent otomatis berhenti setelah membuat rencana. Tidak ada kode yang boleh ditulis sampai developer meninjau dan mengonfirmasi:
> 
> *"Rencana sudah ditinjau dan disetujui. Lanjutkan ke implementasi."*

---

### 9. Implementasi dengan Disiplin Clean Code (`/to-code`)

```text
/to-code @docs/plan/order-tracking-plan.md @docs/spec/order-tracking-spec.md
```

Agent membaca Rencana Implementasi dan Spesifikasi Teknis yang sudah disetujui, lalu mengerjakan Task 1 (Tracer Bullet 1) dengan disiplin rekayasa yang ketat:
- **Clean Code ala Uncle Bob**: Fungsi di bawah 25 baris, satu tingkat abstraksi per fungsi, dan nama yang jelas maksudnya.
- **Boy Scout Rule**: File yang disentuh ditinggalkan dalam keadaan lebih bersih dari sebelumnya.
- **Aturan Pengujian Dua Lapis**: Menjalankan pengecekan tipe yang cepat (`check:fast`) dan test per potongan vertikal (`check:task`) sebelum menyelesaikan setiap task.
- **Penjaga Anti-Curang**: Dilarang memakai `@ts-ignore`, melewati test, atau meninggalkan komentar `TODO` kosong.
- **Komentar Berbahasa Indonesia**: Setiap fungsi baru diberi docblock, dan setiap blok kode penting diberi komentar singkat dalam bahasa Indonesia supaya mudah dipahami.

---

### 10. Review, Audit & Transfer Pengetahuan (`/to-review` & `/to-docs`)

```text
# Adaptive Quality & Release Audit (Quick / Standard / Deep based on Risk Tier)
/to-review @docs/plan/order-tracking-plan.md @docs/spec/order-tracking-spec.md

# Focused Adversarial Security Audit
/to-review security @docs/spec/order-tracking-spec.md
```
Skill ini mengelompokkan perubahan berdasarkan seberapa luas dampaknya, yaitu **Tingkat Risiko (`Low` / `Medium` / `High-Critical`)** dan Kedalaman Review (**`Quick` / `Standard` / `Deep`**), serta menandai bagian sensitif dengan `[MANDATORY HUMAN AUDIT REQUIRED]`. Kode diaudit terhadap 5 prinsip SOLID, batas-batas invariant, dan 14 vektor keamanan defensif (OWASP, isolasi tenant, batas LLM/MCP). Temuan yang hanya "berisik" disaring dengan menandai setiap temuan sebagai **`[Important]`**, **`[Nit]`**, atau **`[Pre-existing]`** beserta **`Bug Class`**-nya. Review dibatasi maksimal 3 putaran, lalu diakhiri dengan keputusan tegas `GO | NO-GO` memakai 3 status keamanan (`CONFIRMED`, `NEEDS_VALIDATION`, `REJECTED`) di dalam `docs/reviews/order-tracking-review.md`.

```text
/to-docs @docs/spec/order-tracking-spec.md @docs/plan/order-tracking-plan.md
```
Menghasilkan dokumentasi yang jelas berdasarkan kontrak yang sudah terverifikasi di Spesifikasi dan Rencana, disusun mengikuti **Kerangka Diátaxis** (Tutorial, Panduan How-To, Referensi, atau Penjelasan Arsitektur) di dalam folder `docs/`.

---

## ⚡ Jalur Cepat (`/to-quick-fix`)

Mau memperbaiki salah ketik, mengubah konfigurasi, atau melakukan perubahan kecil di 1–2 file? Kamu tidak perlu melewati 6 fase SDLC yang berat untuk perubahan kecil:

```text
/to-quick-fix Fix typo in redis timeout config and update connection retry count
```

Mengikuti prinsip Pólya *Pedantry vs. Mastery* (1945), yaitu menerapkan aturan dengan bijak, bukan kaku, `/to-quick-fix` melewati spesifikasi formal tetapi tetap menjaga kualitas kode, pengecekan tipe, dan commit yang atomik.

---

## 🔌 Platform yang Didukung

Pólya SDLC Coder mendukung semua platform AI coding agent modern utama melalui arsitektur **satu sumber kebenaran** (*Single Source of Truth*):

| Platform | Folder Konfigurasi | Deteksi & Setup |
| :--- | :--- | :--- |
| **GitHub Copilot** | `.agents/` | Didukung langsung di VS Code, JetBrains, dan Copilot CLI |
| **Google Antigravity** | `.agents/` | Skill dan persona berjalan penuh lewat Antigravity runner |
| **Cursor** | `.cursor/` atau `.agents/` | Pemanggilan skill dan integrasi rules yang mulus |
| **Claude Code** | `.claude/` | Integrasi plugin/skill secara langsung |
| **OpenCode / CommandCode** | `.agents/` | Sub-skill ditemukan secara otomatis |
| **ChatGPT Codex** | `.agents/` | Dijalankan lewat file instruksi proyek |
| **Pi Dev & Oh My Pi (`omp`)** | `.agents/` | Kompatibel penuh dengan agent skill |

---

## 🧠 Memori Sesi yang Persisten

Pólya SDLC menyimpan konteks yang awet di antara sesi chat melalui [`memory.instructions.md`](.agents/instructions/memory.instructions.md):

- Jalankan `/to-memory` untuk melihat, menyimpan checkpoint, atau meringkas pelajaran dari sesi saat ini.
- Mencatat tracer bullet yang sedang dikerjakan, keputusan arsitektur yang sudah terverifikasi (ADR), dan jebakan yang sudah diketahui.
- Mencegah konteks hilang saat restart atau berganti tool.

---

## 🤝 Berkontribusi

Kontribusi sangat disambut! Untuk berkontribusi:

1. Fork repository ini.
2. Buat branch fitur: `git checkout -b feat/my-new-skill`.
3. Ikuti heuristik George Pólya dan konvensi Clean Architecture ala Uncle Bob.
4. Uji dan verifikasi semua definisi skill dengan lint check.
5. Buka Pull Request dengan deskripsi yang jelas dan terstruktur.

---

## 📜 Lisensi

Didistribusikan di bawah **Lisensi MIT**. Lihat [`LICENSE`](LICENSE) untuk detailnya.

---

<p align="center">
  <i>"Bodoh rasanya menjawab pertanyaan yang tidak kita pahami. Menyedihkan rasanya bekerja untuk tujuan yang tidak kita inginkan."</i><br>
  — <b>George Pólya</b>, <i>How to Solve It (1945)</i>
</p>
