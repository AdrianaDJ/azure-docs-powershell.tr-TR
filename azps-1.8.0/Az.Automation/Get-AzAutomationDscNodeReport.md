---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: a8d0244b9a26616e796a4e867a193da4ed3888d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761622"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
DSC düğümünden otomatikleştirme 'ye gönderilen raporları alır.

## INDEKI

### Tümü (varsayılan)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### En son
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Byıd
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzAutomationDscNodeReport** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) düğümünden Azure Otomasyonu 'na gönderilen raporları alır.

## ÖRNEKLERDEN

### Örnek 1: DSC düğümü için tüm raporları alma
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.
İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen tüm raporlarda meta verileri alır.
Komut, düğümü $Node nesnesinin **ID** özelliğini kullanarak belirtir.

### Örnek 2: rapor KIMLIĞIYLE bir DSC düğümü için rapor alma
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.
İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen belirtilen KIMLIğIN meta verilerini alır.

### Örnek 3: DSC düğümü için en son raporu alma
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.
İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen en son raporun meta verilerini alır.

## PARAMETRELERINE

### -AutomationAccountName
Otomasyon hesabının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği hesaba ait bir DSC düğümünün raporlarını dışarı aktarır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Bitişsaati
Bitiş saati belirtir.
Bu cmdlet, bu tarihten önce Otomasyon tarafından alınan raporları alır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Bu cmdlet 'in alınacağı DSC düğümü raporunun benzersiz KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -En son
Bu cmdlet 'in yalnızca belirtilen düğüm için en son DSC raporunu aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
Bu cmdlet 'in raporları aldığı DSC düğümünün benzersiz KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in raporları aldığı DSC düğümünü içeren bir kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Başlangıçsaati
Başlangıç zamanını belirtir.
Bu cmdlet, bu süreden sonra Otomasyon tarafından alınan raporları alır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
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

### System. Guid

### System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. DscNode

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Dışarı aktarma-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


