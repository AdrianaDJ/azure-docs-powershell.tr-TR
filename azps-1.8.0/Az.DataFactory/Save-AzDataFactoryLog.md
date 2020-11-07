---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 19d2c5c9b03b08bd31839dfe7e072de9517ff459
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917043"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Azure HDInsight işlemeden günlük dosyalarını indirir.

## INDEKI

### ByFactoryName (varsayılan)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Save-AzDataFactoryLog** cmdlet 'ı, domuz veya Hive projelerinin Azure HDInsight işlemeyle ilişkili günlük dosyalarını veya özel etkinlikleri yerel sabit sürücünüze indirir.
İlk olarak, bir veri dilimi için bir etkinliğin KIMLIĞINI almak üzere Get-AzDataFactoryRun cmdlet 'i çalıştırırsınız ve ardından bu KIMLIĞI kullanarak, HDInsight kümesiyle ilişkili ikili büyük nesne (BLOB) depolama alanından günlük dosyalarını alırsınız.
*Downloadlogs* parametresini belirtmezseniz, cmdlet yalnızca günlük dosyalarının konumunu döndürür.
Bir çıkış dizini ( *Çıkış* parametresi) belirtmeden *downloadlogs* belirtirseniz, günlük dosyaları varsayılan belgeler klasörüne indirilir.
Bir çıkış klasörüyle ( *Çıkış* ) birlikte *downloadlogs günlükleri* belirtirseniz, günlük dosyaları belirtilen klasöre indirilir.

## ÖRNEKLERDEN

### Örnek 1: günlük dosyalarını belirli bir klasöre kaydetme
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Bu komut, etkinliğin günlük dosyalarını, etkinliğin, ADF adlı kaynak grubundaki Logprocessingname adlı Data Factory adındaki bir ardışık düzene ait 841b77c9-d56c-48D1-99a3-8c16c3e77d39 KIMLIĞIYLE çalışır.
Günlük dosyaları C:\Test klasörüne kaydedilir.

### Örnek 2: günlük dosyalarını varsayılan belgeler klasörüne kaydetme
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Bu komut günlük dosyalarını Belgeler klasörüne kaydeder (varsayılan).

### Örnek 3: günlük dosyalarının konumunu alma
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Bu komut, günlük dosyalarının konumunu döndürür.
*Downloadlogs* 'un belirtilmemiştir.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Veri Fabrikası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veri fabrikası için günlük dosyalarını indirir.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
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

### -DownloadLogs
Bu cmdlet 'in günlük dosyalarını yerel bilgisayarınıza indirdiğini belirtir.
*Ouptut* klasörü belirtilmezse, dosyalar alt klasörün altındaki Belgeler klasörüne kaydedilir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Veri dilimi için etkinliğin çalışma KIMLIĞINI belirtir.
KIMLIK almak için Get-AzDataFactoryRun cmdlet 'ini kullanın.

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

### -Çıktı
İndirilen günlük dosyalarının kaydedildiği çıkış klasörünü belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataFactory. modeller. Psrunlogınfo

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-Azverfactorypya](./Get-AzDataFactoryPipeline.md)

[Yeni-Azveri Factorypya](./New-AzDataFactoryPipeline.md)

[Remove-Azdatafactorypda](./Remove-AzDataFactoryPipeline.md)

[Set-Azdatafactorypipelineactivedönem](./Set-AzDataFactoryPipelineActivePeriod.md)

[Askıya al-Azverfactorypya](./Suspend-AzDataFactoryPipeline.md)


