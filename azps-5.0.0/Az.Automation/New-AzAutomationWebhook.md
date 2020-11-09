---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321849"
---
# New-AzAutomationWebhook

## SYNOPSIS
Otomasyon Runbook için Web kancası oluşturur.

## INDEKI

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook için Web kancası oluşturur.
Bu cmdlet 'in döndürdüğü Web kancası URL 'sini kaydettiğinizden emin olun, çünkü yeniden alamazsınız.

## ÖRNEKLERDEN

### Örnek 1: Web kancası oluşturma
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Bu komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook06 adında bir Web kancası oluşturur.
Komut, $Webhook değişkeninde Web kancasını depolar.
Web kancası etkinleştirildi.
Web kancası belirtilen zamanda sona erecek.
Bu komut Web kancası parametreleri için hiçbir değer sağlamaz.
Bu komut *Force* parametresini belirtir.
Bu nedenle sizden onay istemez.

### Örnek 2: parametrelerle bir Web kancası oluşturma
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

İlk komut, bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.
İkinci komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook11 adında bir Web kancası oluşturur.
Komut, $Params parametreleri Web kancası 'na atar.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in Web kancası oluşturduğu Otomasyon hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### -ExpiryTime
Web kancası için son kullanma süresini **DateTimeOffset** nesnesi olarak belirtir.
Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize veya **TarihSaat** belirtebilirsiniz.

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
ps_force

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

### -IsEnabled
Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Web kancası için bir ad belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parametreler
Anahtar/değer çiftleri sözlüğünü belirtir.
Anahtarlar, runbook parametre adlarıdır.
Değerler runbook parametre değerleridir.
Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in Web kancası oluşturduğu kaynak grubunun adını belirtir.

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

### -RunbookName
Web kancası ile ilişkilendirilecek runbook adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Runbook 'u yürütecek karma çalışanı grubunun isteğe bağlı adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Boolean

### System. DateTimeOffset

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Web kancası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azautomationweb kancası](./Get-AzAutomationWebhook.md)

[Remove-Azautomationweb kancası](./Remove-AzAutomationWebhook.md)

[Set-Azautomationweb kancası](./Set-AzAutomationWebhook.md)


