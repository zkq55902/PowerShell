# Hyper-V

**VM Summary with info on CPU and Memory used:**

*`Get-VM | Select-Object Name, @{Name='CPU'; Expression={$_.ProcessorCount}}, @{Name='Max mem [GB]'; Expression={If ($_.DynamicMemoryEnabled) {($_.MemoryMaximum/1GB).ToString("#,##0.##")} Else {($_.MemoryStartup/1Gb).ToString("#,##0.##")}}}, @{Name='Dynamic mem'; Expression={$_.DynamicMemoryEnabled}}, @{Name='Mem [GB]'; Expression={($_.MemoryAssigned/1GB).ToString("#,##0.##")}} | FT`*
