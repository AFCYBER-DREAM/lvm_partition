Docker Setup
=========

Creates a new volume group and logical volume on a raw unpartitioned disk and ensures that it is mounted.

Requirements
------------

None

Role Variables
--------------

| Variable Name | Description | Default |
|---------------|-------------|---------|
| vg_name | Name of the vg to create. | **vg_data** |
| lv_name | Name of Logical Volume to create. | **lv_data** |
| device | Device physical volume/partition exists on: | **/dev/sdb** |
| add_space | Percentage of drive to add to the VG?: | **100** |
| unit | Unit type to use with parted. | **%** |
| mount_point | Where to mount the new lvm. | **/mnt** |
| filesystem | Filesystem to use for the new volume. | **ext4** |
| part_number | Which partition to start with. | **1** |

Dependencies
------------

None

Example Playbook
----------------

A use example:

    - hosts: servers
      roles:
         - { role: lvm_partition }

License
-------

MIT

Author Information
------------------

The Development Range Engineering, Architecture, and Modernization (DREAM) Team.
