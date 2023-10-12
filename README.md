# HypervOVAConverter

## Powershell prerequisites (do with administrator rights)

1. for Windows 10
    ```
    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
    ```
    or for Windows 8
    ```
    Add-WindowsFeature RSAT-Hyper-V-Tools –IncludeAllSubFeature
    ```

1. then do Hyper-V VM export

## Convert exported Hyper-V VM to .ova
```
Convert-VM.ps1 –HyperVVMPath <string> –OVAPath <string> [-TmpCopyPath <string>] [<CommonParameters>] 
```
* "HyperVVMPath" must contain path to exported Hyper-V VM
* "OVAPath" must contain path to converted VM
* Optionally set "TmpCopyPath" to convert VM on system where this VM currently runs.

## Convert virtual drive .vhd/.vhdx to .ova
```
Convert-VM.ps1 –VHDPath <string> –OVAPath <string> [–CPU <byte>] [–Memory <byte>] [<CommonParameters>]
```
