# ClipTimeFix — GoPro video timestamp fixer for Lightroom Classic

**GoPro videos showing the wrong recording time in Adobe Lightroom Classic?** ClipTimeFix is a free, portable Windows beta that helps investigate and correct a specific timestamp mismatch — so videos can potentially appear in the right chronological order.

## The problem

A GoPro recording can contain different timestamps: the camera's **local recording time** in GoPro metadata and a different **QuickTime creation time** in the video file. For example, an actual 16:02 recording may have a QuickTime creation timestamp of 14:02. Depending on how software interprets that metadata, the video may appear at the wrong time alongside your photos.

**ClipTimeFix compares those timestamps, shows the proposed correction, and can create a separate video copy with corrected QuickTime capture-time metadata.** It does not re-encode the video or audio.

This is a standalone utility, **not an Adobe plugin**. Whether a correction changes the time shown in Lightroom Classic is the main question this beta is intended to test.

## What it does

- **Analyze** GoPro video files and display the detected camera, GoPro local recording time, QuickTime creation time, and difference.
- **Preview before fixing.** A timestamp difference alone does not prove that Lightroom is wrong; check the proposed time against the actual recording.
- **Create a separate corrected copy** with a `_ClipTimeFix` suffix. The original is left unchanged.
- **Work locally** on Windows without a user account or cloud upload. The implemented workflow has no telemetry.

## Try the Windows beta

**[Download ClipTimeFix v0.1.0-beta.2 (Windows x64)](https://github.com/iChicknHD/cliptimefix-downloads/releases/tag/v0.1.0-beta.2)**

1. Download and extract `ClipTimeFix-v0.1.0-beta.2-windows-x64.zip`.
2. Launch `ClipTimeFix.exe` from the extracted folder.
3. Select an expendable GoPro test video and run **Analyze**.
4. If the proposed time matches the actual recording time, use **Create Fixed Copies**.
5. Import the original and corrected copy separately into a fresh Lightroom Classic test catalog and compare the displayed capture times and sorting.

**Keep backups and use non-critical recordings.** This is experimental, unsigned beta software, so Windows may show an unknown-publisher warning. Check the archive hash against the release's `SHA256SUMS.txt`.

## What has actually been verified?

| Area | Status |
| --- | --- |
| Real GoPro HERO11 MP4: core analyze, fix and metadata read-back | **Tested** |
| Original file unchanged; video/audio streams not re-encoded in the HERO11 test | **Tested** |
| Portable Windows EXE startup and bundled ExifTool | **Tested** |
| Packaged GUI file-selection/analyze/fix interaction | **Not yet verified end-to-end** |
| Real Adobe Lightroom Classic import and timeline behavior | **Not yet verified** |
| HERO10, HERO12, HERO13 camera recordings | **Not yet verified with real footage** |
| MOV recordings | **Not yet verified with real footage** |

HERO10–13 and MP4/MOV are the intended implementation scope, **not a guarantee of compatibility**. See [Known Limitations](KNOWN_LIMITATIONS.md).

## Help test it

We're looking for Windows users with **GoPro HERO10–13 and Adobe Lightroom Classic**, especially those who have already noticed shifted video capture times.

Please follow the [Beta Test Guide](BETA_TEST_GUIDE.md) and report the GoPro model, Lightroom Classic version, original vs. corrected capture times, and whether chronological sorting improves. Please don't post personal videos, GPS details or unredacted metadata publicly.

## Support development

ClipTimeFix is **free to download and test**. If it helps, you can optionally [support development on Ko-fi](https://ko-fi.com/W6B32843F4). A donation is never required.

This repository hosts beta download information, not the private application source. The release ZIP includes third-party license and notice files. ClipTimeFix is an independent project and is not affiliated with GoPro or Adobe.
