---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938497"
---
# <span data-ttu-id="4f32b-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f32b-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="4f32b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f32b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f32b-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f32b-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="4f32b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f32b-104">SYNTAX</span></span>

### <span data-ttu-id="4f32b-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f32b-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f32b-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4f32b-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f32b-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4f32b-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f32b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f32b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f32b-109">New-AzHDInsightCluster belirtilen parametreleri kullanarak veya New-AzHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f32b-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4f32b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f32b-110">EXAMPLES</span></span>

### <span data-ttu-id="4f32b-111">Örnek 1: Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f32b-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="4f32b-112">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f32b-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="4f32b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f32b-113">PARAMETERS</span></span>

### <span data-ttu-id="4f32b-114">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="4f32b-114">-AadTenantId</span></span>
<span data-ttu-id="4f32b-115">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-116">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="4f32b-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="4f32b-117">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="4f32b-118">Alternatif olarak Add-AzHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f32b-119">-ApplicationId</span></span>
<span data-ttu-id="4f32b-120">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f32b-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4f32b-121">-CertificateFileContents</span></span>
<span data-ttu-id="4f32b-122">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4f32b-123">-CertificateFilePath</span></span>
<span data-ttu-id="4f32b-124">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4f32b-125">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f32b-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4f32b-126">-CertificatePassword</span></span>
<span data-ttu-id="4f32b-127">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4f32b-128">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f32b-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4f32b-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4f32b-129">-ClusterName</span></span>
<span data-ttu-id="4f32b-130">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-130">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-131">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="4f32b-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="4f32b-132">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-132">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4f32b-133">-ClusterTier</span></span>
<span data-ttu-id="4f32b-134">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4f32b-135">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="4f32b-135">By default, this is Standard.</span></span>
<span data-ttu-id="4f32b-136">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="4f32b-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-137">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4f32b-137">-ClusterType</span></span>
<span data-ttu-id="4f32b-138">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4f32b-139">Seçenekler: Hadoop, HBase, fırtınası, Spark, ıNTERACTIVEKOVANı, Kafka ve RServer</span><span class="sxs-lookup"><span data-stu-id="4f32b-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="4f32b-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4f32b-140">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-141">-Config</span><span class="sxs-lookup"><span data-stu-id="4f32b-141">-Config</span></span>
<span data-ttu-id="4f32b-142">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="4f32b-143">Bu nesne New-AzHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-144">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="4f32b-144">-Configurations</span></span>
<span data-ttu-id="4f32b-145">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="4f32b-146">Alternatif olarak Add-AzHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f32b-147">-DefaultProfile</span></span>
<span data-ttu-id="4f32b-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f32b-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f32b-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f32b-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4f32b-150">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4f32b-151">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f32b-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4f32b-153">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4f32b-154">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4f32b-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4f32b-156">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4f32b-157">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4f32b-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="4f32b-158">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="4f32b-158">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4f32b-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="4f32b-160">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4f32b-161">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4f32b-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="4f32b-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="4f32b-163">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="4f32b-164">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="4f32b-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="4f32b-165">Kümedeki çalışan düğümü rolü için disk sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-165">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f32b-166">-EdgeNodeSize</span></span>
<span data-ttu-id="4f32b-167">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4f32b-168">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4f32b-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4f32b-169">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-169">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4f32b-170">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f32b-170">-HeadNodeSize</span></span>
<span data-ttu-id="4f32b-171">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4f32b-172">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4f32b-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4f32b-173">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="4f32b-173">-HiveMetastore</span></span>
<span data-ttu-id="4f32b-174">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="4f32b-175">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4f32b-176">-HttpCredential</span></span>
<span data-ttu-id="4f32b-177">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-178">-Konum</span><span class="sxs-lookup"><span data-stu-id="4f32b-178">-Location</span></span>
<span data-ttu-id="4f32b-179">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-179">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4f32b-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="4f32b-181">Desteklenen en düşük TLS sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f32b-181">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="4f32b-182">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4f32b-182">-ObjectId</span></span>
<span data-ttu-id="4f32b-183">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4f32b-184">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f32b-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-185">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="4f32b-185">-OozieMetastore</span></span>
<span data-ttu-id="4f32b-186">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="4f32b-187">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="4f32b-188">-OSType</span></span>
<span data-ttu-id="4f32b-189">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="4f32b-190">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="4f32b-190">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-191">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="4f32b-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="4f32b-192">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="4f32b-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="4f32b-193">-RdpCredential</span></span>
<span data-ttu-id="4f32b-194">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="4f32b-195">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-195">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f32b-196">-ResourceGroupName</span></span>
<span data-ttu-id="4f32b-197">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-197">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-198">-Betikler</span><span class="sxs-lookup"><span data-stu-id="4f32b-198">-ScriptActions</span></span>
<span data-ttu-id="4f32b-199">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="4f32b-200">Alternatif olarak Add-AzHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4f32b-201">-SecurityProfile</span></span>
<span data-ttu-id="4f32b-202">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="4f32b-203">Alternatif olarak Add-AzHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f32b-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="4f32b-204">-SshCredential</span></span>
<span data-ttu-id="4f32b-205">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="4f32b-206">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-206">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f32b-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4f32b-207">-SshPublicKey</span></span>
<span data-ttu-id="4f32b-208">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="4f32b-209">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-209">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4f32b-210">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4f32b-210">-SubnetName</span></span>
<span data-ttu-id="4f32b-211">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="4f32b-212">-Version</span><span class="sxs-lookup"><span data-stu-id="4f32b-212">-Version</span></span>
<span data-ttu-id="4f32b-213">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-213">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="4f32b-214">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="4f32b-214">-VirtualNetworkId</span></span>
<span data-ttu-id="4f32b-215">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="4f32b-216">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f32b-216">-WorkerNodeSize</span></span>
<span data-ttu-id="4f32b-217">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4f32b-218">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4f32b-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4f32b-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4f32b-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4f32b-220">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4f32b-221">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4f32b-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4f32b-222">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4f32b-222">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4f32b-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f32b-223">CommonParameters</span></span>
<span data-ttu-id="4f32b-224">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f32b-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f32b-225">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f32b-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f32b-226">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f32b-226">INPUTS</span></span>

### <span data-ttu-id="4f32b-227">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4f32b-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4f32b-228">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f32b-228">OUTPUTS</span></span>

### <span data-ttu-id="4f32b-229">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f32b-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4f32b-230">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f32b-230">NOTES</span></span>
<span data-ttu-id="4f32b-231">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="4f32b-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="4f32b-232">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f32b-232">RELATED LINKS</span></span>

[<span data-ttu-id="4f32b-233">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4f32b-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

