# IMEI Studio

A fast, reliable, Mac-first desktop application for repair technicians that converts an IMEI into clean device information (brand, model number, formatted display name, and images).

Built specifically for repair technicians to eliminate the pain of messy online lookup sites, inconsistent naming, and having to disassemble devices just to identify the model.

## Why This Tool Exists

- Most modern phones no longer print the model number on the chassis.
- Existing free lookup websites have become unusable (heavy ads, broken results, freezing).
- Technicians need **consistent, trustworthy** model names to order correct parts and give accurate quotes.
- App targets ≥95% accuracy with normalized, human-readable output for every major manufacturer.


## Core Features

- 🦀 **Fast.Really Fast:** Built on Rust using zero-cost abstractions for near-instant native execution. Functions 100% offline with zero external network needed for device lookups or API overhead.
- 🔒 **Secure Local-First Architecture:** All data processing is localized and does not leave your machine. Your IMEI history remains private and secure and is not stored remotely. Ever.
- 🚫 **Zero AI Reliance:** Built entirely without unreliable LLM wrappers or generative guesswork. This is a deterministic data engine engineered to parse raw telemetry using strict, rule-based logic, delivering a targeted ≥95% accuracy rate based on real live TAC data, not confident hallucinations from a chatbot that waste your time.
- 🎯 **Instant IMEI → Device Lookup:** Quick matching using a local TAC database utilizing the first 8 digits of any IMEI number.
- 🔄 **Robust Normalization Engine:** A single source of truth for manufacturer-specific model formats (Samsung `SM-XXXX`, Motorola `XT-XXXX`, etc.).
- 🏷️ **Clean Display Names:** Parses raw, messy manufacturer metadata into clean, consistent text (e.g., “Motorola Moto G (XT1033, 2013)”).
- ⚠️ **Smart Code Name Handling:** Detects internal carrier code names and warns you gracefully if you are searching for a recently released device.
- 📋 **Persistent Search History:** Easily track your past lookups with support for custom labels, individual deletion, and full history wipes.
- 🖼️ **Cached Device Media:** Pulls device imagery from GSMArena with smart local caching to prevent interface bloat or repetitive network fetches.
- ⚡ **Automated Data Sync:** Automatic TAC database updates that seamlessly re-apply your custom normalization rules on every new import.
- ✈️ **Fully Offline Architecture:** Functions completely disconnected from the web after your initial setup and database installation.
- 🍏 **Native Apple Silicon UI:** Specifically optimized for macOS, utilizing standard Apple native windows and sandbox-safe system storage paths.

## Roadmap & Milestones

Current status: **Phase 5: Beta Preview Build Completed & Shipped for Public Use** (in progress)

✅ **Phase 0: Setup & Foundations**  
**Milestone 0:** App builds, runs on macOS, and displays the empty UI shell with sidebar.  

✅ **Phase 1: Data Layer, Normalization Rules & Cleaning Engine**  
**Milestone 1:** Normalization rules file is complete and the engine produces clean, consistent output for all major manufacturers. Recent/code-name devices are flagged with warnings. Reliability ≥95% on test set. Database lives in correct macOS AppData location.  

✅ **Phase 2: Search, History & Front End Development - UI/UX Layer**  
**Milestone 2:** Complete end-to-end lookup and history flow. All manufacturer formatting rules are applied consistently. Output is reliable and shop-ready.  

✅ **Phase 3: GSMArena Images, Auto-Updates & Polish**  
**Milestone 3:** Images load reliably via GSMArena + cache. Database updates automatically keep normalized names clean. App consistently hits 95–98% accuracy with professional formatting.  

✅ **Phase 4: Hardening, Testing & Release**  
**Milestone 4:** Fully tested, signed, and reliable internal tool ready for daily use by users. Reliability ≥95–98% on real repair traffic.  

**Phase 5: Post-MVP (Features Planned For Future Development)**  
- Batch IMEI lookup  
- Report a misidentified model or missing device   
- Additional image sources and better code-name resolution  
- In app auto-updater for the app itself  
- Export full bench report with history
