---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594692"
---
# Invoke-AzureRmHDInsightHiveJob

## SYNOPSIS
Bir HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Invoke-AzureRmHDInsightHiveJob** cmdlet 'ı bir Azure HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.
Sorgu için kullanılacak kümeyi belirtmek üzere **Invoke-AzureRmHDInsightHiveJob** ' i çağırmadan önce Use-AzureRmHDInsightCluster cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: bir Azure HDInsight kümesine yığın sorgusu gönderme
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

Bu komut, TABLOLARı-Hadoop-001 adlı kümeye gönderir.

## PARAMETRELERINE

### -Bağımsız değişkenler
İş için bağımsız değişken dizisi belirtir.
Bağımsız değişkenler her göreve komut satırı bağımsız değişkenleri olarak geçirilir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultContainer
Varsayılan Azure depolama hesabında HDInsight kümesinin kullandığı varsayılan kapsayıcının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
HDInsight kümesinin kullandığı varsayılan depolama hesabının hesap anahtarını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
HDInsight kümesinin kullandığı varsayılan depolama hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tanımlar
Bir iş çalıştığında ayarlanacak Hadoop yapılandırma değerlerini belirtir.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dosya
Çalıştırılacak sorguyu içeren Azure depolama 'da bir dosyanın yolunu belirtir.
*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dosyalar
Bir kovan işi için gereken dosyalar koleksiyonunu belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Bir kovan işinin adını belirtir.
Bu parametreyi belirtmezseniz, bu cmdlet varsayılan değeri kullanır: "kovan: \<first 100 characters of Query\> ".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sorgu
Kovan sorgusunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAsFileJob
Bu cmdlet 'in, sorgunun depolanacağı varsayılan Azure depolama hesabında bir dosya oluşturacağını gösterir.
Bu cmdlet, bu dosyaya bir komut dosyası olarak başvuruda bulunan işi gönderir.

Bu işlevi yüzde işareti (%) gibi özel karakterleri işlemek için kullanabilirsiniz Bu, Templeton aracılığıyla bir iş gönderimi için başarısız olacak, çünkü Templeton yüzde işaretiyle bir sorguyu URL parametresi olarak yorumlar.

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

### -StatusFolder
İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Use-AzureRmHDInsightCluster](./Use-AzureRmHDInsightCluster.md)


