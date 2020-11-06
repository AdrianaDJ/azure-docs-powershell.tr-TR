---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594480"
---
# Add-AzureRmAutoscaleSetting

## SYNOPSIS
Otomatik ölçeklendirme ayarı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### UpdateAutoscaleSetting
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateAutoscaleSetting
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarı oluşturur.

Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.

## ÖRNEKLERDEN

### Örnek 1: otomatik ölçeklendirme ayarı oluşturma
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

İlk iki komut New-AzureRmAutoscaleRule kullanarak iki otomatik ölçeklendirme kuralı, $Rule 1 ve $Rule 2 oluşturur.

Üçüncü ve dördüncü komutlarda, $Rule 1 ve $Rule 2 kullanarak otomatik ölçeklendirme profilleri, $Profile 1 ve $Profile 2 kullanarak New-AzureRmAutoscaleProfile kullanılır.

Son komutu $Profile 1 ve $Profile 2 ' deki profilleri kullanarak otomatik ölçeklendirme ayarı oluşturur.

## PARAMETRELERINE

### -AutoscaleProfile
Otomatik ölçeklendirme ayarına eklenecek profillerin listesini belirtir veya profil eklemek için $Null.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DisableSetting
Varolan bir otomatik ölçeklendirme ayarını devre dışı bırakır.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Otomatik ölçeklendirme ayarının konumunu belirtir.

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Oluşturulacak otomatik ölçeklendirme ayarının adını belirtir.

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bildirim
Virgülle ayrılmış bildirimlerin listesini belirtir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Otomatik ölçeklendirme ayarıyla ilişkili kaynak için kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SettingSpec
Bir **Otomatik ölçek ayarı** nesnesi belirtir.
**Otomatik ölçek ayarı** nesnesi almak için Get-AzureRmAutoscaleSetting cmdlet 'ini kullanabilir veya Windows PowerShell betiği içinde bir tane oluşturabilirsiniz.

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Targetresourceıd
Otomatik ölçeklendirme için kaynağın KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAutoscaleSetting](./Get-AzureRmAutoscaleSetting.md)

[Yeni-AzureRmAutoscaleProfile](./New-AzureRmAutoscaleProfile.md)

[Yeni-AzureRmAutoscaleRule](./New-AzureRmAutoscaleRule.md)

[Remove-AzureRmAutoscaleSetting](./Remove-AzureRmAutoscaleSetting.md)


