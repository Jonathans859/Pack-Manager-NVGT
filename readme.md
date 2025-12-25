# Pack Manager for NVGT
An utility for the [Nonvisual Gaming Toolkit](https://nvgt.dev) to create and extract pack files of your NVGT applications using the pack_file class.

## Features

### Pack Creation
- Create encrypted pack files from any directory
- Add files or entire folders to existing packs
- Recursive directory traversal
- Progress bar with file count display
- Optional audio feedback during operations

### Pack Extraction
- Extract all files from a pack with directory structure preservation
- Selective file extraction (choose which files to extract)
- Automatic subdirectory creation during extraction
- Choose custom extraction destination

### Pack Management
- View pack statistics (file count, total size, individual file sizes)
- Browse and extract individual files from the stats viewer
- Open packs directly without saved configuration (for quick extraction)
- Edit existing configurations
- Delete configurations with confirmation

### Configuration System
- Save pack configurations for repeated use
- Store pack path, content directory, and encryption key
- Random key generator for secure encryption
- Browse dialogs for file/folder selection

## Usage

1. Run Pack Manager
2. Create a new pack configuration or open an existing pack directly
3. Select an action:
   - **Create/repack pack**: Creates a new pack from the configured directory
   - **Add files to pack**: Add additional files to an existing pack
   - **Extract pack (all files)**: Extract all files to a chosen destination
   - **Extract pack (select files)**: Choose specific files to extract
   - **View pack stats**: Browse pack contents with file sizes
   - **Delete files from pack**: (Note: requires sqlite_pack format)

## Keyboard Shortcuts

- **Delete**: Remove selected configuration (with confirmation)
- **Enter**: Execute selected action (on Execute button)
- **Escape**: Exit or cancel current dialog

## Technical Notes

- Uses NVGT's `pack_file` class for pack operations
- Pack files support encryption with custom keys
- The standard `pack_file` format is read-only after creation (cannot delete individual files)
- For mutable packs, consider using `sqlite_pack` format (future enhancement)
