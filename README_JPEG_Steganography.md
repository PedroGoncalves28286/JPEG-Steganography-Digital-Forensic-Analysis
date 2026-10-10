# JPEG Steganography & Digital Forensic Analysis

**Author:** Pedro Gonçalves  
**Category:** Digital Forensics · Steganography · Cybersecurity Laboratory  
**Environment:** Kali Linux

## Project Overview

This hands-on digital forensics project investigates a JPEG image (`doggo.jpg`) suspected of containing hidden information. The investigation documents evidence integrity checks, preliminary file inspection, decoding of a provided clue, and recovery of an embedded text file using Steghide.

The work is presented as an **authorized educational laboratory exercise**, not an investigation of a real-world target.

## Objectives

- Examine the supplied JPEG for indications of concealed data.
- Record file properties and verify evidence integrity with SHA-256.
- Compare preliminary inspection methods and their limitations.
- Decode a Base64 clue and apply ROT13 to recover the laboratory passphrase.
- Extract and inspect the embedded text using Steghide.
- Document the procedure, evidence, and findings in a technical report.

## Tools and Techniques

| Tool / technique | Purpose |
| --- | --- |
| Kali Linux | Forensic analysis environment |
| `wc` | Check file size |
| `sha256sum` | Record SHA-256 digest for integrity verification |
| `strings` | Inspect readable strings |
| `binwalk` | Check for recognizable embedded file signatures |
| `exiftool` | Inspect image metadata |
| `ent` | Examine statistical properties |
| `stegseek` | Test candidate passphrases in the lab |
| Base64 and ROT13 | Decode the provided clue |
| `steghide` | Extract password-protected hidden content |

## Investigation Workflow

1. **Evidence identification:** examine the provided JPEG and record its size and SHA-256 hash.
2. **Initial triage:** run basic content, metadata, signature, and statistical checks. These checks did not directly reveal the hidden message.
3. **Clue interpretation:** decode the provided Base64 text and then its ROT13-encoded passphrase.
4. **Data extraction:** use Steghide with the recovered lab passphrase to extract `text.txt`.
5. **Review and reporting:** inspect the recovered message and document the findings.

The recovered text discusses a *claimed* vulnerability involving NTLM credential exposure. The project analyzes a hidden message; **it does not demonstrate or verify that vulnerability**.

## Key Takeaways

- A normal-looking JPEG may contain concealed data not found by basic text or signature inspection.
- Hashes provide a reproducible integrity reference for the examined file.
- Encoded clues can be important to forensic triage; Base64 and ROT13 are encodings, not encryption.
- Forensic conclusions should distinguish observed evidence from claims contained within recovered files.

## Full Technical Report

📄 **[Read the complete PDF report](JPEG_Steganography_Forensic_Analysis_Pedro_Goncalves_COMPLETO.pdf)**

The report includes screenshots, command examples, the image used in the exercise, extraction evidence, and technical explanations.

## Responsible Use

All procedures were carried out in a controlled learning environment using an authorized sample. Do not apply forensic or security-testing techniques to systems or files without permission. Review screenshots and recovered content for sensitive information before public distribution.

## Author

**Pedro Gonçalves**  
[GitHub Portfolio](https://github.com/PedroGoncalves28286)

---
*Digital forensics portfolio project — JPEG steganography and hidden-data analysis.*
