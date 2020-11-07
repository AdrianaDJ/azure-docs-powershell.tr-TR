---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: d9c036c7047ee0d568f5e1451bce46dfe2903e29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761503"
---
# Set-AzAutomationModule

## SYNOPSIS
Otomasyon 'da bir modülü güncelleştirir.

## INDEKI

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-AzAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda bir modülü güncelleştirir.
Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.
Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir: 
- . psm1 veya. dll dosya adı uzantısına sahip wps_2 modülü 
- . psd1 dosya adı uzantısına sahip wps_2 modül bildirimi,. zip dosyasının adı, klasörün adı ve klasörün adı aynı olmalıdır.
. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.
Bu cmdlet veya New-AzAutomationModule cmdlet 'ini kullanarak bir wps_2 modülünü Otomasyonu
Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.
Başarılı olup olmadığını denetlemek için, aşağıdaki komutu çalıştırarak: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName başarılı bir şekilde **provisioningstate** özelliğini denetleyin.

## ÖRNEKLERDEN

### Örnek 1: modül güncelleştirme
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Bu komut, Contoso17 adlı Otomasyon hesabına ContosoModule adlı var olan bir modülün güncelleştirilmiş sürümünü alır.  Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in modülü güncelleştirdiği Otomasyon hesabının adını belirtir.

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
Bu cmdlet 'in içeri aktardığından, modülün yeni sürümünü içeren. zip dosyasının URL 'sini belirtir.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Bu cmdlet 'in Otomasyonu güncelleştirdiği modülün sürümünü belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Bu cmdlet 'in modülü güncelleştirdiği kaynak grubunun adını belirtir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Uri

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Module

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Yeni-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


