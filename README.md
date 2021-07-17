# package-flippy-openwrt


# Parameters

| Inputs | Type |Description | Value |
| --- | --- | --- |--- |
| types           | String | The type of the drive (required)|   Default is s905d.  Multi version compilation: s905d,s905x2.        |
| openwrt-version | String | The openwrt version  |  Default null   |
|kernel-version| String | The kernel version | Default is Latest. Latest is the latest of +o.  latest+ is the latest of + |
|whoami|  String | The name of build the openwrt | Default is mingxiaoyu|
|out| String | The output path of the openwrt  | Default is /out |
|openwrt-path| String | The input path of the openwrt |   Default is null. openwrt-path or openwrt-url should have one.  |
|openwrt-url| String | The url of the openwrt|  Default is null. openwrt-path or openwrt-url should have one.  |
|sub-name |  String | add the sub name in file: xxxx-xx-{sub-name}.img.gz| Default is null |
    
 kernel-version check in [flippy-packages](https://github.com/doctor-design/flippy-packages)   
 types: plus,beikeyun,l1pro,s905,s905d,s905x2,s905x3,s912,s922x.
 
| OutPuts | Type | Description | Value |
| --- | --- | --- | --- |
| status | boolean | The status of action | true or false |

# Usage the aciton


 name: Package OpenWrt with flippy script
  # You may pin to the exact commit or the version.
  uses: doctor-design/package-flippy-openwrt@main
  with:
    # The type of the drive
    types: # optional, default is s905d
    # The openwrt version
    openwrt-version: # optional
    # The kernel version
    kernel-version: # optional, Latest
    # The name of build the openwrt
    whoami: # optional, default is mingxiaoyu
    # The output path of the openwrt
    out: # optional, default is /out
    # The input path of the openwrt
    openwrt-path: # optional
    # The url of the openwrt
    openwrt-url: # optional
    # add the sub name in file: xxxx-xx-{sub-name}.img.gz
    sub-name: # optional
 ```
 simple
 ```
 name: Package OpenWrt with flippy script
  # You may pin to the exact commit or the version.
  uses: doctor-design/package-flippy-openwrt@main
  with:
    # The type of the drive
    types: # optional, default is s905d
    # The input path/ulr of the openwrt
    openwrt-path/openwrt-url: # optional
