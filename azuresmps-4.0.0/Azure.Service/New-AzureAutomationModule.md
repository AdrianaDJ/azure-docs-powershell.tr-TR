---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106223"
---
# New-AzureAutomationModule

## SYNOPSIS

Bir modülü otomatikleştirme 'ye aktarır.

## INDEKI

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**New-AzureAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.
Modül, aşağıdaki dosya türlerinden birini içeren bir klasör içeren,. zip uzantılı sıkıştırılmış bir dosyadır:

- Windows PowerShell modülü (psm1 dosyası). 

- Windows PowerShell modülü bildirimi (psd1 dosyası). 

- Derleme (dll dosyası).

Zip dosyasının adları, ZIP dosyasındaki klasör ve klasördeki (. psm1, PSD. 1 veya. dll) dosya eşleşmelidir.

## ÖRNEKLERDEN

### Örnek 1: modül Içeri aktarma
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.
Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.

## PARAMETRELERINE

### -AutomationAccountName
Modülün saklanacağı Otomasyon hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLink
Web sitesi veya modül dosyasının yolunu belirten Azure Blob deposu gibi ortak URL.
Bu konuma publicolarak erişilebilir olması gerekir.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Modül için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Etiketler
Modülle ilgili bir veya daha fazla etiketi belirtir.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Module

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Set-AzureAutomationModule](./Set-AzureAutomationModule.md)


