---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595133"
---
# Export-AzureRmApiManagementApi

## SYNOPSIS
Bir dosyaya API 'YI dışarı aktarır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ExportToPipeline (varsayılan)
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ExportToFile
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Export-Azurermapımanagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.

## ÖRNEKLERDEN

### Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

Bu komut, bir WADL dosyasına API dışarı aktarır.

## PARAMETRELERINE

### -Apııd
Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.

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

### -Force
Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveAs
Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SpecificationFormat
API biçimini belirtir.
psdx_paramvalues Wadl ve Swagger.

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Dizisi
Bu cmdlet, dışarı aktarılan API içeriğini dize olarak döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermapımanagementapı](./Get-AzureRmApiManagementApi.md)

[Import-Azurermapımanagementapı](./Import-AzureRmApiManagementApi.md)

[Yeni-Azurermapımanagementapı](./New-AzureRmApiManagementApi.md)

[Remove-Azurermapımanagementapı](./Remove-AzureRmApiManagementApi.md)

[Set-Azurermapımanagementapı](./Set-AzureRmApiManagementApi.md)


