---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 0e287922c692a8271a82a62f20539bb97518b9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764061"
---
# <span data-ttu-id="090be-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="090be-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="090be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="090be-102">SYNOPSIS</span></span>
<span data-ttu-id="090be-103">Bir küme yapılandırma nesnesine bir Hadoop yapılandırma değeri özelleştirmesi ve/veya kovan Paylaşılan kitaplık özelleştirmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="090be-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="090be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="090be-104">SYNTAX</span></span>

### <span data-ttu-id="090be-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="090be-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="090be-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="090be-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="090be-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="090be-107">DESCRIPTION</span></span>
<span data-ttu-id="090be-108">**Add-AzureRmHDInsightConfigValues** cmdlet 'i, core-site.xml veya hive-site.xml ve/veya New-AzureRmHDInsightClusterConfig cmdlet 'i tarafından oluşturulan HDInsight yapılandırma nesnesine bir Hive Paylaşılan kitaplık özelleştirmesi gibi bir Hadoop yapılandırma değeri ekler.</span><span class="sxs-lookup"><span data-stu-id="090be-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="090be-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="090be-109">EXAMPLES</span></span>

### <span data-ttu-id="090be-110">Örnek 1: küme yapılandırma nesnesine özel bir yapılandırma değeri ekleme</span><span class="sxs-lookup"><span data-stu-id="090be-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="090be-111">Bu komut,-Hadoop-001 adlı kümeye bir Hadoop yapılandırması değeri ekler.</span><span class="sxs-lookup"><span data-stu-id="090be-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="090be-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="090be-112">PARAMETERS</span></span>

### <span data-ttu-id="090be-113">-Config</span><span class="sxs-lookup"><span data-stu-id="090be-113">-Config</span></span>
<span data-ttu-id="090be-114">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="090be-115">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="090be-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="090be-116">Çekirdekli</span><span class="sxs-lookup"><span data-stu-id="090be-116">-Core</span></span>
<span data-ttu-id="090be-117">Bu HDInsight kümesinin çekirdek site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="090be-118">-HBaseEnv</span></span>
<span data-ttu-id="090be-119">Bu HDInsight kümesinin HBase env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="090be-120">-HBaseSite</span></span>
<span data-ttu-id="090be-121">Bu HDInsight kümesinin HBase site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-122">-Bir</span><span class="sxs-lookup"><span data-stu-id="090be-122">-Hdfs</span></span>
<span data-ttu-id="090be-123">Bu HDInsight kümesinin işlem yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="090be-124">-HiveEnv</span></span>
<span data-ttu-id="090be-125">Bu HDInsight kümesinin yığın env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="090be-126">-HiveSite</span></span>
<span data-ttu-id="090be-127">Bu HDInsight kümesinin kovan site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="090be-128">-MapRed</span></span>
<span data-ttu-id="090be-129">Bu HDInsight kümesinin MapRed site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-130">-Oozıeenv</span><span class="sxs-lookup"><span data-stu-id="090be-130">-OozieEnv</span></span>
<span data-ttu-id="090be-131">Bu HDInsight kümesinin Oozıe env yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-132">-Oozıesite</span><span class="sxs-lookup"><span data-stu-id="090be-132">-OozieSite</span></span>
<span data-ttu-id="090be-133">Bu HDInsight kümesinin Oozıe site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="090be-134">-RServer</span></span>
<span data-ttu-id="090be-135">RServer yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="090be-136">Yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="090be-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="090be-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="090be-137">-Spark2Defaults</span></span>
<span data-ttu-id="090be-138">Bu HDInsight kümesinin Spark2 Varsayılanları yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="090be-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="090be-140">Bu HDInsight kümesinin Spark2 Thrift parlak conf yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-141">-Parlak varsayılanlar</span><span class="sxs-lookup"><span data-stu-id="090be-141">-SparkDefaults</span></span>
<span data-ttu-id="090be-142">Bu HDInsight kümesinin Spark Varsayılanları yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-143">-Parlak Thriftconf</span><span class="sxs-lookup"><span data-stu-id="090be-143">-SparkThriftConf</span></span>
<span data-ttu-id="090be-144">Bu HDInsight kümesinin Spark, RIFT mini conf yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-145">-Fırtınası</span><span class="sxs-lookup"><span data-stu-id="090be-145">-Storm</span></span>
<span data-ttu-id="090be-146">Bu HDInsight kümesinin fırtınası site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="090be-147">-Tez</span></span>
<span data-ttu-id="090be-148">Bu HDInsight kümesinin tez site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="090be-149">-WebHCat</span></span>
<span data-ttu-id="090be-150">Bu HDInsight kümesinin WebHCat site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-151">-Yars</span><span class="sxs-lookup"><span data-stu-id="090be-151">-Yarn</span></span>
<span data-ttu-id="090be-152">Bu HDInsight kümesinin YARN site yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="090be-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="090be-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090be-153">-DefaultProfile</span></span>
<span data-ttu-id="090be-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="090be-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="090be-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090be-155">CommonParameters</span></span>
<span data-ttu-id="090be-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="090be-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090be-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090be-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090be-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="090be-158">INPUTS</span></span>

### <span data-ttu-id="090be-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="090be-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="090be-160">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="090be-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="090be-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="090be-161">OUTPUTS</span></span>

### <span data-ttu-id="090be-162">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="090be-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="090be-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="090be-163">NOTES</span></span>

## <span data-ttu-id="090be-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="090be-164">RELATED LINKS</span></span>

[<span data-ttu-id="090be-165">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="090be-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


