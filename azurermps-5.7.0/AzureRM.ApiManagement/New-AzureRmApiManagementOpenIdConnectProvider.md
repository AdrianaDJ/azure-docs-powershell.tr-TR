---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586846"
---
# New-AzureRmApiManagementOpenIdConnectProvider

## SYNOPSIS
OpenID Connect sağlayıcısı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API yönetiminde bir OpenID Connect sağlayıcısı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: sağlayıcı oluşturma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

Bu komut contoso OpenID Connect Provider adlı bir OpenID Connect **sağlayıcısı** oluşturur

## PARAMETRELERINE

### -Clitıd
Geliştirici konsolunun istemci KIMLIĞINI belirtir.

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

### -ClientSecret
Geliştirici konsolunun istemci gizliliğini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Açıklama
Bir açıklama belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MetadataEndpointUri
Sağlayıcının meta veri uç noktası URI 'sini belirtir.

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

### -Ad
Sağlayıcı için kolay bir ad belirtir.

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

### -Openıdconnectproviderıd
Sağlayıcı için bir KIMLIK belirtir.
KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.

```yaml
Type: String
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. Apsananaen. ServiceManagement. modeller. Psapsananagementopenıdconnectprovider

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermapımanagementopenıdconnectprovider](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[Remove-Azurermapımanagementopenıdconnectprovider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[Set-Azurermapımanagementopenıdconnectprovider](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


