---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 696e2de560b67db78f24dea7e8512d85c3640902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587586"
---
# Save-AzureRmDataFactoryLog

## SYNOPSIS
Azure HDInsight işlemeden günlük dosyalarını indirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByFactoryName (varsayılan)
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Save-AzureRmDataFactoryLog** cmdlet 'ı, domuz veya kovan projelerinin Azure HDInsight işlemeyle ilişkili günlük dosyalarını veya özel etkinlikleri yerel sabit sürücünüze indirir.
İlk olarak, bir veri dilimi için bir etkinliğin KIMLIĞINI almak üzere Get-AzureRmDataFactoryRun cmdlet 'i çalıştırırsınız ve ardından bu KIMLIĞI kullanarak, HDInsight kümesiyle ilişkili ikili büyük nesne (BLOB) depolama alanından günlük dosyalarını alırsınız.

*Downloadlogs* parametresini belirtmezseniz, cmdlet yalnızca günlük dosyalarının konumunu döndürür.

Bir çıkış dizini ( *Çıkış* parametresi) belirtmeden *downloadlogs* belirtirseniz, günlük dosyaları varsayılan belgeler klasörüne indirilir.

Bir çıkış klasörüyle ( *Çıkış* ) birlikte *downloadlogs günlükleri* belirtirseniz, günlük dosyaları belirtilen klasöre indirilir.

## ÖRNEKLERDEN

### Örnek 1: günlük dosyalarını belirli bir klasöre kaydetme
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Bu komut, etkinliğin günlük dosyalarını, etkinliğin, ADF adlı kaynak grubundaki Logprocessingname adlı Data Factory adındaki bir ardışık düzene ait 841b77c9-d56c-48D1-99a3-8c16c3e77d39 KIMLIĞIYLE çalışır.
Günlük dosyaları C:\Test klasörüne kaydedilir.

### Örnek 2: günlük dosyalarını varsayılan belgeler klasörüne kaydetme
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Bu komut günlük dosyalarını Belgeler klasörüne kaydeder (varsayılan).

### Örnek 3: günlük dosyalarının konumunu alma
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Bu komut, günlük dosyalarının konumunu döndürür.
*Downloadlogs* 'un belirtilmemiştir.

## PARAMETRELERINE

### -DataFactory
**Psdatafactory** nesnesini belirtir.

```yaml
Type: PSDataFactory
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
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: SwitchParameter
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
KIMLIK almak için Get-AzureRmDataFactoryRun cmdlet 'ini kullanın.

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

### -Çıktı
İndirilen günlük dosyalarının kaydedildiği çıkış klasörünü belirtir.

```yaml
Type: String
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
Type: String
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataFactory. modeller. Psrunlogınfo

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar

## ILGILI BAĞLANTıLAR

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Get-Azurermdatafactorypda](./Get-AzureRmDataFactoryPipeline.md)

[Yeni-Azurermdatafactorypeline](./New-AzureRmDataFactoryPipeline.md)

[Remove-Azurermdatafactorypda](./Remove-AzureRmDataFactoryPipeline.md)

[Set-Azurermdatafactoryptam](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Askıya al-Azurermdatafactorypla](./Suspend-AzureRmDataFactoryPipeline.md)


