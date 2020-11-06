---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 3d6d3628ba15fa4b775f4c747a29645ec0628402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595116"
---
# Get-AzureRmAutomationDscConfiguration

## SYNOPSIS
Otomasyondan DSC yapılandırmalarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tümü (varsayılan)
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationDscConfiguration** cmdlet 'i, Mac otomasyonundan APS Istenen durum yapılandırma (DSC) yapılandırmalarını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm DSC yapılandırmalarını alma
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm DSC yapılandırmalarının meta verilerini alır.

### Örnek 2: ada göre bir DSC yapılandırması alma
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

Bu komut, Contoso17 adlı Otomasyon hesabında MyConfiguration adlı bir DSC yapılandırmasının meta verilerini alır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in aldığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.

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
Bu cmdlet 'in aldığı DSC yapılandırmasının adını belirtir.

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.

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

### Microsoft. Azure. Commands. Automation. model. DscConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Dışarı aktarma-AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[Import-AzureRmAutomationDscConfiguration](./Import-AzureRmAutomationDscConfiguration.md)


