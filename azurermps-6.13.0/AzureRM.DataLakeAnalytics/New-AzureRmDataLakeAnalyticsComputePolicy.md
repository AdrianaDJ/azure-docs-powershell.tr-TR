---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 679c02edde85b9f64eb037d6d30be1e7c36cdeb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593260"
---
# New-AzureRmDataLakeAnalyticsComputePolicy

## SYNOPSIS
Belirli bir AAD varlığı için bir Data Lake Analytics COMPUTE ilke kuralı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmDataLakeAnalyticsComputePolicy** , Azure Data Lake Analytics hesabındaki belırlı bir AAD varlığı için belirtilen işlem ilkesi kuralını oluşturur.

## ÖRNEKLERDEN

### Örnek 1: tek bir kuralla bir işlem ilkesi oluşturma
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur

### Örnek 2: her iki kuralın de ayarlandığı bir işlem ilkesi oluşturma
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

Bu komut, "83cb7ad2-3523-4b82-b909-dp478b0t8aea3 100" kimliğine sahip kullanıcı için "contosoadla" hesabında "" adlı bir ilke oluşturur

## PARAMETRELERINE

### -Hesap
İşlem ilkesinin ekleneceği hesabın adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Maxanalyzer Ticsunesperjob
Bu ilke için iş başına desteklenen en yüksek analitik birim.
Bu, Minpriorityi veya her iki parametre de belirtilmelidir.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Minpriorityi
Bu ilke için iş başına desteklenen en düşük öncelik.
Bu, Maxanalyzer Ticsunesperjob veya her iki parametre de belirtilmelidir.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Oluşturulacak işlem ilkesinin adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
İlkenin uygulanacağı Kullanıcı veya grubun Azure Active Directory nesne kimliği.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NesneTürü
İçeri aktarılan nesne KIMLIĞI için Azure Active Directory nesne türü.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Hesabınızın bulunduğu kaynak grubunun adı.
İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Guid

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## ÇıKıŞLAR

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
