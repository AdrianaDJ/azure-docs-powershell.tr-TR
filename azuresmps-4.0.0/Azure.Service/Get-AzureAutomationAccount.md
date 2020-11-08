---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106371"
---
# Get-AzureAutomationAccount

## SYNOPSIS

Azure Otomasyonu hesaplarını alır.

## INDEKI

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationAccount** cmdlet 'i aboneliğiniz Için Microsoft Azure Otomasyon hesaplarını alır.
Otomasyon hesabı, diğer otomasyon hesaplarının kaynaklarından yalıtılmış olan otomasyon kaynakları için bir kapsayıcıdır.
Otomasyon kaynakları, runbook 'lar, işler ve varlıklar içerir.

## ÖRNEKLERDEN

### Örnek 1: Otomasyon hesabı alma
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

Bu komut, Contoso17 adlı Otomasyon hesabını alır.

## PARAMETRELERINE

### -Konum
Otomasyon hesaplarıyla ilişkili bir Azure konumunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Azure Otomasyonu hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. AutomationAccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureAutomationAccount](./New-AzureAutomationAccount.md)

[Remove-AzureAutomationAccount](./Remove-AzureAutomationAccount.md)


