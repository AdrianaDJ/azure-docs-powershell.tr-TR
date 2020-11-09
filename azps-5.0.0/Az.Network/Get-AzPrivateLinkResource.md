---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323848"
---
# Get-AzPrivateLinkResource

## SYNOPSIS
Özel bir bağlantı kaynağı alır.

## INDEKI

### Byprivatelinkresourceıd (varsayılan)
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByResource
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## Tanım
**Get-AzPrivateLinkResource** cmdlet 'i tüm bağlantı kaynaklarını alır privatelinkresource.

## ÖRNEKLERDEN

### Örnek 1
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

Bu örnekte, tüm özel bağlantı kaynakları e-mySql adlı SQL Server 'a aittir.

## PARAMETRELERINE

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

### -Privatelinkresourceıd
Özel bağlantı kaynağının Azure Resource Manager kimliği.

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateLinkResourceType
Özel bağlantı kaynağı türü.

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Özel bağlantı hizmeti adı.

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
