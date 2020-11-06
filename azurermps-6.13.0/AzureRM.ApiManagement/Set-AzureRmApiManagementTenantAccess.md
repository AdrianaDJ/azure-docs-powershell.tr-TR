---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c8f05c7ca9ddeb5868d62633600d63f5d7f01be0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587325"
---
# Set-AzureRmApiManagementTenantAccess

## SYNOPSIS
Kiracı erişimini etkinleştirilir veya devre dışı bırakır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmApiManagementTenantAccess** cmdlet 'i kiracı erişimini devre dışı bırakır veya devre dışı bırakır.

## ÖRNEKLERDEN

### Örnek 1: kiracı erişimini etkinleştirme
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

Bu komut, belirtilen bağlamda kiracı erişimini etkinleştirmiştir.

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

### Özellikli
Bu cmdlet 'in kiracı erişimini etkinleştirip etkinleştirmeyeceğini belirtir.
Etkinleştirmek $False veya devre dışı bırakmak için $True değeri belirtin.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in değiştirdiği **Psapsananagementaccessınformation** olduğunu gösterir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmApiManagementTenantAccess](./Get-AzureRmApiManagementTenantAccess.md)


