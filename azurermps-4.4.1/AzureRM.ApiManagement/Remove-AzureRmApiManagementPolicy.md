---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587031"
---
# Remove-AzureRmApiManagementPolicy

## SYNOPSIS
Belirtilen kapsamdan API yönetim ilkesini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Kiracı düzeyi (varsayılan)
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Ürün düzeyi
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### API düzeyi
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### İşlem düzeyi
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermapsananagementpolicy** cmdlet 'i, BELIRTILEN kapsamdan API yönetim ilkesini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: kiracı düzeyi ilkesini kaldırma
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

Bu komut, kiracı düzeyi ilkesini API yönetiminden kaldırır.

### Örnek 2: ürün kapsamı ilkesini kaldırma
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

Bu komut, API yönetiminden ürün kapsam ilkesini kaldırır.

### Örnek 3: API kapsam ilkesini kaldırma
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

Bu komut API Yönetimi 'nden API kapsam ilkesini kaldırır.

### Örnek 4: işlem kapsamı ilkesini kaldırma
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

Bu komut, işlem kapsam ilkesini API yönetiminden kaldırır.

## PARAMETRELERINE

### -Apııd
Var olan bir API 'ın tanımlayıcısını belirtir.
Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini kaldırır.

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
**Psapimanagementcontext** nesnesinin örneğini belirtir.

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

### -OperationId
Var olan bir işlemin tanımlayıcısını belirtir.
Bu parametreyi *Apııd* parametresiyle belirtirseniz, bu cmdlet işlem kapsamı ilkesini kaldırır.

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.

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
Var olan ürünün tanımlayıcısını belirtir.
Bu parametreyi belirtirseniz, cmdlet ürün kapsam ilkesini kaldırır.

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

### Boole

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermapımanagementpolicy](./Get-AzureRmApiManagementPolicy.md)

[Set-Azurermapımanagementpolicy](./Set-AzureRmApiManagementPolicy.md)


