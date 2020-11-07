---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764494"
---
# New-AzureRmApiManagementApi

## SYNOPSIS
Bir API oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azurermapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'si oluşturur.

## ÖRNEKLERDEN

### Örnek 1: API oluşturma
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

Bu komut, belirtilen URL ile yankı adlı bir API oluşturur.

## PARAMETRELERINE

### -Apııd
Oluşturulacak API 'nin KIMLIĞINI belirtir.
Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir KIMLIK oluşturur.

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

### -AuthorizationScope
OAuth işlemleri kapsamını belirtir.
Varsayılan değer $Null.

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

### -Authorizationserverıd
OAuth yetkilendirme sunucusu KIMLIĞINI belirtir.
Varsayılan değer $Null.
*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.

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
Web API 'sinin açıklamasını belirtir.

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
Web API 'sinin adını belirtir.
Bu, API 'nin geliştirici ve yönetici portalında göründüğü şekliyle genel adıdır.

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

### -Yol
API 'nin Genel URL 'sinin son bölümü olan ve yönetici portalında Web API URL soneki alanına karşılık gelen Web API yolunu belirtir.
Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.
Varsayılan değer $Null.

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

### -ProductIds
Yeni API 'yi ekleyeceğiniz ürün kimlikleri dizisini belirtir.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protokoller
Web API protokolleri dizisini belirtir.
Geçerli değerler http, https 'dir.
Bu, API 'nin kullanılabileceği Web protokollerdir.
Varsayılan değer $Null.

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUrl
API 'yi sunan Web hizmetinin URL 'sini belirtir.
Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.
URL, 2000 karakter uzunluğunda olmalıdır.

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

### -SubscriptionKeyHeaderName
Abonelik anahtarı üst bilgi adını belirtir.
Varsayılan değer $Null.

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

### -SubscriptionKeyQueryParamName
Abonelik anahtarı sorgu dizesi parametre adını belirtir.
Varsayılan değer $Null.

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

### Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Dışarı aktarma-Azurermapımanagementapı](./Export-AzureRmApiManagementApi.md)

[Get-Azurermapımanagementapı](./Get-AzureRmApiManagementApi.md)

[Import-Azurermapımanagementapı](./Import-AzureRmApiManagementApi.md)

[Remove-Azurermapımanagementapı](./Remove-AzureRmApiManagementApi.md)

[Set-Azurermapımanagementapı](./Set-AzureRmApiManagementApi.md)


