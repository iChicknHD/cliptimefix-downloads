# ClipTimeFix beta.2

ClipTimeFix is a portable Windows beta utility designed to correct GoPro video capture-time metadata for Adobe Lightroom Classic workflows.

This is a free, experimental beta for a small number of testers. Processing is local. No account, cloud processing, or telemetry is part of the implemented workflow. The tool compares capture-time metadata and, when the result is deterministic, creates a separate corrected copy. It changes metadata only; it does not re-encode video or audio. Keep original files and use copies of non-sensitive test footage. No result is guaranteed.

## Download

Download `ClipTimeFix-v0.1.0-beta.2-windows-x64.zip` from the [v0.1.0-beta.2 prerelease](https://github.com/iChicknHD/cliptimefix-downloads/releases/tag/v0.1.0-beta.2). Verify the SHA-256 using the release's `SHA256SUMS.txt`.

## Verification status

- HERO11 core analyze/fix/read-back with a real video: tested.
- HERO10, HERO12, HERO13: not verified with real camera footage.
- MOV runtime: not verified.
- Packaged GUI interaction: not verified.
- Lightroom Classic workflow: not verified.

See [Beta Test Guide](BETA_TEST_GUIDE.md) and [Known Limitations](KNOWN_LIMITATIONS.md). The ZIP contains third-party license and notice files. This beta notice is not a commercial-release clearance.
