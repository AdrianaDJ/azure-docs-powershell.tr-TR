---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936437"
---
# Get-AzProviderOperation

## SYNOPSIS
Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.

## INDEKI

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.
İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.
Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (joker karakter () içeren) olarak alır *. Tüm Azure Resource providers için tüm işlemleri almak için Get-AzProviderOperation * kullanın. Microsoft. COMPUTE/' Get-AzProviderOperation kullanarak* Microsoft 'un tüm işlemlerini alın. kaynak sağlayıcısını hesaplama.

## ÖRNEKLERDEN

### Tüm sağlayıcılar için tüm eylemleri alma
```
PS C:\> Get-AzProviderOperation *
```

### Belirli bir kaynak sağlayıcısının eylemlerini alma
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Sanal makinelerde gerçekleştirilebilen tüm eylemleri alma
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
İşlem arama dizesi (olası joker karakter (*) ile)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String
Parametreler: Işlemkimliği (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation

## NOTLARıNDA
Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR
