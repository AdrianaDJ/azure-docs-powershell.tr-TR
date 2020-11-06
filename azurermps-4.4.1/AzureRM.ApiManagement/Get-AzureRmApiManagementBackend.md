---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591844"
---
# Get-AzureRmApiManagementBackend

## SYNOPSIS
Arka ucun ayrıntılarını edinin.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm backenleri al (varsayılan)
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Arka uç KIMLIĞIYLE al
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Arka ucun ayrıntılarını edinin.

## ÖRNEKLERDEN

### --------------------------Örnek 1--------------------------
@ {paragraf = PS C: \\ \> }







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

Api Yönetim hizmetinde yapılandırılmış tüm Backen'ler listesini alır.

### --------------------------Örnek 2--------------------------
@ {paragraf = PS C: \\ \> }







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

Belirtilen arka ucun ayrıntılarını ' 123 ' tanımlayıcısıyla

## PARAMETRELERINE

### -Backenmuydunuz
Arka ucun tanıtıcısı.
Belirtilirse, tanımlayıcı tarafından arka uç bulmayı dener.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Psapsananagementcontext örneği.
Bu parametre gereklidir.

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

### IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementarka uç>

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgünlükçü. Psapimanagementarka uç

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapsananaarka uç](./New-AzureRmApiManagementBackend.md)

[Yeni-Azurermapımanagementbackendcredential](./New-AzureRmApiManagementBackendCredential.md)

[Yeni-Azurermapımanagementbackendproxy](./New-AzureRmApiManagementBackendProxy.md)

[Set-Azurermapımanaarka uç](./Set-AzureRmApiManagementBackend.md)

[Remove-Azurermapsananaarka uç](./Remove-AzureRmApiManagementBackend.md)
