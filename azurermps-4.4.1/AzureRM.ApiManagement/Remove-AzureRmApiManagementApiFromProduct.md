---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587035"
---
# Remove-AzureRmApiManagementApiFromProduct

## SYNOPSIS
Bir üründen API 'YI kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermapımanagementapifromproduct** cmdlet 'i bir üründen Azure API yönetim API 'sini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: bir üründen API 'YI kaldırma
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

Bu işlem, belirtilen API 'YI üründen kaldırır.

## PARAMETRELERINE

### -Apııd
Üründen kaldırılacak API 'nin KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
**Psapsananabir Gementcontext** belirtir.

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

### -Geçiş
Bu cmdlet 'in başarılı olduğu bir $True değerini (veya $False) döndürmediğini belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ÜrünKimliği
API 'nin kaldırılacağı ürünün KIMLIĞINI belirtir.

```yaml
Type: System.String
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

### bool

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermapımanagementapitoproduct](./Add-AzureRmApiManagementApiToProduct.md)


