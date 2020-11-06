---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593862"
---
# Get-AzureRmApiManagementSubscription

## SYNOPSIS
Abonelikleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm abonelikleri al (varsayılan)
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Alt simge alma KIMLIĞI
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Kullanıcı KIMLIĞINE göre al
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Ürün KIMLIĞINE göre al
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.

## ÖRNEKLERDEN

### Örnek 1: tüm abonelikleri al
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

Bu komut tüm abonelikleri alır.

### Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

Bu komut, KIMLIĞI bir abonelik alır.

### Örnek 3: kullanıcıya yönelik tüm abonelikleri alma
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

Bu komut kullanıcının aboneliklerini alır.

### Örnek 4: bir ürüne yönelik tüm abonelikleri alma
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

Bu komut, ürünün tüm aboneliklerini alır.

## PARAMETRELERINE

### -Context
**Psapsananagementcontext** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ÜrünKimliği
Ürün tanımlayıcısını belirtir.
Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionID
Abonelik tanımlayıcısını belirtir.
Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserID
Kullanıcı tanımlayıcısını belirtir.
Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
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

### IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapımanagementsubscription](./New-AzureRmApiManagementSubscription.md)

[Remove-Azurermapımanagementsubscription](./Remove-AzureRmApiManagementSubscription.md)

[Set-Azurermapımanagementsubscription](./Set-AzureRmApiManagementSubscription.md)


