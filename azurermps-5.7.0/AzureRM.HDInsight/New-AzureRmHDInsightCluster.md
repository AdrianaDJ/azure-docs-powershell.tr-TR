---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: 2e778f84eabf7e5dc4dd325d2a17361064c5d99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594957"
---
# <span data-ttu-id="27cad-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="27cad-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="27cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27cad-102">SYNOPSIS</span></span>
<span data-ttu-id="27cad-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27cad-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27cad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27cad-104">SYNTAX</span></span>

### <span data-ttu-id="27cad-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27cad-105">Default (Default)</span></span>
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

### <span data-ttu-id="27cad-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="27cad-106">CertificateFilePath</span></span>
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

### <span data-ttu-id="27cad-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="27cad-107">CertificateFileContents</span></span>
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

## <span data-ttu-id="27cad-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27cad-108">DESCRIPTION</span></span>
<span data-ttu-id="27cad-109">New-AzureHDInsightCluster belirtilen parametreleri kullanarak veya New-AzureRmHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27cad-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="27cad-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27cad-110">EXAMPLES</span></span>

### <span data-ttu-id="27cad-111">--------------------------Örnek 1: Azure HDInsight kümesi oluşturma--------------------------</span><span class="sxs-lookup"><span data-stu-id="27cad-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
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

<span data-ttu-id="27cad-112">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27cad-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="27cad-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27cad-113">PARAMETERS</span></span>

### <span data-ttu-id="27cad-114">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="27cad-114">-AadTenantId</span></span>
<span data-ttu-id="27cad-115">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-116">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="27cad-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="27cad-117">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="27cad-118">Alternatif olarak Add-AzureRmHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="27cad-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="27cad-119">-CertificateFileContents</span></span>
<span data-ttu-id="27cad-120">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="27cad-121">-CertificateFilePath</span></span>
<span data-ttu-id="27cad-122">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="27cad-123">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27cad-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="27cad-124">-CertificatePassword</span></span>
<span data-ttu-id="27cad-125">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="27cad-126">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27cad-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="27cad-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="27cad-127">-ClusterName</span></span>
<span data-ttu-id="27cad-128">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-128">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-129">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="27cad-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="27cad-130">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="27cad-131">-ClusterTier</span></span>
<span data-ttu-id="27cad-132">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="27cad-133">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="27cad-133">By default, this is Standard.</span></span>
<span data-ttu-id="27cad-134">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="27cad-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="27cad-135">-ClusterType</span></span>
<span data-ttu-id="27cad-136">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="27cad-137">Seçenekler: Hadoop, HBase, fırtınası, Spark</span><span class="sxs-lookup"><span data-stu-id="27cad-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="27cad-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="27cad-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="27cad-139">-Config</span><span class="sxs-lookup"><span data-stu-id="27cad-139">-Config</span></span>
<span data-ttu-id="27cad-140">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="27cad-141">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="27cad-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-142">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="27cad-142">-Configurations</span></span>
<span data-ttu-id="27cad-143">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="27cad-144">Alternatif olarak Add-AzureRmHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="27cad-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cad-145">-DefaultProfile</span></span>
<span data-ttu-id="27cad-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="27cad-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27cad-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="27cad-148">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="27cad-149">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27cad-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="27cad-151">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="27cad-152">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="27cad-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="27cad-154">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="27cad-155">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="27cad-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="27cad-156">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="27cad-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="27cad-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="27cad-158">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="27cad-159">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="27cad-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="27cad-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="27cad-161">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="27cad-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="27cad-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="27cad-163">Kümedeki çalışan düğümü rolü için disk sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="27cad-164">-EdgeNodeSize</span></span>
<span data-ttu-id="27cad-165">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="27cad-166">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="27cad-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="27cad-167">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="27cad-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="27cad-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="27cad-168">-HeadNodeSize</span></span>
<span data-ttu-id="27cad-169">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="27cad-170">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="27cad-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="27cad-171">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="27cad-171">-HiveMetastore</span></span>
<span data-ttu-id="27cad-172">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="27cad-173">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="27cad-174">-HttpCredential</span></span>
<span data-ttu-id="27cad-175">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-176">-Konum</span><span class="sxs-lookup"><span data-stu-id="27cad-176">-Location</span></span>
<span data-ttu-id="27cad-177">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-177">Specifies the location for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-178">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="27cad-178">-ObjectId</span></span>
<span data-ttu-id="27cad-179">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="27cad-180">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27cad-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-181">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="27cad-181">-OozieMetastore</span></span>
<span data-ttu-id="27cad-182">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="27cad-183">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="27cad-184">-OSType</span></span>
<span data-ttu-id="27cad-185">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="27cad-186">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="27cad-186">Options are: Windows, Linux</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-187">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="27cad-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="27cad-188">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="27cad-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="27cad-189">-RdpCredential</span></span>
<span data-ttu-id="27cad-190">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="27cad-191">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="27cad-191">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27cad-192">-ResourceGroupName</span></span>
<span data-ttu-id="27cad-193">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-193">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-194">-Betikler</span><span class="sxs-lookup"><span data-stu-id="27cad-194">-ScriptActions</span></span>
<span data-ttu-id="27cad-195">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="27cad-196">Alternatif olarak Add-AzureRmHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="27cad-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="27cad-197">-SecurityProfile</span></span>
<span data-ttu-id="27cad-198">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="27cad-199">Alternatif olarak Add-AzureRmHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27cad-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="27cad-200">-SshCredential</span></span>
<span data-ttu-id="27cad-201">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="27cad-202">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="27cad-202">This is only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cad-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="27cad-203">-SshPublicKey</span></span>
<span data-ttu-id="27cad-204">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="27cad-205">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="27cad-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="27cad-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="27cad-206">-SubnetName</span></span>
<span data-ttu-id="27cad-207">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="27cad-208">-Version</span><span class="sxs-lookup"><span data-stu-id="27cad-208">-Version</span></span>
<span data-ttu-id="27cad-209">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="27cad-210">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="27cad-210">-VirtualNetworkId</span></span>
<span data-ttu-id="27cad-211">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="27cad-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="27cad-212">-WorkerNodeSize</span></span>
<span data-ttu-id="27cad-213">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="27cad-214">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="27cad-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="27cad-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="27cad-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="27cad-216">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cad-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="27cad-217">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="27cad-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="27cad-218">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="27cad-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="27cad-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cad-219">CommonParameters</span></span>
<span data-ttu-id="27cad-220">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27cad-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cad-221">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27cad-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cad-222">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27cad-222">INPUTS</span></span>

### <span data-ttu-id="27cad-223">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="27cad-223">AzureHDInsightConfig</span></span>
<span data-ttu-id="27cad-224">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="27cad-224">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="27cad-225">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27cad-225">OUTPUTS</span></span>

### <span data-ttu-id="27cad-226">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="27cad-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="27cad-227">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27cad-227">NOTES</span></span>
<span data-ttu-id="27cad-228">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="27cad-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="27cad-229">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27cad-229">RELATED LINKS</span></span>

[<span data-ttu-id="27cad-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="27cad-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

