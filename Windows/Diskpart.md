---
tags:
  - Windows
---
Diskpart is a command-line utility used to manage and configure hard drives.
## Set up a new disk
```cmd
C:\Users\...> diskpart
```
This command is used to get into the diskpart command-line utility
>[!Info] FYI
>You need to be part of the local Administrator group to use this command.

```cmd
DISKPART> list disk

 Datenträger ###  Status         Größe    Frei     Dyn  GPT
  ---------------  -------------  -------  -------  ---  ---
  Datenträger 0    Online          465 GB  1024 KB        *
```
The above command is used to list all disks connected to the PC. They will show up here if they are working, even if the disk isn't initialized yet or not found by the File Explorer.

```cmd
DISKPART> select disk 0
```
Will switch the focus of the selected disk. If successful it will say that the selected disk is now the disk with that number.

```cmd
DISKPART> clean
```
Cleaning a selected disk will remove all existing partitions as well as all volume formatting.

```cmd
DISKPART> convert gpt
```
This will convert the selected disk to the specified partition-style, in the example command it would be GPT. Other options like MBR exist as well.
>[!Info] FYI
> The disk needs to be empty to run this command. For GPT you need at least 128 MB of free space.

```cmd
DISKPART> create partition primary
```
Creates a new Section on that disk that can be formatted. Partitions will be treated by your PC like independent disks.

```cmd
DISKPART> format fs=ntfs quick
```
Formatting a disk will prepare the partition for the operating system to store data on the disk. The option fs=ntfs will set the used File System to [[AP1/GroupLearning/Anwendungen, Betriebssysteme.md#Dateisysteme|NTFS]] while the option quick will remove the file table but wont scan the disk for any bad sectors.

```cmd
DISKPART> assign
```
This will tell Windows to attach a letter to the partition. After this step the partition should be visible in the File Explorer. By default the next available letter will be assigned. By adding the option letter=E you can assign them by hand.
## Command Table
| Command                                                                                                                          | Description                                                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [active](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/active)                                | Marks the disk's partition with focus, as active.                                                                                                                                 |
| [add](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/add)                                      | Mirrors the simple volume with focus to the specified disk.                                                                                                                       |
| [assign](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/assign)                                | Assigns a drive letter or mount point to the volume with focus.                                                                                                                   |
| [attach vdisk](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/attach-vdisk)                    | Attaches (sometimes called mounts or surfaces) a virtual hard disk (VHD) so that it appears on the host computer as a local hard disk drive.                                      |
| [attributes](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/attributes)                        | Displays, sets, or clears the attributes of a disk or volume.                                                                                                                     |
| [automount](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/automount)                          | Enables or disables the automount feature.                                                                                                                                        |
| [break](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/break)                                  | Breaks the mirrored volume with focus into two simple volumes.                                                                                                                    |
| [clean](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/clean)                                  | Removes any and all partition or volume formatting from the disk with focus.                                                                                                      |
| [compact vdisk](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/compact-vdisk)                  | Reduces the physical size of a dynamically expanding virtual hard disk (VHD) file.                                                                                                |
| [convert](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/convert)                              | Converts file allocation table (FAT) and FAT32 volumes to the NTFS file system, leaving existing files and directories intact.                                                    |
| [create](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/create)                                | Creates a partition on a disk, a volume on one or more disks, or a virtual hard disk (VHD).                                                                                       |
| [delete](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/delete)                                | Deletes a partition or a volume.                                                                                                                                                  |
| [detach vdisk](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/detach-vdisk)                    | Stops the selected virtual hard disk (VHD) from appearing as a local hard disk drive on the host computer.                                                                        |
| [detail](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/detail)                                | Displays information about the selected disk, partition, volume, or virtual hard disk (VHD).                                                                                      |
| [exit](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/exit)                                    | Exits the diskpart command interpreter.                                                                                                                                           |
| [expand vdisk](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand-vdisk)                    | Expands a virtual hard disk (VHD) to the size that you specify.                                                                                                                   |
| [extend](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/extend)                                | Extends the volume or partition with focus, along with its file system, into free (unallocated) space on a disk.                                                                  |
| [filesystems](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/filesystems)                      | Displays information about the current file system of the volume with focus and lists the file systems that are supported for formatting the volume.                              |
| [format](https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/cc753770\(v=ws.11\)) | Formats a disk to accept files.                                                                                                                                                   |
| [gpt](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/gpt)                                      | Assigns the gpt attribute(s) to the partition with focus on basic GUID partition table (gpt) disks.                                                                               |
| [help](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/help)                                    | Displays a list of the available commands or detailed help information on a specified command.                                                                                    |
| [import](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/import_1)                              | Imports a foreign disk group into the disk group of the local computer.                                                                                                           |
| [inactive](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/inactive)                            | Marks the system partition or boot partition with focus as inactive on basic master boot record (MBR) disks.                                                                      |
| [list](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/list)                                    | Displays a list of disks, of partitions in a disk, of volumes in a disk, or of virtual hard disks (VHDs).                                                                         |
| [merge vdisk](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/merge-vdisk)                      | Merges a differencing virtual hard disk (VHD) with its corresponding parent VHD.                                                                                                  |
| [offline](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/offline)                              | Takes an online disk or volume to the offline state.                                                                                                                              |
| [online](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/online)                                | Takes an offline disk or volume to the online state.                                                                                                                              |
| [recover](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/recover)                              | Refreshes the state of all disks in a disk group, attempt to recover disks in an invalid disk group, and resynchronizes mirrored volumes and RAID-5 volumes that have stale data. |
| [rem](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/rem)                                      | Provides a way to add comments to a script.                                                                                                                                       |
| [remove](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/remove)                                | Removes a drive letter or mount point from a volume.                                                                                                                              |
| [repair](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/repair)                                | Repairs the RAID-5 volume with focus by replacing the failed disk region with the specified dynamic disk.                                                                         |
| [rescan](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/rescan)                                | Locates new disks that may have been added to the computer.                                                                                                                       |
| [retain](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/retain)                                | Prepares an existing dynamic simple volume to be used as a boot or system volume.                                                                                                 |
| [san](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/san)                                      | Displays or sets the storage area network (san) policy for the operating system.                                                                                                  |
| [select](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/select)                                | Shifts the focus to a disk, partition, volume, or virtual hard disk (VHD).                                                                                                        |
| [set id](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/set-id)                                | Changes the partition type field for the partition with focus.                                                                                                                    |
| [shrink](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/shrink)                                | Reduces the size of the selected volume by the amount you specify.                                                                                                                |
| [uniqueid](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/uniqueid)                            | Displays or sets the GUID partition table (GPT) identifier or master boot record (MBR) signature for the disk with focus.                                                         |

---
## Sources 
+ https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/diskpart