---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108087"
---
# New-AzImageBuilderCustomizerObject

## SYNOPSIS
Bir resim özelleştirme birimi tanımlar

## INDEKI

### Shellözelleştirici (varsayılan)
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### Dosya Özelleştirici
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### Powershellözelleştirici
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### RestartCustomizer
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### Windowsupdateözelleştirici
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## Tanım
Bir resim özelleştirme birimi tanımlar

## ÖRNEKLERDEN

### Örnek 1: Windows Update Özelleştirici oluşturma
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

Bu komut Windows Update Özelleştirici oluşturur.

### Örnek 2: dosya Özelleştirici oluşturma
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

Bu komut bir dosya Özelleştirici oluşturur.

### Örnek 3: PowerShell Özelleştirici oluşturma
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

Bu komut, PowerShell Özelleştirici oluşturur.

### Örnek 4: yeniden başlatma Özelleştirici oluşturma
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

Bu komut, yeniden başlatma Özelleştirici oluşturur.

### Örnek 5: kabuk Özelleştirici oluşturma
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

Bu komut, kabuk Özelleştirici oluşturur.

## PARAMETRELERINE

### -CustomizerName
Bu özelleştirme adımında bağlam sağlamak için kolay ad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hedef
Dosyanın (sourceUri 'den) VM 'de yükleneceği bir dosyanın mutlak yolu (halen oluşturulmuş olan iç içe dizin yapıları ile).

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fileözelleştirici
Dosyaları VM 'lere (Linux, Windows) yükler.
Packer dosya hazırlayıcısı 'na karşılık gelir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtre
Uygulanacak güncelleştirmeleri seçmek için filtre dizisi.
Varsayılanı (filtre yok) kullanmak için boş dizi atlayın veya belirtin.
Örnekler ve bu alanın ayrıntılı açıklaması için yukarıdaki bağlantıya bakın.

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Satır içi
Yürütülecek kabuk komutlarının dizisi.

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Powershellözelleştirici
VM 'de belirtilen PowerShell 'i (Windows) çalıştırır.
Packer PowerShell hazırlayıcısı 'na karşılık gelir.
Tam olarak ' scriptUri ' veya ' inline ' belirtilebilir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCheckCommand
Yeniden başlatmanın başarılı olup olmadığını denetleme komutu [varsayılan: ' '].

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCommand
Yeniden başlatmayı yürütme komutu [Default: ' Shutdown/r/f/t 0/c Packer Restart ']

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartCustomizer
Bir VM 'yi yeniden başlatır ve geri dönmek için bekler (Windows).
Windows 'un yeniden başlatma hazırlayıcısı 'na karşılık gelir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartTimeout
Yeniden başlatma zaman aşımı, bir büyüklük ve birim dizesi olarak belirtildi; Örneğin, ' 5m ' (5 dakika) veya ' 2 saat) [varsayılan: ' 5m '].

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Runyükselmesine
Belirtilmişse, PowerShell betiği yükseltilmiş ayrıcalıklarla çalıştırılır.

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptUri
Özelleştirme için çalıştırılacak kabuk betiğinin URI 'SI.
Bir GitHub bağlantısı, Azure depolama için SAS URI 'SI olabilir.

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aramaölçütü
Güncellemeleri arama ölçütleri.
Varsayılanı (tümünü ara) kullanmak için boş dize kullanmayın veya belirtin.
Örnekler ve bu alanın ayrıntılı açıklaması için yukarıdaki bağlantıya bakın.

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sha256Checksum
ScriptUri alanında sağlanan kabuk betiğinin SHA256 sağlama toplamı.

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Shellözelleştirici
Özelleştirme aşamasında (Linux) bir kabuk betiğini çalıştırır.
Packer kabuğu hazırlayıcısı 'na karşılık gelir.
Tam olarak ' scriptUri ' veya ' inline ' belirtilebilir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceUri
VM 'yi özelleştirmek için karşıya yüklenecek dosyanın URI 'SI.
Bir GitHub bağlantısı, Azure depolama için SAS URI 'SI olabilir.

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateLimit
Bir kerede uygulanacak en fazla güncelleştirme sayısı.
Varsayılanı (1000) kullanmak için atlayın veya 0 değerini belirtin.

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidExitCode
PowerShell betiği için geçerli çıkış kodları.
[Varsayılan: 0].

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Windowsupdateözelleştirici
Windows güncelleştirmelerini yükler.
Windows Update Provisioner ( https://github.com/rgl/packer-provisioner-windows-update) .

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplateözelleştirici

## NOTLARıNDA

DIĞER adları

## ILGILI BAĞLANTıLAR

