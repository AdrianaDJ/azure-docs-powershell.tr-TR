---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590262"
---
# <span data-ttu-id="c7a03-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c7a03-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="c7a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a03-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a03-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7a03-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7a03-104">SYNTAX</span></span>

### <span data-ttu-id="c7a03-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7a03-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a03-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c7a03-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a03-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c7a03-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a03-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7a03-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a03-109">New-AzureHDInsightCluster belirtilen parametreleri kullanarak veya New-AzureRmHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7a03-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c7a03-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7a03-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a03-111">Örnek 1: Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7a03-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
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

<span data-ttu-id="c7a03-112">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7a03-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="c7a03-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7a03-113">PARAMETERS</span></span>

### <span data-ttu-id="c7a03-114">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="c7a03-114">-AadTenantId</span></span>
<span data-ttu-id="c7a03-115">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c7a03-116">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="c7a03-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="c7a03-117">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="c7a03-118">Alternatif olarak Add-AzureRmHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c7a03-119">-CertificateFileContents</span></span>
<span data-ttu-id="c7a03-120">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c7a03-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c7a03-121">-CertificateFilePath</span></span>
<span data-ttu-id="c7a03-122">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c7a03-123">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7a03-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c7a03-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c7a03-124">-CertificatePassword</span></span>
<span data-ttu-id="c7a03-125">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c7a03-126">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7a03-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c7a03-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c7a03-127">-ClusterName</span></span>
<span data-ttu-id="c7a03-128">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c7a03-129">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="c7a03-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="c7a03-130">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="c7a03-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c7a03-131">-ClusterTier</span></span>
<span data-ttu-id="c7a03-132">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c7a03-133">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="c7a03-133">By default, this is Standard.</span></span>
<span data-ttu-id="c7a03-134">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="c7a03-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c7a03-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c7a03-135">-ClusterType</span></span>
<span data-ttu-id="c7a03-136">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c7a03-137">Seçenekler: Hadoop, HBase, fırtınası, Spark</span><span class="sxs-lookup"><span data-stu-id="c7a03-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="c7a03-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c7a03-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="c7a03-139">-Config</span><span class="sxs-lookup"><span data-stu-id="c7a03-139">-Config</span></span>
<span data-ttu-id="c7a03-140">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="c7a03-141">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-142">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="c7a03-142">-Configurations</span></span>
<span data-ttu-id="c7a03-143">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="c7a03-144">Alternatif olarak Add-AzureRmHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a03-145">-DefaultProfile</span></span>
<span data-ttu-id="c7a03-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7a03-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7a03-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c7a03-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c7a03-148">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c7a03-149">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c7a03-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c7a03-151">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c7a03-152">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c7a03-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="c7a03-154">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="c7a03-155">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="c7a03-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="c7a03-156">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="c7a03-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="c7a03-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7a03-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="c7a03-158">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c7a03-159">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="c7a03-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="c7a03-161">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="c7a03-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="c7a03-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="c7a03-163">Kümedeki çalışan düğümü rolü için disk sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="c7a03-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c7a03-164">-EdgeNodeSize</span></span>
<span data-ttu-id="c7a03-165">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c7a03-166">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c7a03-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c7a03-167">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c7a03-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c7a03-168">-HeadNodeSize</span></span>
<span data-ttu-id="c7a03-169">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c7a03-170">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c7a03-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c7a03-171">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="c7a03-171">-HiveMetastore</span></span>
<span data-ttu-id="c7a03-172">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="c7a03-173">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c7a03-174">-HttpCredential</span></span>
<span data-ttu-id="c7a03-175">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="c7a03-176">-Konum</span><span class="sxs-lookup"><span data-stu-id="c7a03-176">-Location</span></span>
<span data-ttu-id="c7a03-177">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="c7a03-178">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c7a03-178">-ObjectId</span></span>
<span data-ttu-id="c7a03-179">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c7a03-180">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7a03-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c7a03-181">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="c7a03-181">-OozieMetastore</span></span>
<span data-ttu-id="c7a03-182">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="c7a03-183">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="c7a03-184">-OSType</span></span>
<span data-ttu-id="c7a03-185">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="c7a03-186">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="c7a03-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="c7a03-187">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="c7a03-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="c7a03-188">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="c7a03-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="c7a03-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c7a03-189">-RdpCredential</span></span>
<span data-ttu-id="c7a03-190">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="c7a03-191">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="c7a03-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a03-192">-ResourceGroupName</span></span>
<span data-ttu-id="c7a03-193">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c7a03-194">-Betikler</span><span class="sxs-lookup"><span data-stu-id="c7a03-194">-ScriptActions</span></span>
<span data-ttu-id="c7a03-195">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="c7a03-196">Alternatif olarak Add-AzureRmHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="c7a03-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="c7a03-197">-SecurityProfile</span></span>
<span data-ttu-id="c7a03-198">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="c7a03-199">Alternatif olarak Add-AzureRmHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a03-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="c7a03-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="c7a03-200">-SshCredential</span></span>
<span data-ttu-id="c7a03-201">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="c7a03-202">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="c7a03-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c7a03-203">-SshPublicKey</span></span>
<span data-ttu-id="c7a03-204">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="c7a03-205">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="c7a03-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c7a03-206">-SubnetName</span></span>
<span data-ttu-id="c7a03-207">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="c7a03-208">-Version</span><span class="sxs-lookup"><span data-stu-id="c7a03-208">-Version</span></span>
<span data-ttu-id="c7a03-209">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="c7a03-210">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="c7a03-210">-VirtualNetworkId</span></span>
<span data-ttu-id="c7a03-211">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="c7a03-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c7a03-212">-WorkerNodeSize</span></span>
<span data-ttu-id="c7a03-213">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c7a03-214">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c7a03-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c7a03-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c7a03-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c7a03-216">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c7a03-217">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c7a03-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c7a03-218">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c7a03-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c7a03-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a03-219">CommonParameters</span></span>
<span data-ttu-id="c7a03-220">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7a03-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a03-221">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a03-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a03-222">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7a03-222">INPUTS</span></span>

### <span data-ttu-id="c7a03-223">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c7a03-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="c7a03-224">Parametreler: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7a03-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="c7a03-225">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7a03-225">OUTPUTS</span></span>

### <span data-ttu-id="c7a03-226">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c7a03-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c7a03-227">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7a03-227">NOTES</span></span>
<span data-ttu-id="c7a03-228">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="c7a03-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="c7a03-229">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7a03-229">RELATED LINKS</span></span>

[<span data-ttu-id="c7a03-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c7a03-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

