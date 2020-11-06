---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 479aaf61169cb09d8561e9f09b05a5852c93b58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586950"
---
# Restart-AzureRmVmss

## SYNOPSIS
Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Restart-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesini (VMSS) yeniden başlatır.
Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1: VMSS 'yi yeniden başlatın
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.

### Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.

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

### -InstanceId
Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS 'nin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

###  
Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Yeni-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Başlangıç-AzureRmVmss](./Start-AzureRmVmss.md)

[Dur-AzureRmVmss](./Stop-AzureRmVmss.md)

[Güncelleştirme-AzureRmVmss](./Update-AzureRmVmss.md)


