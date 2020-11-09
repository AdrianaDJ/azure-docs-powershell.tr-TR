---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323953"
---
# Get-AzBillingAccount

## SYNOPSIS
Fatura hesapları edinin.

## INDEKI

### Liste (varsayılan)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Başına
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzBillingAccount** cmdlet 'i fatura hesaplarını alır, kullanıcının erişimi olur. 

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzBillingAccount
```

Kullanıcının erişebileceği tüm ödeme hesaplarını edinin.

### Örnek 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Belirtilen adla faturalandırma hesabı alın.

### Örnek 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Tüm faturalama hesaplarının kullanıcısına erişimi alın ve adresi sonuca ekleyin.

### Örnek 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Tüm faturalama hesaplarının kullanıcısına erişimi alın ve sonuç olarak faturalandırma profillerini ekleyin.

### Örnek 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Tüm faturalandırma hesaplarının kullanıcısına erişimi olan tüm fatura hesaplarını alın ve sonuç olarak bunların altında faturalandırma profilleri ve fatura bölümlerini ekleyin.

### Örnek 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Belirtilen adı taşıyan faturalandırma hesabını alın ve adres, faturalandırma profilleri ve fatura bölümlerini sonuçlarda ekleyin.

## PARAMETRELERINE

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

### -Includeaddress
Faturalandırma hesabının adresini ekleyin.

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

### -ExpandBillingProfile
Faturalandırma hesabı altına faturalandırma profilini ekleyin.

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

### -ExpandInvoiceSection
Faturalama hesabı ve fatura bölümlerinin altına faturalama profillerini ekleyin.

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

### -Ad
Belirli bir faturalandırma hesabının adı.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
Faturalandırma hesabı altında, abonelik oluşturmak için giriş olarak kullanılabilecek faturalandırma varlıklarını listeleyin.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. faturalandırma. modeller. PSBillingAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
