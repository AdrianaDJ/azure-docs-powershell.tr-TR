---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587086"
---
# Get-AzureRmWebAppBackupList

## SYNOPSIS

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### FromResourceName
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmWebAppBackupList** cmdlet 'ı bir Azure Web App yedeklemelerinin listesini alır.

## ÖRNEKLERDEN

### 2
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

Bu komut, WebApp kaynak grubuyla ilişkilendirilmiş WebApp WebAppStandard ile ilgili bir yedekleme listesi döndürür.

## PARAMETRELERINE

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

### -Ad
WebApp adı

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Yuva adı

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
Piped WebApp

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Management. Web sitesi. modeller. site
Parametreler: WebApp (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
