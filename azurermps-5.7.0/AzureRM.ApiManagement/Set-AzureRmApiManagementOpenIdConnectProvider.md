---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594505"
---
# Set-AzureRmApiManagementOpenIdConnectProvider

## SYNOPSIS
OpenID Connect sağlayıcısını değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-Azurermapımanagementopenıdconnectprovider** cmdlet 'ı, Azure API Yönetimi 'Nde OpenID Connect sağlayıcısını değiştirir.

## ÖRNEKLERDEN

### Örnek 1: sağlayıcı için istemci gizliliğini değiştirme
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

Bu komut, KIMLIĞI OICProvicer01 olan sağlayıcıyı değiştirir.
Komut, sağlayıcı için bir istemci parolası belirtir.

## PARAMETRELERINE

### -Clitıd
Geliştirici konsolunun istemci KIMLIĞINI belirtir.

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

Required: False
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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Openıdconnectproviderıd
Bu cmdlet 'in değiştirdiği sağlayıcı için bir KIMLIK belirtir.
KIMLIK belirtmezseniz, bu cmdlet bir tane oluşturur.

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

### -Geçiş
Bu cmdlet 'in değiştirdiği **Psapsananagementopenıdconnectprovider** öğesini döndürmediğini belirtir.

```yaml
Type: SwitchParameter
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

[Yeni-Azurermapımanagementopenıdconnectprovider](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[Remove-Azurermapımanagementopenıdconnectprovider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


