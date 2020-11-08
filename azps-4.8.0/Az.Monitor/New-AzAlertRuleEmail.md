---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267106"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Uyarı kuralı için e-posta eylemi oluşturur.

## INDEKI

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzAlertRuleEmail** cmdlet 'i, bir uyarı kuralı için e-posta eylemi oluşturur.

## ÖRNEKLERDEN

### Örnek 1: hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturma
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Bu komut, bir uyarı kuralı başlatıldığında hizmet sahipleri için gönderilecek bir uyarı kuralı e-posta eylemi oluşturur.

### Örnek 2: hizmet dışı sahipler için uyarı kuralı oluşturma
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Bu komut belirtilen e-posta adresleri için bir uyarı kuralı e-posta eylemi oluşturur, ancak hizmet sahipleri için kullanılmaz.

### Örnek 3: hizmet sahipleri ve hizmet dışı sahipler için bir uyarı kuralı e-posta eylemi oluşturma
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Bu komut, belirtilen adres ve hizmet sahipleri için bir uyarı kuralı e-posta eylemi oluşturur.

## PARAMETRELERINE

### -Customeposta
Virgülle ayrılmış e-posta adreslerinin listesini belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -SendToServiceOwner
Bu işlemin, kural tetiklendiğinde hizmet sahiplerine e-posta gönderdiğini gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String []

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Management. Monitor. Management. modeller. Ruleemailate

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Add-Azmetrik ıalertrule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[Yeni-Azalertruleweb kancası](./New-AzAlertRuleWebhook.md)


