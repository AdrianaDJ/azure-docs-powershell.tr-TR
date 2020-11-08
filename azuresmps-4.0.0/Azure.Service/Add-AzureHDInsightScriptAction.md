---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105720"
---
# Add-AzureHDInsightScriptAction

## SYNOPSIS
HDInsight betik eylemi ekler.

## INDEKI

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.
Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.
Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.

Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

**Add-AzureHDInsightScriptAction** cmdlet 'i, ek yazılım yüklemek veya Windows PowerShell komut dosyalarını kullanarak bir Hadoop kümesinde çalışan uygulamaların yapılandırmalarını değiştirmek Için kullanılan Azure HDInsight işlevselliğini sağlar.

Bir betik eylemi, HDInsight kümeleri dağıtıldığında küme düğümlerinde çalışır ve kümenin tamamlanma HDInsight yapılandırmasındaki düğümlerden sonra çalışırlar.
Komut dosyası eylemi sistem yöneticisi hesap ayrıcalıklarıyla çalışır ve küme düğümlerine tam erişim hakları sağlar.
Belirli bir sırada çalışacak bir komut dosyası eylemleri listesi içeren her kümeyi sağlayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: kümeye komut dosyası eylemi ekleme
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

İlk komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.

İkinci komut, $Config öğesine TestScriptAction adlı betik eylemini eklemek için **Add-AzureHDInsightScriptAction** cmdlet 'ini kullanır.

Son komutu, $Config uygulamasında depolanan komut dosyası eylemini çalıştıran yeni bir HDInsight kümesi oluşturmak için **New-AzureHDInsightCluster** cmdlet 'ini kullanır.

### Örnek 2: kümeye birden çok betik eylemi ekleme
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

İlk komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.

İkinci komut, **Add-AzureHDInsightScriptAction** cmdlet 'ini kullanarak belirtilen komut dosyası eylemini $config ve ardından $config **geçirmek için $config ikinci bir komut** dosyası eylemi ekleme

Final komutu, $Config komut dosyası eylemlerini çalıştıran bir küme oluşturmak için **New-AzureHDInsightCluster** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -ClusterRoleCollection
Komut dosyası çalıştıracak düğümleri belirtir.
Bu parametre için kabul edilebilir değerler: HeadNode veya DataNode.

Bir değer veya her iki değeri de belirtebilirsiniz.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Yapılandırma nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği nesneye betik eylem bilgileri ekler.

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

### -Ad
Betik eyleminin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametreler
Komut dosyası eyleminin gerektirdiği parametreleri belirtir.

```yaml
Type: String
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

### -URI
Çalıştırılacak komut dosyasının URI konumunu belirtir.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
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


