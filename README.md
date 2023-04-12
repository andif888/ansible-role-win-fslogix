# ansible-role-win-fslogix

Role to install FSLogix on Windows.

## Table of content

- [Default Variables](#default-variables)
  - [fslogix_download_url](#fslogix_download_url)
  - [fslogix_extract_dir](#fslogix_extract_dir)
  - [fslogix_no_restart](#fslogix_no_restart)
  - [fslogix_officecontainer_enabled](#fslogix_officecontainer_enabled)
  - [fslogix_officecontainer_exclude_list](#fslogix_officecontainer_exclude_list)
  - [fslogix_officecontainer_include_teams](#fslogix_officecontainer_include_teams)
  - [fslogix_officecontainer_size_in_mbs](#fslogix_officecontainer_size_in_mbs)
  - [fslogix_officecontainer_use_config](#fslogix_officecontainer_use_config)
  - [fslogix_officecontainer_vhd_access_mode](#fslogix_officecontainer_vhd_access_mode)
  - [fslogix_officecontainer_vhd_locations](#fslogix_officecontainer_vhd_locations)
  - [fslogix_officecontainer_vhd_sector_size](#fslogix_officecontainer_vhd_sector_size)
  - [fslogix_officecontainer_volume_type](#fslogix_officecontainer_volume_type)
  - [fslogix_profilecontainer_delete_local_profile_when_vhd_should_apply](#fslogix_profilecontainer_delete_local_profile_when_vhd_should_apply)
  - [fslogix_profilecontainer_enabled](#fslogix_profilecontainer_enabled)
  - [fslogix_profilecontainer_exclude_list](#fslogix_profilecontainer_exclude_list)
  - [fslogix_profilecontainer_frxtray_enabled](#fslogix_profilecontainer_frxtray_enabled)
  - [fslogix_profilecontainer_profile_type](#fslogix_profilecontainer_profile_type)
  - [fslogix_profilecontainer_size_in_mbs](#fslogix_profilecontainer_size_in_mbs)
  - [fslogix_profilecontainer_use_config](#fslogix_profilecontainer_use_config)
  - [fslogix_profilecontainer_vhd_locations](#fslogix_profilecontainer_vhd_locations)
  - [fslogix_profilecontainer_vhd_sector_size](#fslogix_profilecontainer_vhd_sector_size)
  - [fslogix_profilecontainer_volume_type](#fslogix_profilecontainer_volume_type)
  - [fslogix_rule_editor_install](#fslogix_rule_editor_install)
  - [fslogix_rule_editor_product_id](#fslogix_rule_editor_product_id)
  - [fslogix_rule_files_contents](#fslogix_rule_files_contents)
  - [fslogix_service_product_id](#fslogix_service_product_id)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### fslogix_download_url

download URL

#### Default value

```YAML
fslogix_download_url: https://download.microsoft.com/download/c/4/4/c44313c5-f04a-4034-8a22-967481b23975/FSLogix_Apps_2.9.8440.42104.zip
```

### fslogix_extract_dir

extract directory

#### Default value

```YAML
fslogix_extract_dir: C:\Windows\Temp\fslogix
```

### fslogix_no_restart

Prevent restart after driver install

#### Default value

```YAML
fslogix_no_restart: false
```

### fslogix_officecontainer_enabled

Enable office container feature

#### Default value

```YAML
fslogix_officecontainer_enabled: false
```

### fslogix_officecontainer_exclude_list

List of users or groups to exclude from office container feature

#### Default value

```YAML
fslogix_officecontainer_exclude_list:
  - Administrators
```

### fslogix_officecontainer_include_teams

Include Teams in container

#### Default value

```YAML
fslogix_officecontainer_include_teams: 1
```

### fslogix_officecontainer_size_in_mbs

Office container size in megabytes

#### Default value

```YAML
fslogix_officecontainer_size_in_mbs: 10240
```

### fslogix_officecontainer_use_config

Set to true to execute task config_officecontainer.yml

#### Default value

```YAML
fslogix_officecontainer_use_config: false
```

### fslogix_officecontainer_vhd_access_mode

VHD Access Mode (0,1,2,3)

#### Default value

```YAML
fslogix_officecontainer_vhd_access_mode: 0
```

### fslogix_officecontainer_vhd_locations

VHD Locations

#### Default value

```YAML
fslogix_officecontainer_vhd_locations:
  - \\fileserver\fslogixodfc
```

### fslogix_officecontainer_vhd_sector_size

VHDX sector size

#### Default value

```YAML
fslogix_officecontainer_vhd_sector_size: 4096
```

### fslogix_officecontainer_volume_type

Volume Type (vhd, vhdx)

#### Default value

```YAML
fslogix_officecontainer_volume_type: vhdx
```

### fslogix_profilecontainer_delete_local_profile_when_vhd_should_apply

delete local profile when vhd should apply

#### Default value

```YAML
fslogix_profilecontainer_delete_local_profile_when_vhd_should_apply: false
```

### fslogix_profilecontainer_enabled

Enable profile container feature

#### Default value

```YAML
fslogix_profilecontainer_enabled: false
```

### fslogix_profilecontainer_exclude_list

List of users or groups to exclude from profile container feature

#### Default value

```YAML
fslogix_profilecontainer_exclude_list:
  - Administrators
```

### fslogix_profilecontainer_frxtray_enabled

Enable frxtray application

#### Default value

```YAML
fslogix_profilecontainer_frxtray_enabled: false
```

### fslogix_profilecontainer_profile_type

Profile Type (0,1,2,3)

#### Default value

```YAML
fslogix_profilecontainer_profile_type: 0
```

### fslogix_profilecontainer_size_in_mbs

Profile container size in megabytes

#### Default value

```YAML
fslogix_profilecontainer_size_in_mbs: 5120
```

### fslogix_profilecontainer_use_config

Set to true to execute task config_profilecontainer.yml

#### Default value

```YAML
fslogix_profilecontainer_use_config: false
```

### fslogix_profilecontainer_vhd_locations

VHD Locations

#### Default value

```YAML
fslogix_profilecontainer_vhd_locations:
  - \\fileserver\fslogixprofiles
```

### fslogix_profilecontainer_vhd_sector_size

VHDX sector size

#### Default value

```YAML
fslogix_profilecontainer_vhd_sector_size: 4096
```

### fslogix_profilecontainer_volume_type

Volume Type (vhd, vhdx)

#### Default value

```YAML
fslogix_profilecontainer_volume_type: vhdx
```

### fslogix_rule_editor_install

Set to true to install FSLogix Rule Editor

#### Default value

```YAML
fslogix_rule_editor_install: false
```

### fslogix_rule_editor_product_id

product id to check if already installed

#### Default value

```YAML
fslogix_rule_editor_product_id: '{8530E679-5D70-43A7-9EE8-ABADCFCDCB7B}'
```

### fslogix_rule_files_contents

Directory path which contains rule files to copy

#### Default value

```YAML
fslogix_rule_files_contents: ''
```

### fslogix_service_product_id

product id to check if already installed

#### Default value

```YAML
fslogix_service_product_id: '{18F03C3D-4235-4F6A-A222-B13BA34F25C8}'
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
