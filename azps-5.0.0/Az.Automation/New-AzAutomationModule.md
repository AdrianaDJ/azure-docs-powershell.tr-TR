---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321870"
---
# New-AzAutomationModule

## SYNOPSIS
Bir modülü otomatikleştirme 'ye aktarır.

## INDEKI

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.
Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.
Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir: 
- . Psm1 veya. dll dosya adı uzantısına sahip Windows PowerShell modülü 
- . Psd1 dosya adı uzantısına sahip Windows PowerShell modülü bildirimi. zip dosyasının adı, klasörün adı ve klasörün adı aynı olmalıdır.
. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.
Windows PowerShell modülünü bu cmdlet 'i veya Set-AzAutomationModule cmdlet 'ini kullanarak Otomasyon 'a aktarırsanız, işlem zaman uyumsuzdur.
Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.
Başarılı olup olmadığını denetlemek için, aşağıdaki komutu çalıştırarak: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName başarılı bir şekilde **provisioningstate** özelliğini denetleyin.

## ÖRNEKLERDEN

### Örnek 1: modül Içeri aktarma
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.
Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in modül aldığı Otomasyon hesabının adını belirtir.

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

### -ContentLinkUri
Modül zip paketinin URL 'si

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
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

### -Ad
Bu cmdlet 'in içeri aktardığından modülün adını belirtir.

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

### -ResourceGroupName
Bu cmdlet 'in modül aldığı kaynak grubunun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Uri

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Module

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


