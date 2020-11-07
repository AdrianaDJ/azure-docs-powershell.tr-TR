---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763334"
---
# Get-AzureRmProviderOperation

## SYNOPSIS
Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzureRmProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.
İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.
Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (*) karakteri ((*) karakteri) olarak alır.

Tüm Azure Resource providers için tüm işlemleri almak için Get-AzureRmProviderOperation * kullanın.

Microsoft 'un tüm işlemlerini almak için Microsoft. COMPUTE/* Get-AzureRmProviderOperation kullanın. kaynak sağlayıcısını hesaplama.

## ÖRNEKLERDEN

### Tüm sağlayıcılar için tüm eylemleri----------------------------------------------------
```
PS C:\> Get-AzureRmProviderOperation *
```

### Belirli bir kaynak sağlayıcısı için eylemleri----------------------------------------------------
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### Sanal makinelerde gerçekleştirilebilen tüm eylemlerin----------------------------------------------------
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## PARAMETRELERINE

### -OperationSearchString
İşlem arama dizesi (olası joker karakter (*) ile)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Dizisi
' OperationSearchString ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

