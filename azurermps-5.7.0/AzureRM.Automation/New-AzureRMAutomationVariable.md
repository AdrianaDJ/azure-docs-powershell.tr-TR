---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593751"
---
# New-AzureRmAutomationVariable

## SYNOPSIS
Otomasyon değişkeni oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**New-AzureRmAutomationVariable** cmdlet 'ı Azure Otomasyonu 'nda bir değişken oluşturur.
Değişkeni şifrelemek için, *şifrelenen* parametreyi belirtin.
Oluşturulduktan sonra bir değişkenin şifreli durumunu değiştiremezsiniz.

## ÖRNEKLERDEN

### Örnek 1: basit bir değer içeren bir değişken oluşturma
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

Bu komut, Contoso17 adlı Otomasyon hesabında dize değeriyle birlikte StringVariable22 adlı bir değişken oluşturur.

### Örnek 2: karmaşık bir değer içeren bir değişken oluşturma
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

İlk komut, Get-AzureVM cmdlet 'ini kullanarak sanal makine alır.
Komut, $VirtualMachine değişkeninde depolar.

İkinci komut, Contoso17 adlı Otomasyon hesabında ComplexVariable01 adlı bir değişken oluşturur.
Bu komut, değeri için, bu örnekte $VirtualMachine sanal makinesi olan karmaşık bir nesneyi kullanır.

## PARAMETRELERINE

### -AutomationAccountName
Değişkenin depolanacağı Otomasyon hesabının adını belirtir.

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

### -Açıklama
Değişken için bir açıklama belirtir.

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

### -Şifreli
Bu cmdlet 'in değişkenin değerini depolama için şifreleyip şifrelenemeyeceğini belirtir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Değişken için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in değişken oluşturduğu kaynak grubunu belirtir.

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

### -Değer
Değişken için bir değer belirtir.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Get-AzureRmAutomationVariable](./Get-AzureRMAutomationVariable.md)

[Remove-AzureRmAutomationVariable](./Remove-AzureRMAutomationVariable.md)

[Set-AzureRmAutomationVariable](./Set-AzureRMAutomationVariable.md)


