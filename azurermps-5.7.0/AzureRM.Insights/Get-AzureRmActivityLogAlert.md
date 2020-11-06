---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594474"
---
# Get-AzureRmActivityLogAlert

## SYNOPSIS
Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Getbynaik Vseçresourcegroup
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmActivityLogAlert** cmdlet 'i, bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.

## ÖRNEKLERDEN

### Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma
```
PS C:\>Get-AzureRmActivityLogAlert
```

Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.

### Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.

### Örnek 3: etkinlik günlüğü uyarısı alın.
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Ad
Etkinlik günlüğü uyarısının adı.

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Uyarı kaynağının bulunduğu kaynak grubunun adı.
Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
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

## ÇıKıŞLAR

### <System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]

### Yabilirsiniz

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Güncelleştirme-AzureRmActivityLogAlert](./Update-AzureRmActivityLogAlert.md)

[Remove-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[Yeni-AzureRmActionGroup](./New-AzureRmActionGroup.md)

[Yeni-AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)
