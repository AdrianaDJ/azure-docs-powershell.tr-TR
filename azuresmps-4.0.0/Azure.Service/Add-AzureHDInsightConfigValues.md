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
# <span data-ttu-id="51a4d-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="51a4d-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="51a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="51a4d-103">HDInsight küme yapılandırmasına bir Hadoop yapılandırma değeri özelleştirmesi veya kovan Paylaşılan kitaplık özelleştirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="51a4d-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="51a4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51a4d-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51a4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="51a4d-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="51a4d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="51a4d-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="51a4d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="51a4d-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="51a4d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="51a4d-109">Küme oluştururken yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için, [Azure PowerShell kullanarak HDInsight 'Ta Linux tabanlı kümeler oluşturma](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="51a4d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="51a4d-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, [HDInsight 'de Hadoop Işlerini gönderme](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="51a4d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="51a4d-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [bkz.](https://msdn.microsoft.com/en-us/library/mt438705.aspx)</span><span class="sxs-lookup"><span data-stu-id="51a4d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="51a4d-112">**Add-AzureHDInsightConfigValues** cmdlet 'i, Core-site.xml veya Hive-site.xml gibi bir Hadoop yapılandırma değeri özelleştirmesi veya bir Azure HDInsight küme yapılandırmasına yığın Paylaşılan kitaplık özelleştirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="51a4d-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="51a4d-113">Cmdlet, belirtilen yapılandırma nesnesine özel yapılandırma değerleri ekler.</span><span class="sxs-lookup"><span data-stu-id="51a4d-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="51a4d-114">Özel ayarlar, küme dağıtıldığında ilgili Hadoop hizmetlerinin yapılandırma dosyalarına eklenir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="51a4d-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51a4d-115">EXAMPLES</span></span>

### <span data-ttu-id="51a4d-116">Örnek 1: kümeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="51a4d-116">Example 1: Configure a cluster</span></span>
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

<span data-ttu-id="51a4d-117">İlk komut yeni bir **AzureHDInsightHiveConfiguration** nesnesi oluşturur ve $HiveConfigValues değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="51a4d-118">Sonraki beş komut, kovan için yapılandırma değerleri oluşturur ve bu değerleri $HiveConfigValues üyeleri olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="51a4d-119">Yedinci komutu bir **AzureHDInsightOozieConfiguration** nesnesi oluşturur ve $OozieConfigValues değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="51a4d-120">Sekizinci komutu Oozie için bir yapılandırma değeri oluşturur ve bu değerleri $OozieConfigValues üyesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="51a4d-121">Dokuzuncu komutu bir **AzureHDInsightMapReduceConfiguration** nesnesi oluşturur ve $MapredConfigValues değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="51a4d-122">Sonraki iki komut MapReduce için yapılandırma değerleri oluşturur ve bu değerleri $MapredConfigValues üyeleri olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="51a4d-123">On ikinci komut, bir HDInsight küme yapılandırması oluşturmak için **New-AzureHDInsightClusterConfig** cmdlet 'ini kullanır ve ardından $config değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51a4d-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="51a4d-124">Bu komut, AzureHDInsightDefaultStorage cmdlet 'ini **set-** cmdlet 'ine geçirmek için $config geçirmek üzere, yeni yapılandırma değerlerini küme yapılandırmasına eklemek için **Add-AzureHDInsightConfigValues** cmdlet 'ine kullanır.</span><span class="sxs-lookup"><span data-stu-id="51a4d-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="51a4d-125">Son komutu, AzureHDInsightCluster cmdlet 'ini yeni bir HDInsight kümesi oluşturmak için **Yeni-** cmdlet 'ine $config geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="51a4d-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="51a4d-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51a4d-126">PARAMETERS</span></span>

### <span data-ttu-id="51a4d-127">-Config</span><span class="sxs-lookup"><span data-stu-id="51a4d-127">-Config</span></span>
<span data-ttu-id="51a4d-128">Hadoop yapılandırması ekleyeceğiniz yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

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

### <span data-ttu-id="51a4d-129">Çekirdekli</span><span class="sxs-lookup"><span data-stu-id="51a4d-129">-Core</span></span>
<span data-ttu-id="51a4d-130">Core-site.xml için bir Hadoop yapılandırma değerleri kümesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

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

### <span data-ttu-id="51a4d-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="51a4d-131">-HBase</span></span>
<span data-ttu-id="51a4d-132">Hbase-site.xml için HBase yapılandırma değerleri kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

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

### <span data-ttu-id="51a4d-133">-Bir</span><span class="sxs-lookup"><span data-stu-id="51a4d-133">-Hdfs</span></span>
<span data-ttu-id="51a4d-134">Hdfs-site.xml için bir Hadoop yapılandırma değerleri kümesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

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

### <span data-ttu-id="51a4d-135">-Kovanı</span><span class="sxs-lookup"><span data-stu-id="51a4d-135">-Hive</span></span>
<span data-ttu-id="51a4d-136">Hive-site.xml ve kovan paylaşılan kitaplıkları için bir Hadoop yapılandırma değeri içeren bir Hadoop kovanı hizmeti özelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

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

### <span data-ttu-id="51a4d-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="51a4d-137">-MapReduce</span></span>
<span data-ttu-id="51a4d-138">MapReduce ve kapasite Zamanlayıcısı için bir özelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

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

### <span data-ttu-id="51a4d-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="51a4d-139">-Oozie</span></span>
<span data-ttu-id="51a4d-140">Oozie-site.xml için bir Hadoop yapılandırma değeri içeren bir Hadoop Oozıe hizmeti özelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

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

### <span data-ttu-id="51a4d-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="51a4d-141">-Profile</span></span>
<span data-ttu-id="51a4d-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51a4d-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="51a4d-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51a4d-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="51a4d-144">-Spark</span></span>
<span data-ttu-id="51a4d-145">Apache Spark için özelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-145">Specifies a customization object for Apache Spark.</span></span>

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

### <span data-ttu-id="51a4d-146">-Fırtınası</span><span class="sxs-lookup"><span data-stu-id="51a4d-146">-Storm</span></span>
<span data-ttu-id="51a4d-147">Apache fırtınası için özelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-147">Specifies a customization object for Apache Storm.</span></span>

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

### <span data-ttu-id="51a4d-148">-Yars</span><span class="sxs-lookup"><span data-stu-id="51a4d-148">-Yarn</span></span>
<span data-ttu-id="51a4d-149">Yarn-site.xml için özelleştirilmiş YARıM yapılandırma değerleri kümesini belirten Hadoop YARN özelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51a4d-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

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

### <span data-ttu-id="51a4d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a4d-150">CommonParameters</span></span>
<span data-ttu-id="51a4d-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51a4d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a4d-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a4d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a4d-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51a4d-153">INPUTS</span></span>

## <span data-ttu-id="51a4d-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51a4d-154">OUTPUTS</span></span>

## <span data-ttu-id="51a4d-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51a4d-155">NOTES</span></span>

## <span data-ttu-id="51a4d-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51a4d-156">RELATED LINKS</span></span>

[<span data-ttu-id="51a4d-157">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="51a4d-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="51a4d-158">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="51a4d-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="51a4d-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="51a4d-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
