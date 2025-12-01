### Windows and .NET Framework Compatibility Matrix

The following tables show which .NET Framework versions are included with each Windows version, the maximum supported .NET Framework version you can install, and when support ends for each OS.

#### Windows Client Operating Systems

| Windows Version | OS Support Status | OS End of Support | .NET Framework Included | Maximum .NET Framework | Notes |
|----------------|-------------------|-------------------|------------------------|----------------------|-------|
| **Windows 11 24H2** | ✅ Supported | TBD | 4.8.1 | 4.8.1 | Latest Windows version |
| **Windows 11 23H2** | ✅ Supported | TBD | 4.8.1 | 4.8.1 | Current recommended version |
| Windows 11 22H2 | ❌ Out of support | 2024 | 4.8.1 | 4.8.1 | |
| Windows 11 21H2 | ❌ Out of support | 2023 | 4.8 | 4.8.1 | Can upgrade to 4.8.1 |
| **Windows 10 22H2** | ✅ Supported | **October 14, 2025** | 4.8 | 4.8.1 | **FINAL Windows 10 version** |
| Windows 10 21H2 | ❌ Out of support | June 11, 2024 | 4.8 | 4.8.1 | |
| Windows 10 21H1 | ❌ Out of support | December 13, 2022 | 4.8 | 4.8.1 | |
| Windows 10 20H2 | ❌ Out of support | May 9, 2023 | 4.8 | 4.8.1 | |
| Windows 10 2004 | ❌ Out of support | December 14, 2021 | 4.8 | 4.8 | |
| Windows 10 1909 | ❌ Out of support | May 10, 2022 | 4.8 | 4.8 | |
| Windows 10 1903 | ❌ Out of support | December 8, 2020 | 4.8 | 4.8 | |
| Windows 10 1809 | ❌ Out of support | May 11, 2021 | 4.7.2 | 4.8 | |
| Windows 10 1803 | ❌ Out of support | November 10, 2020 | 4.7.2 | 4.8 | |
| Windows 10 1709 | ❌ Out of support | October 13, 2020 | 4.7.1 | 4.8 | |
| Windows 10 1703 | ❌ Out of support | October 9, 2018 | 4.7 | 4.8 | |
| Windows 10 1607 | ❌ Out of support | October 13, 2020 | 4.6.2 | 4.8 | |
| Windows 10 1511 | ❌ Out of support | October 10, 2017 | 4.6.1 | 4.6.2 | Limited upgrade path |
| Windows 10 1507 (LTSC 2015) | ❌ Out of support | **October 14, 2025** | 4.6 | 4.6.2 | **Exception: .NET 4.6 supported until 10/2025** |
| Windows 8.1 | ❌ Out of support | January 10, 2023 | 4.5.1 | 4.8 | |
| Windows 8 | ❌ Out of support | January 12, 2016 | 4.5 | 4.6.1 | Very limited upgrade path |
| Windows 7 SP1 | ❌ Out of support | January 14, 2020 | 3.5 | 4.8 | ESU ended January 10, 2023 |
| Windows Vista | ❌ Out of support | April 11, 2017 | 3.0 | 4.6 | |
| Windows XP SP3 | ❌ Out of support | April 8, 2014 | None | 4.0.3 | |

#### Windows Server Operating Systems

| Windows Server Version | OS Support Status | OS End of Support | .NET Framework Included | Maximum .NET Framework | ESU Available Until |
|------------------------|-------------------|-------------------|------------------------|----------------------|-------------------|
| **Windows Server 2025** | ✅ Supported | TBD | 4.8.1 | 4.8.1 | N/A |
| **Windows Server 2022** | ✅ Supported | October 13, 2026 (Mainstream) | 4.8 | 4.8.1 | N/A |
| Windows Server 2019 | ❌ Out of support | January 9, 2024 | 4.7.2 | 4.8 | N/A |
| Windows Server 2016 | ❌ Out of support | January 12, 2027 (Extended ends) | 4.6.2 | 4.8 | N/A |
| Windows Server 2012 R2 | ❌ Out of support | October 10, 2023 | 4.5.1 | 4.8 | **October 13, 2026** |
| Windows Server 2012 | ❌ Out of support | October 10, 2023 | 4.5 | 4.8 | **October 13, 2026** |
| Windows Server 2008 R2 SP1 | ❌ Out of support | January 14, 2020 | 3.5 | 4.8 | Ended January 10, 2023 |
| Windows Server 2008 SP2 | ❌ Out of support | January 14, 2020 | 2.0 | 4.6 | Ended January 10, 2023 |

#### Key to Understanding the Table

**OS Support Status:**
- ✅ **Supported** = Operating system is currently receiving security updates from Microsoft
- ❌ **Out of support** = Operating system is no longer receiving updates (unless ESU purchased)

**Understanding ".NET Framework Included" and "Maximum .NET Framework":**
- **Included** = The .NET Framework version that ships with the OS by default
- **Maximum** = The highest .NET Framework version you can upgrade to on that OS

**CRITICAL: Backward Compatibility Note**
All .NET Framework 4.x versions are **in-place updates** and are **backward compatible**:
- If you have .NET Framework 4.8.1 installed, you can run applications targeting ANY 4.x version (4.0, 4.5, 4.5.1, 4.5.2, 4.6, 4.6.1, 4.6.2, 4.7, 4.7.1, 4.7.2, 4.8)
- You cannot have multiple 4.x versions installed simultaneously - the latest version replaces all previous ones
- Applications targeting older 4.x versions will automatically run on the newer runtime
- **Example:** Windows 11 24H2 comes with .NET Framework 4.8.1, which means it can run apps targeting .NET Framework 4.6.1, even though you cannot install 4.6.1 separately

**Important Notes:**
1. **.NET Framework support follows the OS support** - Once the OS is out of support, the .NET Framework version on that OS is also out of support (with rare exceptions like the SHA-1 retirement)
2. **In-place updates** - All .NET Framework 4.x versions are in-place updates. You can't have multiple 4.x versions installed simultaneously
3. **3.5 coexistence** - .NET Framework 3.5 can be installed alongside .NET Framework 4.x versions
4. **Maximum version limitations** - Older operating systems cannot install the latest .NET Framework versions due to OS-level dependencies

#### Critical Dates to Remember

| Date | Event | Impact |
|------|-------|--------|
| **April 26, 2022** | .NET Framework 4.5.2, 4.6, 4.6.1 ended support (all OS versions) | Due to SHA-1 certificate retirement |
| **October 14, 2025** | Windows 10 22H2 end of support | Last Windows 10 version reaches end of life |
| **October 14, 2025** | Windows 10 LTSC 2015 end of support | .NET Framework 4.6 exception expires on this date |
| **October 13, 2026** | Windows Server 2012/2012 R2 ESU ends | Final date for Extended Security Updates |
| **January 9, 2029** | .NET Framework 3.5 SP1 end of support | As standalone product on Win10 1809+ and Server 2019+ |

---
