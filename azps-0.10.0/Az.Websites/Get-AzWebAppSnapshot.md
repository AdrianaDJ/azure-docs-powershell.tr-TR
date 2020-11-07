---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936107"
---
# Get-AzWebAppSnapshot

## SYNOPSIS
Web uygulaması için sağlanan anlık görüntüleri alır.

## INDEKI

### FromResourceName
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### FromWebApp
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## Tanım
**Get-AzWebAppSnapshot** cmdlet 'i, bir Web uygulamasının tüm anlık görüntülerini döndürür. Anlık görüntüler, Web uygulamasının dosyalarının ve ayarlarının otomatik yedeğine sahiptir. **Restore-AzWebAppSnapshot** cmdlet 'i ile anlık görüntü geri yüklenebilir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

"Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip "ConstosoApp" adlı bir Web uygulamasının anlık görüntülerini alma

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Web uygulamasının adı.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Web uygulaması yuvasının adı.

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
Web App nesnesi

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### System. String
Microsoft. Azure. Management. Web sitesi. modeller. site


## ÇıKıŞLAR

### Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

