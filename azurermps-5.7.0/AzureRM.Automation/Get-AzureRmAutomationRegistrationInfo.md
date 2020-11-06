---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586828"
---
# Get-AzureRmAutomationRegistrationInfo

## SYNOPSIS
DSC düğümünü veya karma çalışanı otomatikleştirme 'ye eklemek için kayıt bilgilerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermautomationregistrationınfo** cmdlet 'ı, Istenen durum YAPıLANDıRMASı (DSC) düğümünü veya karma çalışanı bir Azure Otomasyonu hesabına eklemek için gereken uç nokta ve anahtarları alır.

## ÖRNEKLERDEN

### Örnek 1: kayıt bilgilerini alma
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Otomasyon hesabının kayıt bilgilerini alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in kayıt bilgilerini aldığı Otomasyon hesabının adını belirtir.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği kaynak grubunun kayıt bilgilerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### Microsoft. Azure. Commands. Automation. model. AgentRegistration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAutomationAccount](./Get-AzureRmAutomationAccount.md)

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Yeni-AzureRmAutomationKey](./New-AzureRmAutomationKey.md)


