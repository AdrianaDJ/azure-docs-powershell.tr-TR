---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588943"
---
# Get-AzureRmDataLakeStoreFirewallRule

## SYNOPSIS
Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.
Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzureRmDataLakeStoreFirewallRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.
Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.

## ÖRNEKLERDEN

### Örnek 1: belirli bir güvenlik duvarı kuralını alma
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

"Benimfirewallrule" adlı güvenlik duvarı kuralını "ContosoADL" hesabından döndürür

### Örnek 2: bir hesaptaki tüm güvenlik duvarı kurallarını listeleme
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

"ContosoADL" hesabındaki tüm güvenlik duvarı kurallarını döndürür

## PARAMETRELERINE

### -Hesap
Güvenlik duvarı kuralının alınacağı veri Lake Store hesabı.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak güvenlik duvarı kuralının adı

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### DataLakeStoreFirewallRule
Belirtilen güvenlik duvarı kuralı

### 'Te<DataLakeStoreFirewallRule>
Belirtilen hesaptaki Güvenlik Duvarı kurallarının listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

