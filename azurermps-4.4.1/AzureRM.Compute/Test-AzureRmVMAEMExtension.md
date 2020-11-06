---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3c6f1ca4a50ccc359c1bbf10e63c9a9c0baf05fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594768"
---
# Test-AzureRmVMAEMExtension

## SYNOPSIS
AEM uzantısının yapılandırmasını denetler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Test-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.
AEM uzantısı performans verilerini toplar.
Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.

## ÖRNEKLERDEN

### Örnek 1: AEM uzantısının yapılandırmasını denetleme
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
İşletim sistemi diskinin işletim sisteminin türünü belirtir.
İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.
Bu parametre için kabul edilebilir değerler: Windows ve Linux.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorageCheck
Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Sanal makinenin adını belirtir.
Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Waittimeınminutes
Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)


