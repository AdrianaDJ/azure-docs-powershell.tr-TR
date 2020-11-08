---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108019"
---
# Get-AzApiManagementNamedValue

## SYNOPSIS
Bir listeyi veya belirli bir adlandırılmış değeri alır.

## INDEKI

### GetAllNamedValues (varsayılan)
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getbynamedvalueıd
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByTag
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azapsananagementnamedvalue** cmdlet 'i, bir liste veya belirli bir adlandırılmış değeri alır.
Değer parola olarak işaretlenmişse, değer, sonuç ayrıntılarına dahil olmaz. Gizli değer almak için **Get-Azapsananagementnamedvaluesecretvalue** seçeneğini kullanın.

## ÖRNEKLERDEN

### Örnek 1: ada göre adlandırılmış değeri alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

Bu komut, adlandırılmış değer adı verilen değer ayrıntılarını alır.

## PARAMETRELERINE

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

### -Ad
Dize adını içeren adlara sahip adlandırılmış değerleri bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Namedvalueıd
Adlandırılmış değerin tanıtıcısı.
Belirtilmişse tanımlayıcı tarafından adlandırılmış değer bulmayı dener.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Etiketle ilişkilendirilmiş adlandırılmış değerleri bulur.
Belirtilmişse bir etiketle ilişkilendirilmiş tüm özellikleri döndürür.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementnamedvalue

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
