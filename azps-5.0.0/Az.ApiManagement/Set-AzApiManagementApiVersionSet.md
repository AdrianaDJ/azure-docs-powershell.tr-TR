---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323446"
---
# Set-AzApiManagementApiVersionSet

## SYNOPSIS
API yönetim bağlamında ayarlanan bir API sürümünü güncelleştirir.

## INDEKI

### ExpandedParameter (varsayılan)
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByInputObject
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım

**Set-Azapsananagementapiversionset** cmdlet 'ı Azure API yönetim API sürümü kümesini değiştirir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

Bu komut, sürüm oluşturma düzeni `Header` ve üst bilgi parametresiyle var olan BIR API sürüm kümesini güncelleştirir `api-version` .

## PARAMETRELERINE

### -Apıversionsetid
Yeni API sürüm kümesi için tanımlayıcı.

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
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
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Açıklama
API sürüm kümesinin açıklaması.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HeaderName
Sürüm bilgilerini içerecek üst bilgi değeri.
Sürüm oluşturma düzeni üst BILGISI seçilirse, bu değer belirtilmelidir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Psapimanagementapıversionset 'in örneği. Bu parametre gereklidir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Apıversion kümesi adı.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Bu örnekte, değiştirilmiş Apıversionset 'i temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. modellerinin

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SorguAdı
Sürüm bilgilerini içerecek olan sorgu değeri.
Sürüm oluşturma düzeni sorgusu seçilirse, bu değer belirtilmelidir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Düzen
API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.
Bu parametre isteğe bağlıdır.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset

### System. String

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azapsananagementapıversionset](./Get-AzApiManagementApiVersionSet.md)

[New-Azapsananagementapıversionset](./New-AzApiManagementApiVersionSet.md)

[Set-Azapsananagementapiversionset](./Set-AzApiManagementApiVersionSet.md)
