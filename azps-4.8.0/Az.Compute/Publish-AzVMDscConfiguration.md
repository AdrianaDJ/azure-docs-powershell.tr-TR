---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109809"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
DSC betiğini Azure Blob depolama alanına yükler.

## INDEKI

### UploadArchive (varsayılan)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Publish-AzVMDscConfiguration** cmdlet 'i Azure Blob depolama 'ya, daha sonra Set-AzVMDscExtension cmdlet kullanılarak Azure sanal makinelere uygulanabilecek bir Istenen durum YAPıLANDıRMASı (DSC) kodu yükler.

## ÖRNEKLERDEN

### Örnek 1:. zip paketi oluşturma
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu Azure depolama birimine yükler.

### Örnek 2:. zip paketi oluşturma ve yerel dosyaya depolama
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu .\MyConfiguration.ps1.zip adlı yerel dosyada depolar.

### Örnek 3: arşive yapılandırma ekleme ve ardından depolama birimine yükleme
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Bu Sample.ps1 komut, Azure depolama 'ya yüklemek ve bağımlı kaynak modüllerini atlar.

### Örnek 4: arşive yapılandırma ve yapılandırma verileri ekleme ve ardından depolama birimine yükleme
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Bu komut, Azure depolama 'ya yüklemek için yapılandırma arşivine SampleData.psd1 adlı Sample.ps1 adlı yapılandırmayı ekler.

### Örnek 5: arşive yapılandırma, yapılandırma verileri ve ek içerik ekleme ve ardından depolama birimine yükleme
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Bu komut Sample.ps1, yapılandırma verileri SampleData.psd1 adlı yapılandırmayı ve Azure depolama 'ya yüklenecek yapılandırma arşivine ek içeriği ekler.

## PARAMETRELERINE

### -Addiyolu
Yapılandırma arşivine eklenecek dosyanın veya dizinin yolunu belirtir.
Yapılandırmayla birlikte sanal makineye indirilir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Yapılandırma verilerini belirten bir. psd1 dosyasının yolunu belirtir.
Bu, yapılandırma arşivine eklenir ve ardından yapılandırma işlevine geçirilir.
Set-AzVMDscExtension cmdlet ile sağlanan yapılandırma veri yolunun üzerine yazılır

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Bir veya daha fazla yapılandırma içeren dosyanın yolunu belirtir.
Dosya bir Windows PowerShell betik (. ps1) dosyası veya Windows PowerShell modülü (. psm1) dosyası olabilir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Kapsayıcıadı
Yapılandırmanın karşıya yüklediği Azure depolama kapsayıcısı 'nın adını belirtir.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputArchivePath
Yapılandırma Arşivi yazılacak yerel. zip dosyasının yolunu belirtir.
Bu parametre kullanıldığında, yapılandırma betiği Azure Blob depolama alanına yüklenmez.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Depolama hesabını içeren kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Bu cmdlet 'in DSC Kaynak bağımlılıklarını yapılandırma arşivinden dışarıda tutuyorsa gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
*ContainerName* parametresinde belirtilen kapsayıcıya yapılandırma betiğini yüklemek Için kullanılan Azure depolama hesap adını belirtir.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Depolama uç noktasının sonekini belirtir.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. String []

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


