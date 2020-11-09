---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320581"
---
# Get-AzDataLakeStoreFirewallRule

## SYNOPSIS
Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.
Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.

## INDEKI

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzDataLakeStoreFirewallRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.
Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.

## ÖRNEKLERDEN

### Örnek 1: belirli bir güvenlik duvarı kuralını alma
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

"Benimfirewallrule" adlı güvenlik duvarı kuralını "ContosoADL" hesabından döndürür

### Örnek 2: bir hesaptaki tüm güvenlik duvarı kurallarını listeleme
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

"ContosoADL" hesabındaki tüm güvenlik duvarı kurallarını döndürür

## PARAMETRELERINE

### -Hesap
Güvenlik duvarı kuralının alınacağı veri Lake Store hesabı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Ad
Alınacak güvenlik duvarı kuralının adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Belirtilen hesabın belirtilen güvenlik duvarı kuralını almak istediğiniz kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreFirewallRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
