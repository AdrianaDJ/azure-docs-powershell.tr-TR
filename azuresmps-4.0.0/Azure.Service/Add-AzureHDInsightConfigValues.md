---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105728"
---
# Add-AzureHDInsightConfigValues

## SYNOPSIS
HDInsight küme yapılandırmasına bir Hadoop yapılandırma değeri özelleştirmesi veya kovan Paylaşılan kitaplık özelleştirmesi ekler.

## INDEKI

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.
Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.
Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.

Küme oluştururken yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için, [Azure PowerShell kullanarak HDInsight 'Ta Linux tabanlı kümeler oluşturma](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)konusuna bakın.
Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, [HDInsight 'de Hadoop Işlerini gönderme](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)konusuna bakın.
Azure PowerShell HDInsight hakkında başvuru bilgileri için [bkz.](https://msdn.microsoft.com/en-us/library/mt438705.aspx)

**Add-AzureHDInsightConfigValues** cmdlet 'i, Core-site.xml veya Hive-site.xml gibi bir Hadoop yapılandırma değeri özelleştirmesi veya bir Azure HDInsight küme yapılandırmasına yığın Paylaşılan kitaplık özelleştirmesi ekler.

Cmdlet, belirtilen yapılandırma nesnesine özel yapılandırma değerleri ekler.
Özel ayarlar, küme dağıtıldığında ilgili Hadoop hizmetlerinin yapılandırma dosyalarına eklenir.

## ÖRNEKLERDEN

### Örnek 1: kümeyi yapılandırma
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

İlk komut yeni bir **AzureHDInsightHiveConfiguration** nesnesi oluşturur ve $HiveConfigValues değişkeninde depolar.

Sonraki beş komut, kovan için yapılandırma değerleri oluşturur ve bu değerleri $HiveConfigValues üyeleri olarak depolar.

Yedinci komutu bir **AzureHDInsightOozieConfiguration** nesnesi oluşturur ve $OozieConfigValues değişkeninde depolar.
Sekizinci komutu Oozie için bir yapılandırma değeri oluşturur ve bu değerleri $OozieConfigValues üyesi olarak depolar.

Dokuzuncu komutu bir **AzureHDInsightMapReduceConfiguration** nesnesi oluşturur ve $MapredConfigValues değişkeninde depolar.
Sonraki iki komut MapReduce için yapılandırma değerleri oluşturur ve bu değerleri $MapredConfigValues üyeleri olarak depolar.

On ikinci komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.
Bu komut, AzureHDInsightDefaultStorage cmdlet 'ini **set-** cmdlet 'ine geçirmek için $config geçirmek üzere, yeni yapılandırma değerlerini küme yapılandırmasına eklemek için **Add-AzureHDInsightConfigValues** cmdlet 'ine kullanır.

Son komutu, AzureHDInsightCluster cmdlet 'ini yeni bir HDInsight kümesi oluşturmak için **Yeni-** cmdlet 'ine $config geçirmek için ardışık düzen işlecini kullanır.

## PARAMETRELERINE

### -Config
Hadoop yapılandırması ekleyeceğiniz yapılandırma nesnesini belirtir.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### Çekirdekli
Core-site.xml için bir Hadoop yapılandırma değerleri kümesi belirtir.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HBase
Hbase-site.xml için HBase yapılandırma değerleri kümesini belirtir.

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bir
Hdfs-site.xml için bir Hadoop yapılandırma değerleri kümesi belirtir.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kovanı
Hive-site.xml ve kovan paylaşılan kitaplıkları için bir Hadoop yapılandırma değeri içeren bir Hadoop kovanı hizmeti özelleştirme nesnesini belirtir.

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapReduce
MapReduce ve kapasite Zamanlayıcısı için bir özelleştirme nesnesi belirtir.

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oozie
Oozie-site.xml için bir Hadoop yapılandırma değeri içeren bir Hadoop Oozıe hizmeti özelleştirme nesnesini belirtir.

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Spark
Apache Spark için özelleştirme nesnesi belirtir.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fırtınası
Apache fırtınası için özelleştirme nesnesi belirtir.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yars
Yarn-site.xml için özelleştirilmiş YARıM yapılandırma değerleri kümesini belirten Hadoop YARN özelleştirme nesnesini belirtir.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
