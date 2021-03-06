---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765113"
---
# Get-AzureRmAutomationDscNodeReport

## SYNOPSIS
DSC düğümünden otomatikleştirme 'ye gönderilen raporları alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tümü (varsayılan)
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### En son
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Byıd
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmAutomationDscNodeReport** cmdlet 'ı, APS Istenen durum YAPıLANDıRMASı (DSC) düğümünden Azure Otomasyonu 'na gönderilen raporları alır.

## ÖRNEKLERDEN

### Örnek 1: DSC düğümü için tüm raporları alma
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.

İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen tüm raporlarda meta verileri alır.
Komut, düğümü $Node nesnesinin **ID** özelliğini kullanarak belirtir.

### Örnek 2: rapor KIMLIĞIYLE bir DSC düğümü için rapor alma
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.

İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen belirtilen KIMLIğIN meta verilerini alır.

### Örnek 3: DSC düğümü için en son raporu alma
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.
Komut bu nesneyi $Node değişkeninde depolar.

İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen en son raporun meta verilerini alır.

## PARAMETRELERINE

### -AutomationAccountName
Otomasyon hesabının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği hesaba ait bir DSC düğümünün raporlarını dışarı aktarır.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: DateTimeOffset
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
Type: Guid
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
Type: SwitchParameter
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
Type: Guid
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
Type: String
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
Type: DateTimeOffset
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. DscNode

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Dışarı aktarma-AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)


