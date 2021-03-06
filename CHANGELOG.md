# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).

## [1.5.0.10] - 2018-06-03

### Added

- Library Creation Button (Thank you [Catalin Chelariu](http://www.softpedia.com/editors/browse/catalin-chelariu) for suggestion)
- Settings tab to tabcontrol

### Changed

- Steam restart function updated
- File movement order

### Fixed

- Reflection of disk size changes
- "If you click check for backup updates while a backup is being performed, the game you are backing up will reappear" - Thank you Mobeeuz, like always.
- "Remove from List" origin context menu item appearing for Steam / SLM libraries.
- SLM Libraries being duplicated on save.

### Removed

- Settings button from top right corner.

## [1.5.0.9] - 2018-05-29

### Added

- NLog (https://github.com/NLog/NLog)

### Changed

- Buffer size for file movement
- SaveWindowPlacement is set to True
- Parsed form parts into user controls for easier access & edit.

### Removed

- Custom file logger
- ConfigureAwait calls

## [1.5.0.8] - 2018-05-26

### Added

- Discord button
- Patreon button

### Changed

- Handling of DirectoryNotFoundException in Steam Library - UpdateAppList

### Fixed

- Proper pausing on Task Manager
- Same goes for the Origin releated tasks

## [1.5.0.7] - 2018-05-25

### Fixed

- Fix for memory overflow happens on task manager when task is paused.

## [1.5.0.6] - 2018-01-13

### Added

- Custom styling support

### Fixed

- FileNotFoundException happens on getting version info.
- InvalidOperationException happens on getting junk files.
- IOException happens on library cleaner.
- DirectoryNotFoundException and IOException on GetCommonFiles.
- ArgumentNullException caused by IOException on DeleteFilesAsync method.
- ArgumentOutOfRangeException happens on generating Steam library list.

## [1.5.0.5] - 2018-01-08

### Fixed

- FileNotFoundException happens on file removal which caused by cached file properties.
- InvalidOperationException happens on updating junk list.
- Workshop files for tasked items are being detected by junk cleaner.
- ArgumentException happens on getting disk details for mapped network locations.(Haven't tried mapped location yet, not sure if it works or not)
- ArgumentOutOfRangeException on generating SLM library list.
- Handling of UnauthorizedAccessException on CopyFilesAsync/Steam method.
- InvalidOperationException happens on Updating application list for Steam.

## [1.5.0.4] - 2018-01-06

### Added

- Handled UnauthorizedAccessException on Steam.CopyFiles method

### Fixed

- FileNotFoundException happens on file removal which caused by cached file properties.
- IOException happens on getting directory info in case the device is not ready.
- DriveNotFoundException happens with offline libraries.
- ArgumentException in AddNew library function(?)

## [1.5.0.3] - 2018-01-03

### Changed

- Task Manager UI
  - Changed showing of current file info and file movement info.

### Fixed

- Check for backup updates function
- Steam generated backups are not visible if there is a SLM generated backup in the same library.

## [1.5.0.2] - 2018-01-03

### Changed

- .Net Framework target version to 4.5 from 4.6
- ACF file detection - using the manual method now.

### Fixed

- Win32Exception caused by context menu actions.
- DirectoryNotFoundException caused by application file list generation.
- ArgumentException caused by getting libraries' drive info.
- A possible memory leak happens during file movement.
- File attributes which was broken since v1.5
- Check for Backup Updates function

### Removed

- TaskbarItemInfo which was used to current task's progress in taskbar.
- FileSystemWatcher which was used to detect .ACF file changes on libraries.
- [Resourcer.Fody](https://github.com/Fody/Resourcer) as it is not being used currently and not supported in .Net Framework 4.5