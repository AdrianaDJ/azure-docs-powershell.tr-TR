---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595078"
---
# Get-AzureRmNetworkProfile

## SYNOPSIS
Var olan bir ağ profili üst düzey kaynağını alır

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoExpand (varsayılan)
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceNameExpandParameterSet
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyresourcenparameteroexpandparameterset
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyresourceidexpanvseçparameterset
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyresourceıdnoexpandparameterset
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmNetworkProfile** cmdlet 'i mevcut bir ağ profili üst düzey kaynağı alır

## ÖRNEKLERDEN

### Örnek 1
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

Bu, kaynak grubundaki NP1 ağ profilini alır RG1

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

### -ExpandResource
Genişletilecek kaynak başvurusu.

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Ağ profilinin adı.

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Ağ profilinin kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Ağ profilinin Azure Kaynak Yöneticisi kimliği.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
