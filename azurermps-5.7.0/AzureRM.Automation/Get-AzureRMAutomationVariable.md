---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595123"
---
# Get-AzureRmAutomationVariable

## SYNOPSIS
Bir Otomasyon değişkeni alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tümü (varsayılan)
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationVariable** cmdlet 'i bir veya birden çok Azure Otomasyonu değişkenini alır.
Belirli bir değişken almak için adını belirtin.

## ÖRNEKLERDEN

### Örnek 1: değişken alma
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

İlk komut, Contoso17 adlı hesapta Variable06 adlı bir Otomasyon değişkeni alır.
Komut bu nesneyi $Variable değişkeninde depolar.

İkinci komut, $Variable **değer** özelliğine başvuruda bulunmak için standart nokta gösterimini kullanır.
Komut $value değişkeninde değeri depolar.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in aldığı değişkenleri içeren Otomasyon hesabının adını belirtir.

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

### -Ad
Bu cmdlet 'in aldığı değişkenin adını belirtir.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in değişkenleri aldığı kaynak grubunu belirtir.

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

### Microsoft. Azure. Commands. Automation. model. Variable

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmAutomationVariable](./New-AzureRMAutomationVariable.md)

[Remove-AzureRmAutomationVariable](./Remove-AzureRMAutomationVariable.md)

[Set-AzureRmAutomationVariable](./Set-AzureRMAutomationVariable.md)


