---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105640"
---
# Get-AzureHDInsightJobOutput

## SYNOPSIS
İş için günlük çıkışını alır.

## INDEKI

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.
Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.
Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.

Küme oluştururken yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için, [Azure PowerShell kullanarak HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)'ta Linux tabanlı kümeler oluşturma konusuna bakın.
Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, [HDInsight 'de Hadoop Işlerini gönderme](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)konusuna bakın.
Azure PowerShell HDInsight hakkında başvuru bilgileri için [bkz.](https://msdn.microsoft.com/en-us/library/mt438705.aspx)

**Get-AzureHDInsightJobOutput** cmdlet 'i, kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.
Standart çıktı, standart hata, görev günlükleri ve görev günlüklerinin bir özeti dahil olmak üzere çeşitli türde iş günlükleri alabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: iş çıktısını alın
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

İlk komut geçerli aboneliğin KIMLIĞINI alır ve $SubId değişkeninde depolar.

İkinci komut $Clustername değişkeninde MyCluster adını depolar.

Üçüncü komut bir MapReduce iş tanımı oluşturur ve $WordCountJob değişkeninde depolar.
Komut, işi başlatmak için $WordCountJob işi **Start-AzureHDInsightJob** cmdlet 'ine geçirir.
Ayrıca, işlemin bitmesini beklemek için **wait-AzureHDInsightJob** cmdlet 'ine $WordCountJob geçirir ve ardından iş çıktısını almak için **Get-AzureHDInsightJobOutput** kullanır.

## PARAMETRELERINE

### -Sertifika
Azure aboneliği için yönetim sertifikasını belirtir.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Küme
Bir küme belirtir.
Bu cmdlet, bu parametrenin belirttiği kümeden iş günlüklerini alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DownloadTaskLogs
Bu cmdlet 'in bir iş için görev günlüklerini aldığını gösterir.

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

### Uç nokta
Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.
Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Varsayılan ad boşluğunu kullanmak istemezseniz, bir HDInsight hizmeti ad boşluğunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Alınacak işin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Standara
Bu cmdlet 'in bir işin StdErr çıkışını aldığını gösterir.

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

### -StandardOutput
Bu cmdlet 'in bir işin SdtOut çıktısını aldığını gösterir.

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

### -Abonelik
Alınacak HDInsight kümesini içeren aboneliği belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskLogsDirectory
Görev günlüklerinin depolanacağı yerel klasörü belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSummary
Bu cmdlet 'lerin görev günlüğü özetini aldığını gösterir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[Start-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Bekle-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)
