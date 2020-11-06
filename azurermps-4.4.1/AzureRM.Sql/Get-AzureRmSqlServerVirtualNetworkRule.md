---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587763"
---
# Get-AzureRmSqlServerVirtualNetworkRule

## SYNOPSIS
Azure SQL Server sanal ağ kuralını alır veya listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Bu komut, belirli bir Azure SQL Server sanal ağ kuralını veya bir sunucu altında Azure SQL Server sanal ağ kurallarının listesini alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

Tek bir Azure SQL Server sanal ağ kuralı alır

### Örnek 2
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

Belirtilen sunucunun altındaki Azure SQL Server sanal ağ kurallarının listesini alır

## PARAMETRELERINE

### -ResourceGroupName
Kaynak grubunun adı.

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

### -ServerName
Azure SQL Server adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRuleName
Azure SQL Server sanal ağ kuralı adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. VirtualNetworkRule. model. Azuressqlservervirtualnetworkrulemodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

