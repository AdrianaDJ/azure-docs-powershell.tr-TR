---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594643"
---
# Set-AzureRmMarketplaceTerms

## SYNOPSIS
Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin. Sözleşme şartlarını almak için lütfen Get-AzureRmMarketplaceTerms kullanın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### AgreementAcceptParameterSet (varsayılan)
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AgreementRejectParameterSet
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectAcceptParametrSet
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectRejectParametrSet
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar nesnesini kaydeder.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### Örnek 2
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## PARAMETRELERINE

### -Kabul et
Yasal koşulları kabul etmek için bunu iletin.

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -InputObject
Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi. Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Dağıtılan resmin tanımlayıcı dizesi.

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ürün
Dağıtılan resmin teklif tanımlayıcı dizesi.

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publisher
Dağıtılan resmin yayımcı tanımlayıcı dizesi.

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Red
Yasal şartları reddetmek için bunu iletin.

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Terimler
Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi. Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
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

### Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems
Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems
Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

