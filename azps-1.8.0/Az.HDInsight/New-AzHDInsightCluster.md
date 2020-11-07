---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916600"
---
# <span data-ttu-id="dec9c-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dec9c-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="dec9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dec9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dec9c-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec9c-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="dec9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dec9c-104">SYNTAX</span></span>

### <span data-ttu-id="dec9c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dec9c-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="dec9c-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="dec9c-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="dec9c-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="dec9c-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

## <span data-ttu-id="dec9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dec9c-108">DESCRIPTION</span></span>
<span data-ttu-id="dec9c-109">New-AzHDInsightCluster belirtilen parametreleri kullanarak veya New-AzHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec9c-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="dec9c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dec9c-110">EXAMPLES</span></span>

### <span data-ttu-id="dec9c-111">Örnek 1: Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dec9c-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="dec9c-112">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec9c-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="dec9c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dec9c-113">PARAMETERS</span></span>

### <span data-ttu-id="dec9c-114">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="dec9c-114">-AadTenantId</span></span>
<span data-ttu-id="dec9c-115">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dec9c-116">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="dec9c-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="dec9c-117">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="dec9c-118">Alternatif olarak Add-AzHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="dec9c-119">-CertificateFileContents</span></span>
<span data-ttu-id="dec9c-120">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dec9c-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="dec9c-121">-CertificateFilePath</span></span>
<span data-ttu-id="dec9c-122">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="dec9c-123">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dec9c-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dec9c-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dec9c-124">-CertificatePassword</span></span>
<span data-ttu-id="dec9c-125">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="dec9c-126">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dec9c-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dec9c-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dec9c-127">-ClusterName</span></span>
<span data-ttu-id="dec9c-128">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="dec9c-129">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="dec9c-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="dec9c-130">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="dec9c-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="dec9c-131">-ClusterTier</span></span>
<span data-ttu-id="dec9c-132">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="dec9c-133">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="dec9c-133">By default, this is Standard.</span></span>
<span data-ttu-id="dec9c-134">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="dec9c-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="dec9c-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="dec9c-135">-ClusterType</span></span>
<span data-ttu-id="dec9c-136">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="dec9c-137">Seçenekler: Hadoop, HBase, fırtınası, Spark</span><span class="sxs-lookup"><span data-stu-id="dec9c-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="dec9c-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="dec9c-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="dec9c-139">-Config</span><span class="sxs-lookup"><span data-stu-id="dec9c-139">-Config</span></span>
<span data-ttu-id="dec9c-140">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="dec9c-141">Bu nesne New-AzHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-142">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="dec9c-142">-Configurations</span></span>
<span data-ttu-id="dec9c-143">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="dec9c-144">Alternatif olarak Add-AzHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec9c-145">-DefaultProfile</span></span>
<span data-ttu-id="dec9c-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dec9c-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dec9c-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dec9c-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="dec9c-148">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="dec9c-149">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dec9c-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="dec9c-151">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="dec9c-152">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dec9c-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="dec9c-154">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="dec9c-155">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="dec9c-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="dec9c-156">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="dec9c-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="dec9c-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dec9c-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="dec9c-158">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="dec9c-159">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="dec9c-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="dec9c-161">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="dec9c-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="dec9c-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="dec9c-163">Kümedeki çalışan düğümü rolü için disk sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="dec9c-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="dec9c-164">-EdgeNodeSize</span></span>
<span data-ttu-id="dec9c-165">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="dec9c-166">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="dec9c-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="dec9c-167">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="dec9c-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="dec9c-168">-HeadNodeSize</span></span>
<span data-ttu-id="dec9c-169">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="dec9c-170">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="dec9c-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="dec9c-171">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="dec9c-171">-HiveMetastore</span></span>
<span data-ttu-id="dec9c-172">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="dec9c-173">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="dec9c-174">-HttpCredential</span></span>
<span data-ttu-id="dec9c-175">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="dec9c-176">-Konum</span><span class="sxs-lookup"><span data-stu-id="dec9c-176">-Location</span></span>
<span data-ttu-id="dec9c-177">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="dec9c-178">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="dec9c-178">-ObjectId</span></span>
<span data-ttu-id="dec9c-179">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="dec9c-180">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dec9c-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="dec9c-181">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="dec9c-181">-OozieMetastore</span></span>
<span data-ttu-id="dec9c-182">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="dec9c-183">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="dec9c-184">-OSType</span></span>
<span data-ttu-id="dec9c-185">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="dec9c-186">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="dec9c-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="dec9c-187">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="dec9c-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="dec9c-188">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="dec9c-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="dec9c-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="dec9c-189">-RdpCredential</span></span>
<span data-ttu-id="dec9c-190">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="dec9c-191">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="dec9c-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec9c-192">-ResourceGroupName</span></span>
<span data-ttu-id="dec9c-193">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dec9c-194">-Betikler</span><span class="sxs-lookup"><span data-stu-id="dec9c-194">-ScriptActions</span></span>
<span data-ttu-id="dec9c-195">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="dec9c-196">Alternatif olarak Add-AzHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="dec9c-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="dec9c-197">-SecurityProfile</span></span>
<span data-ttu-id="dec9c-198">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="dec9c-199">Alternatif olarak Add-AzHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dec9c-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="dec9c-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="dec9c-200">-SshCredential</span></span>
<span data-ttu-id="dec9c-201">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="dec9c-202">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="dec9c-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="dec9c-203">-SshPublicKey</span></span>
<span data-ttu-id="dec9c-204">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="dec9c-205">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="dec9c-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="dec9c-206">-SubnetName</span></span>
<span data-ttu-id="dec9c-207">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="dec9c-208">-Version</span><span class="sxs-lookup"><span data-stu-id="dec9c-208">-Version</span></span>
<span data-ttu-id="dec9c-209">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="dec9c-210">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="dec9c-210">-VirtualNetworkId</span></span>
<span data-ttu-id="dec9c-211">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="dec9c-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="dec9c-212">-WorkerNodeSize</span></span>
<span data-ttu-id="dec9c-213">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="dec9c-214">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="dec9c-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="dec9c-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="dec9c-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="dec9c-216">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="dec9c-217">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="dec9c-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="dec9c-218">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="dec9c-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="dec9c-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec9c-219">CommonParameters</span></span>
<span data-ttu-id="dec9c-220">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dec9c-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec9c-221">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec9c-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec9c-222">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dec9c-222">INPUTS</span></span>

### <span data-ttu-id="dec9c-223">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="dec9c-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dec9c-224">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dec9c-224">OUTPUTS</span></span>

### <span data-ttu-id="dec9c-225">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dec9c-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="dec9c-226">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dec9c-226">NOTES</span></span>
<span data-ttu-id="dec9c-227">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="dec9c-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="dec9c-228">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dec9c-228">RELATED LINKS</span></span>

[<span data-ttu-id="dec9c-229">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dec9c-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

