---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 99a575d4eb17cc41eeea49f1db2a801bb6a28c98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586675"
---
# Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys

## SYNOPSIS
Belirtilen Access tuşunu sıfırlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet 'ı Power BI çalışma alanı koleksiyonunuzda belirtilen Access tuşunu sıfırlar.

## ÖRNEKLERDEN

### Örnek 1: birincil erişim anahtarını sıfırlama
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için birincil erişim anahtarını sıfırlar.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Anahtar
Bu cmdlet 'in birincil erişim anahtarını sıfırtığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Anahtar2
Bu cmdlet 'in ikincil erişim tuşunu sıfırtığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Koleksiyonun kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceCollectionName
Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmPowerBIWorkspaceCollectionAccessKeys](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


