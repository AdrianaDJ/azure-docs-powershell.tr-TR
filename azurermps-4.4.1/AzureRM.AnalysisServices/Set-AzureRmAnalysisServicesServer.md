---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587056"
---
# Set-AzureRmAnalysisServicesServer

## SYNOPSIS
Analysis Services sunucusu örneğini değiştirir

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Varsayılan (varsayılan)
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Yedeği devre dışı bırak
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Set-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini değiştirir

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

Anahtar olarak ayarlamak için resourcegroup testgroup içinde TestServer adlı sunucuyu değiştirir testuser1@contoso.com

## PARAMETRELERINE

### -Yönetici
Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.
Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupBlobContainerUri
Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si

```yaml
Type: System.String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableBackup
Yedek blob kapsayıcısını devre dışı bırakma anahtarı.
Yedek blob kapsayıcısını yeniden etkinleştirmek için lütfen yedek blob kapsayıcı URI 'sini-BackupBlobContainerUri olarak sağlayın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Analysis Services sunucusunun adı

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

### -Geçiş
İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür

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

### -ResourceGroupName
Sunucunun ait olduğu Azure Kaynak grubunun adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Sunucunun SKU adı.
Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Management. Analysis. modeller. AnalysisServicesServer

## NOTLARıNDA
Diğer ad: Set-AzureAs

## ILGILI BAĞLANTıLAR

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[Remove-AzureRmAnalysisServicesServer](./Remove-AzureRmAnalysisServicesServer.md)
