---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587043"
---
# Get-AzureRmApiManagementOpenIdConnectProvider

## SYNOPSIS
OpenID Connect sağlayıcılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm OpenID Connect sağlayıcılarını alma (varsayılan)
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### OpenID Connect sağlayıcı KIMLIĞIYLE al
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### OpenID ile bul sağlayıcı kolay adı
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı Azure API yönetiminde OpenID Connect sağlayıcılarını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm sağlayıcıları al
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

Bu komut, belirtilen bağlam için tüm OpenID bağlama sağlayıcılarını alır.

### Örnek 2: KIMLIK kullanarak sağlayıcı alma
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı alır.

### Örnek 3: ad kullanarak sağlayıcı alma
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

Bu komut contoso OpenID Connect Provider adlı sağlayıcıyı alır.

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

### -Ad
Sağlayıcının kolay adını belirtir.
Bir ad belirtirseniz, bu cmdlet bu sağlayıcıyı alır.

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Openıdconnectproviderıd
Bu cmdlet 'in kaldırdığı sağlayıcının KIMLIĞINI belirtir.
Bir KIMLIK belirtirseniz, bu cmdlet bu sağlayıcıyı alır.

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
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

### IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapımanagementopenıdconnectprovider](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[Remove-Azurermapımanagementopenıdconnectprovider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[Set-Azurermapımanagementopenıdconnectprovider](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


