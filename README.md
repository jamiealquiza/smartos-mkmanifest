# mkmanifest
Mkmanifest is a quick tool that helps create VM (KVM based) datasets that can be imported into standalone SmartOS servers or imported into Joyent SmartDataCenter. Datasets are master images consisting of a compressed ZFS snapshot of a prepped VM disk, in addition to metadata describing the VM. Datasets are housed in a repository and cloned to deploy end-user VMs.

NOTICE: Please edit the script to include your private details. All '***' variables must be updated before running.

Sample usage:

	./mkmanifest

	::: Please select a VM (ensure VM is powered off):

	1:      bcf70dbf-c713-4307-be69-7569a9a74c25  stopped           App-0.0.1
	2:      c6083c22-51c0-4204-a828-215b15cebe10  stopped           Node-1.1.5
	3:      8e11cdc8-ea7c-4302-8ba2-833f63d09e31  stopped           TEST4
	4:      d044c0c2-7bf6-4781-a906-8566ea4a3aac  running           Mailbox
	5:      6672f8e9-891e-4049-b423-3c40e2b91553  running           Puppet
	6:      e114ee77-67c1-4f2b-8a74-3743002c1870  running           VBWilk
	7:      f08223c0-f6df-4ece-a8e2-df5ff57bf816  running           Ops_Siege

	VM Number: 1

	Image Name: Cloud-App
	Image Version: 1.0.0
	Image Description: General App Server
	Operating System: CentOS 6.3
	Image Root Disk Size [MB] (Blank to use detected: 16384): 

	::: Create a dataset using the following:

	Virtual Machine:                App-0.0.1
	Image Name:                     Cloud-App
	Image Version:                  1.0.0
	Image Description:              General App Server
	Operating System:               CentOS 6.3
	Image Root Disk Size [MB]:      16384

	Proceed with these settings? (y/N): y

	::: Creating snapshot
	::: Creating a compressed image. This may take a moment...

	Destination directory for dataset (blank for: /opt): 

	::: Done! Dataset can be found at:
	/opt/Cloud-App-1.0.0
