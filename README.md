# To restore a USB flash drive to its full capacity using the command line in Windows 10, you can use the diskpart utility. Here are the steps:

1. Open the Command Prompt as an administrator. You can search for "Command Prompt" in the Start menu, right-click on it, and select "Run as administrator".
In the Command Prompt window, type the following command and press Enter:

`diskpart`
- This will open the DiskPart utility.

- Next, type the following command to list all the available
  `disk drives`


- Identify the USB flash drive you want to format by checking the size and disk number.

- Select the USB flash drive by typing the following command, replacing X with the disk number of your USB drive:

Copy code
select disk X

Once the USB drive is selected, clean the drive by typing the following command:

Copy codeclean
This command will remove all partitions and data from the USB drive.

Next, create a new primary partition on the USB drive:

Copy codecreate partition primary

After creating the partition, you need to format it. You can use the format command with different parameters based on your preferences. For example, to format the partition with the NTFS file system and the default cluster size, use the following command:

Copy codeformat fs=ntfs quick
If you want to perform a full format (which takes longer but is more thorough), omit the quick parameter.

After the format is complete, you can exit the DiskPart utility by typing the following command:

Copy codeexit
Your USB flash drive should now be restored to its full capacity (16 GB in your case) and formatted with the file system you specified.
Note: The diskpart utility is a powerful tool, and improper use can lead to data loss or system issues. Make sure to back up any important data before proceeding with these commands.
