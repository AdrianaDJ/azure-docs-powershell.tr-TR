---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587048"
---
# Get-AzureRmApiManagement

## SYNOPSIS
Bir listeyi veya belirli bir API yönetim hizmeti açıklamasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm abonelikte (varsayılan)
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Tümü kaynak grubunda
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Belirli API Yönetimi hizmeti
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azurermapsananaks** cmdlet 'i, aboneliğin veya BELIRTILEN bir API yönetiminin altındakı tüm API yönetim hizmetlerinin listesini alır.

## ÖRNEKLERDEN

### Örnek 1: tüm API yönetim hizmetlerini alma
```
PS C:\>Get-AzureRmApiManagement
```

Bu komut, bir aboneliğin içindeki tüm API yönetim hizmetlerini alır.

### Örnek 2: belirli bir ad ile tüm API yönetim hizmetlerini alma
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

Bu komut tüm API yönetim hizmetlerini adıyla alır.

## PARAMETRELERINE

### -Ad
API yönetim hizmetinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in API Yönetim hizmetini aldığı kaynak grubun adını belirtir.

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. Koleksiyonlar. Generic. List ' 1 [Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yedek-azurermapı](./Backup-AzureRmApiManagement.md)

[Yeni-azurermapı](./New-AzureRmApiManagement.md)

[Remove-azurermapsanana](./Remove-AzureRmApiManagement.md)

[Geri yükleme-azurermapı](./Restore-AzureRmApiManagement.md)


