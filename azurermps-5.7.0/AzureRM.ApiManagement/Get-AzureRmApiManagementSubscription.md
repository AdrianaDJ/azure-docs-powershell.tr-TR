---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586848"
---
# Get-AzureRmApiManagementSubscription

## SYNOPSIS
Abonelikleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Getallabonelikleri (varsayılan)
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbysubscriptionıd
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyuserıd
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyproductıd
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.

## ÖRNEKLERDEN

### Örnek 1: tüm abonelikleri al
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

Bu komut tüm abonelikleri alır.

### Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

Bu komut, KIMLIĞI bir abonelik alır.

### Örnek 3: kullanıcıya yönelik tüm abonelikleri alma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

Bu komut kullanıcının aboneliklerini alır.

### Örnek 4: bir ürüne yönelik tüm abonelikleri alma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

Bu komut, ürünün tüm aboneliklerini alır.

## PARAMETRELERINE

### -Context
**Psapsananagementcontext** nesnesini belirtir.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ÜrünKimliği
Ürün tanımlayıcısını belirtir.
Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.

```yaml
Type: String
Parameter Sets: GetByProductId
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
Type: String
Parameter Sets: GetBySubscriptionId
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
Type: String
Parameter Sets: GetByUserId
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

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription
API yönetim hizmetindeki aboneliğin ayrıntıları.

### IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription>
API yönetim hizmetindeki abonelik listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapımanagementsubscription](./New-AzureRmApiManagementSubscription.md)

[Remove-Azurermapımanagementsubscription](./Remove-AzureRmApiManagementSubscription.md)

[Set-Azurermapımanagementsubscription](./Set-AzureRmApiManagementSubscription.md)


