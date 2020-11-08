---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 6482c6e6804b9d59ddbd752d20f39d3316b75f8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109634"
---
# <span data-ttu-id="eaeb3-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="eaeb3-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="eaeb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="eaeb3-103">Bir küme yapılandırma nesnesine bir Hadoop yapılandırma değeri özelleştirmesi ve/veya kovan Paylaşılan kitaplık özelleştirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="eaeb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaeb3-104">SYNTAX</span></span>

### <span data-ttu-id="eaeb3-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="eaeb3-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eaeb3-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="eaeb3-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eaeb3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaeb3-107">DESCRIPTION</span></span>
<span data-ttu-id="eaeb3-108">**Add-AzHDInsightConfigValue** cmdlet 'i, core-site.xml veya hive-site.xml ve/veya New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan HDInsight yapılandırma nesnesine bir Hive Paylaşılan kitaplık özelleştirmesi gibi bir Hadoop yapılandırma değeri ekler.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="eaeb3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaeb3-109">EXAMPLES</span></span>

### <span data-ttu-id="eaeb3-110">Örnek 1: küme yapılandırma nesnesine özel bir yapılandırma değeri ekleme</span><span class="sxs-lookup"><span data-stu-id="eaeb3-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="eaeb3-111">Bu komut,-Hadoop-001 adlı kümeye bir Hadoop yapılandırması değeri ekler.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="eaeb3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaeb3-112">PARAMETERS</span></span>

### <span data-ttu-id="eaeb3-113">-Config</span><span class="sxs-lookup"><span data-stu-id="eaeb3-113">-Config</span></span>
<span data-ttu-id="eaeb3-114">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="eaeb3-115">Bu nesne New-AzHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaeb3-116">Çekirdekli</span><span class="sxs-lookup"><span data-stu-id="eaeb3-116">-Core</span></span>
<span data-ttu-id="eaeb3-117">Bu HDInsight kümesinin çekirdek site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaeb3-118">-DefaultProfile</span></span>
<span data-ttu-id="eaeb3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eaeb3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaeb3-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="eaeb3-120">-HBaseEnv</span></span>
<span data-ttu-id="eaeb3-121">Bu HDInsight kümesinin HBase env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="eaeb3-122">-HBaseSite</span></span>
<span data-ttu-id="eaeb3-123">Bu HDInsight kümesinin HBase site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-124">-Bir</span><span class="sxs-lookup"><span data-stu-id="eaeb3-124">-Hdfs</span></span>
<span data-ttu-id="eaeb3-125">Bu HDInsight kümesinin işlem yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="eaeb3-126">-HiveEnv</span></span>
<span data-ttu-id="eaeb3-127">Bu HDInsight kümesinin yığın env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="eaeb3-128">-HiveSite</span></span>
<span data-ttu-id="eaeb3-129">Bu HDInsight kümesinin kovan site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="eaeb3-130">-MapRed</span></span>
<span data-ttu-id="eaeb3-131">Bu HDInsight kümesinin MapRed site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-132">-Oozıeenv</span><span class="sxs-lookup"><span data-stu-id="eaeb3-132">-OozieEnv</span></span>
<span data-ttu-id="eaeb3-133">Bu HDInsight kümesinin Oozıe env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-134">-Oozıesite</span><span class="sxs-lookup"><span data-stu-id="eaeb3-134">-OozieSite</span></span>
<span data-ttu-id="eaeb3-135">Bu HDInsight kümesinin Oozıe site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="eaeb3-136">-RServer</span></span>
<span data-ttu-id="eaeb3-137">RServer yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="eaeb3-138">Yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="eaeb3-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="eaeb3-139">-Spark2Defaults</span></span>
<span data-ttu-id="eaeb3-140">Bu HDInsight kümesinin Spark2 Varsayılanları yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaeb3-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="eaeb3-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="eaeb3-142">Bu HDInsight kümesinin Spark2 Thrift parlak conf yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaeb3-143">-Parlak varsayılanlar</span><span class="sxs-lookup"><span data-stu-id="eaeb3-143">-SparkDefaults</span></span>
<span data-ttu-id="eaeb3-144">Bu HDInsight kümesinin Spark Varsayılanları yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaeb3-145">-Parlak Thriftconf</span><span class="sxs-lookup"><span data-stu-id="eaeb3-145">-SparkThriftConf</span></span>
<span data-ttu-id="eaeb3-146">Bu HDInsight kümesinin Spark, RIFT mini conf yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaeb3-147">-Fırtınası</span><span class="sxs-lookup"><span data-stu-id="eaeb3-147">-Storm</span></span>
<span data-ttu-id="eaeb3-148">Bu HDInsight kümesinin fırtınası site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="eaeb3-149">-Tez</span></span>
<span data-ttu-id="eaeb3-150">Bu HDInsight kümesinin tez site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="eaeb3-151">-WebHCat</span></span>
<span data-ttu-id="eaeb3-152">Bu HDInsight kümesinin WebHCat site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-153">-Yars</span><span class="sxs-lookup"><span data-stu-id="eaeb3-153">-Yarn</span></span>
<span data-ttu-id="eaeb3-154">Bu HDInsight kümesinin YARN site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="eaeb3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaeb3-155">CommonParameters</span></span>
<span data-ttu-id="eaeb3-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaeb3-157">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaeb3-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaeb3-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaeb3-158">INPUTS</span></span>

### <span data-ttu-id="eaeb3-159">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="eaeb3-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="eaeb3-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaeb3-160">OUTPUTS</span></span>

### <span data-ttu-id="eaeb3-161">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="eaeb3-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="eaeb3-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaeb3-162">NOTES</span></span>

## <span data-ttu-id="eaeb3-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaeb3-163">RELATED LINKS</span></span>

[<span data-ttu-id="eaeb3-164">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="eaeb3-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


