---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: a9e9f5fdc71250acb2496c8eaaf1677461e9cd07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098352"
---
# Remove-AzDataShare

## SYNOPSIS
Veri paylaşımını kaldırır.

## INDEKI

### ByFieldsParameterSet (varsayılan)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Byresourceıdparameterset
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzDataShare** cmdlet 'i veri paylaşımını kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Bu komut, Azure veri paylaşımı hesap WikiAds adındaki AdsShare adlı veri paylaşımını kaldırır. 

## PARAMETRELERINE

### -AccountName
Azure veri paylaşımı hesap adı

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
{{Fill Iş açıklaması}}

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

### -InputObject
Azure veri paylaşımı nesnesi ' ' ' YAML türü: PSDataShare parametre kümeleri: ByObjectParameterSet diğer adları: 

Gerekli: doğru konum: adlandırılmış varsayılan değer: None kabul etme girişi: doğru (ByValue) joker karakterleri kabul et: false


### -Ad
Azure veri paylaşımı adı

YAML türü: dize parametre kümeleri: ByFieldsParameterSet diğer adları: 

Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false


### -Geçiş
Return Object (belirtilmişse).

YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar: 

Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false


### -ResourceGroupName
Azure veri paylaşımı hesabının kaynak grubu adı

YAML türü: dize parametre kümeleri: ByFieldsParameterSet diğer adları: 

Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false


### -RESOURCEID
Azure veri paylaşımı 'nın kaynak kimliği

YAML türü: dize parametre kümeleri: Byresourceıdparameterset diğer adları: 

Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: true (ByPropertyName) joker karakter kabul et: false


### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar: CF

Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false


### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar: WI

Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Azure veri paylaşımı adı

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Return Object (belirtilmişse).

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

### -ResourceGroupName
Azure veri paylaşımı hesabının kaynak grubu adı

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Azure veri paylaşımı 'nın kaynak kimliği

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
