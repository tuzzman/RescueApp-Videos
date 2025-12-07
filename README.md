# RescueApp Videos Repository

This document provides instructions for managing the video files in the public repository.

## Repository
**URL:** https://github.com/tuzzman/RescueApp-Videos

## Purpose
This public repository hosts all instructional video files for the Elevator Rescue App. The videos are organized by manufacturer and accessible via GitHub Releases.

## Release Structure

Create the following releases and upload corresponding video files:

### Release Tags:
- **OTIS** - Otis elevator videos (Gen 1 & Gen 2)
- **KONE** - Kone elevator videos
- **GAL** - GAL elevator videos
- **Schindler** - Schindler elevator videos (Gen 1-4)
- **thyssenkrupp** - ThyssenKrupp elevator videos (Gen 1-3)
- **mitsubishi** - Mitsubishi elevator videos
- **FUJITEC** - Fujitec elevator videos
- **westinghouse** - Westinghouse elevator videos
- **bi-part** - Bi-Parting Freight elevator videos

## Video File Naming Convention

Files should be named using this pattern:
```
{manufacturer}_{generation}_{doortype}_{picktype}.mp4
```

Examples:
- `otis_gen1_center_side.mp4`
- `kone_center_centerpick.mp4`
- `schindler_gen2_center_top.mp4`

## Uploading Videos

### Using GitHub Web Interface:
1. Go to https://github.com/tuzzman/RescueApp-Videos/releases/new
2. Create a new release with the appropriate tag (e.g., "OTIS")
3. Upload the .mp4 files as assets
4. Publish the release

### Using GitHub CLI (if installed):
```bash
gh release create OTIS --repo tuzzman/RescueApp-Videos --title "OTIS Videos"
gh release upload OTIS otis_gen1_center_side.mp4 --repo tuzzman/RescueApp-Videos
```

## Video List from Manifest

Below is the complete list of videos currently referenced in the manifest:

### OTIS (8 videos)
- otis_gen1_center_side.mp4
- otis_gen1_center_opt2.mp4
- otis_gen1_single_side.mp4
- otis_gen1_twospeed_side.mp4
- otis_gen2_center_doublelock_rake.mp4
- otis_gen2_center_rake.mp4
- otis_gen2_single_rake.mp4
- otis_gen2_twospeed_rake.mp4
- otis_gen2_twospeed_top_opt2.mp4

### KONE (8 videos)
- kone_center_centerpick.mp4
- kone_single_rt_hook.mp4
- kone_single_slide_lt_hook.mp4
- kone_single_slide_lt_side.mp4
- kone_single_slide_rt_side.mp4
- kone_two_speed_lt_hook.mp4
- kone_two_speed_lt_side.mp4
- kone_two_speed_rt_hook.mp4
- kone_two_speed_rt_side.mp4

### GAL (1 video)
- otis_center_linkage_side.mp4

### Schindler (7 videos)
- schindler_gen1_center_top.mp4
- schindler_gen1_two-speed_top.mp4
- schindler_gen1_single_top.mp4
- schindler_gen2_center_top.mp4
- schindler_gen2_center_side_opt_2.mp4
- schindler_gen3_two-speed_kone_side.mp4
- schindler_gen3_two-speed_rake.mp4
- schindler_gen4_side_pick.mp4
- schindler_gen4_side_opt_2.mp4

### thyssenkrupp (3 videos)
- thyssenkrupp_gen1_center_no_plate_top.mp4
- thyssenkrupp_gen2_center_w__plate_top.mp4
- thyssenkrupp-gen3_center_hook.mp4

### mitsubishi (6 videos)
- mitsubishi_center_no_linkage_top.mp4
- mitsubishi_center_w__linkage_top.mp4
- mitsubishi_center_w__linkage_side.mp4
- mitsubishi_two-speed_w__linkage_top.mp4
- mitsubishi_two-speed_w__linkage_side.mp4

### FUJITEC (1 video)
- fujitec_center_side.mp4

### westinghouse (3 videos)
- westinghouse_center_side.mp4
- westinghouse_center_top.mp4
- westinghouse_two-speed_side.mp4

### bi-part (1 video)
- bi-parting_freight.mp4

## After Uploading Videos

Once videos are uploaded to the public repository, update the manifest URLs:

1. Open the Manifest Admin webapp (http://localhost:5178)
2. Click "Reload Current Manifest"
3. Update URLs using find/replace:
   - Find: `https://github.com/tuzzman/elevatorRescueApp/releases/download/`
   - Replace: `https://github.com/tuzzman/RescueApp-Videos/releases/download/`
4. Click "Export to Server" to save changes

## Verifying Videos

After uploading, verify each video is accessible:
```
https://github.com/tuzzman/RescueApp-Videos/releases/download/OTIS/otis_gen1_center_side.mp4
```

Videos should download directly when accessed.

## Notes

- Repository is **PUBLIC** - anyone can access the videos
- Maximum file size per release asset: 2GB
- Recommended video format: MP4 (H.264)
- Keep original filenames as referenced in the manifest
