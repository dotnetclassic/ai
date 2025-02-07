# Python Package Managers Overview

Here's a concise overview of various Python package managers, their implementation languages, and performance characteristics:

| Package Manager | Implementation Language | Performance Notes |
|---|---|---|
| **pip** | Python | Standard tool; performance varies with package complexity. |
| **conda** | Python | Manages packages and environments; can be slower due to comprehensive dependency management. |
| **mamba** | C++ | A faster alternative to conda, offering improved performance. |
| **poetry** | Python | Provides enhanced dependency resolution; may exhibit slower performance in complex projects. |
| **pipenv** | Python | Integrates pip and virtualenv; performance is comparable to pip. |
| **PDM** | Python | Focuses on PEP 582 compliance; performance is generally efficient. |
| **hatch** | Python | Emphasizes environment management; performance is efficient. |
| **rye** | Rust | Aims for speed and efficiency; still experimental. |
| **uv** | Rust | UV developed in rust and (1. rust is low level language assembly near machine language. 2. parallel downloading. 3. memory management only download one time 4. by default create virtual envirenment 5. fast dependency resolver 6. Can create lock file if open project after 10 year then no issues) Offers significant performance improvements, with benchmarks showing 10–100x faster speeds compared to pip in various scenarios. |


# Installing `uv` on Windows

## Prerequisites
- Windows OS (https://docs.astral.sh/uv/getting-started/installation/)
- PowerShell (Run as Administrator recommended)
- Python (if using `pipx` alternative method)

## Installation Steps

### 1. Open PowerShell as Administrator
Search for **PowerShell**, right-click it, and select **Run as Administrator**.

### 2. Run the Installation Command
Run the following command in PowerShell to download and install `uv`:
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

If this does nothing, manually download and install using the following steps:

### 3. Manually Download and Execute the Script
```powershell
Invoke-WebRequest -Uri "https://astral.sh/uv/install.ps1" -OutFile "install.ps1"
powershell -ExecutionPolicy Bypass -File "install.ps1"
```

### 4. Add `uv` to PATH (If Not Recognized)
After installation, if running `uv --version` results in **Command Not Found**, add it to the PATH.

#### **Temporary PATH Update (For Current Session Only)**
```powershell
$env:Path = "C:\Users\dotne\.local\bin;$env:Path"
```

#### **Permanent PATH Update**
Run the following command to persist the change:
```powershell
$env:Path = "C:\Users\dotne\.local\bin;$env:Path"
```

### 5. Restart PowerShell and Verify Installation
Close PowerShell, reopen it, and check the installation:
```powershell
uv --version
```
If it returns the installed version (e.g., `uv 0.5.29`), the setup is complete!

---



---

## Troubleshooting
- **Command Not Found:** Ensure `C:\Users\dotne\.local\bin` is in your **PATH**.
- **Internet Issues:** Check your firewall, VPN, or proxy settings if `Invoke-WebRequest` fails.
- **Permissions Issues:** Run PowerShell as **Administrator**.

---

### ✅ `uv` is now installed and ready to use! 🚀