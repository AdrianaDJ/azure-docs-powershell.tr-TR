---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 42ef63d9884cef45b107b9c959b264402e4347d1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935753"
---
# Get-AzActivityLogAlert

## SYNOPSIS
Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.

## INDEKI

### Getbynaik Vseçresourcegroup
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azactivilogalert** cmdlet 'i bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.

## ÖRNEKLERDEN

### Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma
```
PS C:\>Get-AzActivityLogAlert
```

Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.

### Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.

### Örnek 3: etkinlik günlüğü uyarısı alın.
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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
Etkinlik günlüğü uyarısının adı.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Uyarı kaynağının bulunduğu kaynak grubunun adı.
Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-Azactivilogalert](./Set-AzActivityLogAlert.md)

[Update-AzActivityLogAlert](./Update-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[Yeni-AzActionGroup](./New-AzActionGroup.md)

[Yeni-Azactivilogalertcondition](./Get-AzActivityLogAlertCondition.md)
