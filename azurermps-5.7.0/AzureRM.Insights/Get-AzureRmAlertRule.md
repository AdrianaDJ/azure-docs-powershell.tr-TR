---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586694"
---
# Get-AzureRmAlertRule

## SYNOPSIS
Uyarı kurallarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### GetByResourceGroup
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceUri
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAlertRule** cmdlet 'i, adı veya URI 'sini ya da belirtilen bir kaynak grubundaki tüm uyarı kurallarını alır.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubu için uyarı kurallarını alma
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

Bu komut, Default-Web-merkezileştirme adlı kaynak grubu için tüm uyarı kurallarını alır.
*DetailedOutput* parametresi belirtilmediğinden, çıktı kurallarla ilgili ayrıntıları içermez.

### Örnek 2: ada göre bir uyarı kuralı alma
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.
*DetailedOutput* parametresi belirtilmediğinden, çıkış yalnızca uyarı kuralıyla ilgili temel bilgileri içerir.

### Örnek 3: ayrıntılı çıktıya sahip bir uyarı kuralı adı alın
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.
*DetailedOutput* parametresi belirtilmiştir, böylece çıktı ayrıntılıdır.

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

### -DetailedOutput
Çıktıda tüm ayrıntıları görüntüler.

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

### -Ad
Alınacak uyarı kuralının adını belirtir.

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.

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

### -Targetresourceıd
Hedef kaynağın KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: GetByResourceUri
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

### Liste<Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[Remove-AzureRmAlertRule](./Remove-AzureRmAlertRule.md)


