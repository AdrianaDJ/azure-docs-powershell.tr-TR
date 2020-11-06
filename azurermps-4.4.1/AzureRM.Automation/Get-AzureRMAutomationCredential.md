---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: f00cbe95c71bdbd8c7f92f123756fa0c474d878f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595043"
---
# Get-AzureRmAutomationCredential

## SYNOPSIS
Otomasyon kimlik bilgilerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tümü (varsayılan)
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationCredential** cmdlet 'i bir veya daha çok Azure Otomasyonu kimlik bilgilerini alır.
Varsayılan olarak, tüm kimlik bilgileri verilir.
Belirli bir kimlik bilgisinin alınacağı kimlik bilgisinin adını belirtin.

Güvenlik amaçları doğrultusunda bu cmdlet kimlik bilgileri parolalarını döndürmez.

## ÖRNEKLERDEN

### Örnek 1: tüm kimlik bilgilerini alma
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerinin meta verilerini alır.

### Örnek 2: kimlik bilgileri alma
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

Bu komut, Contoso17 adlı Otomasyon hesabında ContosoCredential adlı kimlik bilgisinin meta verilerini alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in kimlik bilgilerini aldığı Otomasyon hesabının adını belirtir.

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

### -Ad
Alınacak kimlik bilgisinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in kimlik bilgilerini aldığı kaynak grubunu belirtir.

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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Credentialınfo

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmAutomationCredential](./New-AzureRMAutomationCredential.md)

[Remove-AzureRmAutomationCredential](./Remove-AzureRMAutomationCredential.md)

[Set-AzureRmAutomationCredential](./Set-AzureRMAutomationCredential.md)


