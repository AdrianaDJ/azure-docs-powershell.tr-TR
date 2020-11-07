---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764845"
---
# <span data-ttu-id="6856b-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6856b-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="6856b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6856b-102">SYNOPSIS</span></span>
<span data-ttu-id="6856b-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6856b-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6856b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6856b-104">SYNTAX</span></span>

### <span data-ttu-id="6856b-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6856b-105">Default (Default)</span></span>
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
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6856b-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6856b-106">CertificateFilePath</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6856b-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6856b-107">CertificateFileContents</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6856b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6856b-108">DESCRIPTION</span></span>
<span data-ttu-id="6856b-109">New-AzureHDInsightCluster belirtilen parametreleri kullanarak veya New-AzureRmHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6856b-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="6856b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6856b-110">EXAMPLES</span></span>

### <span data-ttu-id="6856b-111">--------------------------Örnek 1: Azure HDInsight kümesi oluşturma--------------------------</span><span class="sxs-lookup"><span data-stu-id="6856b-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="6856b-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6856b-112">@{paragraph=PS C:\\\>}</span></span>









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

<span data-ttu-id="6856b-113">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6856b-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="6856b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6856b-114">PARAMETERS</span></span>

### <span data-ttu-id="6856b-115">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="6856b-115">-AadTenantId</span></span>
<span data-ttu-id="6856b-116">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6856b-117">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="6856b-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="6856b-118">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="6856b-119">Alternatif olarak Add-AzureRmHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="6856b-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="6856b-120">-CertificateFileContents</span></span>
<span data-ttu-id="6856b-121">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6856b-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6856b-122">-CertificateFilePath</span></span>
<span data-ttu-id="6856b-123">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6856b-124">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6856b-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6856b-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6856b-125">-CertificatePassword</span></span>
<span data-ttu-id="6856b-126">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="6856b-127">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6856b-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6856b-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6856b-128">-ClusterName</span></span>
<span data-ttu-id="6856b-129">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-129">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6856b-130">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="6856b-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="6856b-131">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-131">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="6856b-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="6856b-132">-ClusterTier</span></span>
<span data-ttu-id="6856b-133">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="6856b-134">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="6856b-134">By default, this is Standard.</span></span>
<span data-ttu-id="6856b-135">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="6856b-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="6856b-136">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="6856b-136">-ClusterType</span></span>
<span data-ttu-id="6856b-137">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="6856b-138">Seçenekler: Hadoop, HBase, fırtınası, Spark</span><span class="sxs-lookup"><span data-stu-id="6856b-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="6856b-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="6856b-139">-ComponentVersion</span></span>
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

### <span data-ttu-id="6856b-140">-Config</span><span class="sxs-lookup"><span data-stu-id="6856b-140">-Config</span></span>
<span data-ttu-id="6856b-141">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="6856b-142">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="6856b-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="6856b-143">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="6856b-143">-Configurations</span></span>
<span data-ttu-id="6856b-144">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="6856b-145">Alternatif olarak Add-AzureRmHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="6856b-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6856b-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="6856b-147">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6856b-148">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6856b-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6856b-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="6856b-150">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6856b-151">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6856b-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6856b-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="6856b-153">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="6856b-154">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="6856b-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="6856b-155">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="6856b-155">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="6856b-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6856b-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="6856b-157">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="6856b-158">Alternatif olarak Set-AzureRmHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="6856b-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="6856b-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="6856b-160">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="6856b-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="6856b-161">-EdgeNodeSize</span></span>
<span data-ttu-id="6856b-162">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="6856b-163">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="6856b-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="6856b-164">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6856b-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="6856b-165">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="6856b-165">-HeadNodeSize</span></span>
<span data-ttu-id="6856b-166">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="6856b-167">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="6856b-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="6856b-168">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="6856b-168">-HiveMetastore</span></span>
<span data-ttu-id="6856b-169">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="6856b-170">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="6856b-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="6856b-171">-HttpCredential</span></span>
<span data-ttu-id="6856b-172">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="6856b-173">-Konum</span><span class="sxs-lookup"><span data-stu-id="6856b-173">-Location</span></span>
<span data-ttu-id="6856b-174">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-174">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="6856b-175">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="6856b-175">-ObjectId</span></span>
<span data-ttu-id="6856b-176">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="6856b-177">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6856b-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="6856b-178">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="6856b-178">-OozieMetastore</span></span>
<span data-ttu-id="6856b-179">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="6856b-180">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="6856b-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="6856b-181">-OSType</span></span>
<span data-ttu-id="6856b-182">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="6856b-183">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="6856b-183">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="6856b-184">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="6856b-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="6856b-185">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="6856b-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="6856b-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6856b-186">-RdpCredential</span></span>
<span data-ttu-id="6856b-187">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="6856b-188">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="6856b-188">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="6856b-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6856b-189">-ResourceGroupName</span></span>
<span data-ttu-id="6856b-190">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-190">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6856b-191">-Betikler</span><span class="sxs-lookup"><span data-stu-id="6856b-191">-ScriptActions</span></span>
<span data-ttu-id="6856b-192">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="6856b-193">Alternatif olarak Add-AzureRmHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="6856b-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="6856b-194">-SecurityProfile</span></span>
<span data-ttu-id="6856b-195">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="6856b-196">Alternatif olarak Add-AzureRmHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6856b-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="6856b-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="6856b-197">-SshCredential</span></span>
<span data-ttu-id="6856b-198">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="6856b-199">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="6856b-199">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="6856b-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6856b-200">-SshPublicKey</span></span>
<span data-ttu-id="6856b-201">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="6856b-202">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="6856b-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="6856b-203">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6856b-203">-SubnetName</span></span>
<span data-ttu-id="6856b-204">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="6856b-205">-Version</span><span class="sxs-lookup"><span data-stu-id="6856b-205">-Version</span></span>
<span data-ttu-id="6856b-206">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="6856b-207">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="6856b-207">-VirtualNetworkId</span></span>
<span data-ttu-id="6856b-208">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="6856b-209">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="6856b-209">-WorkerNodeSize</span></span>
<span data-ttu-id="6856b-210">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="6856b-211">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="6856b-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="6856b-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="6856b-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="6856b-213">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6856b-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="6856b-214">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="6856b-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="6856b-215">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6856b-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="6856b-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6856b-216">-DefaultProfile</span></span>
<span data-ttu-id="6856b-217">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6856b-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6856b-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6856b-218">CommonParameters</span></span>
<span data-ttu-id="6856b-219">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6856b-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6856b-220">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6856b-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6856b-221">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6856b-221">INPUTS</span></span>

### <span data-ttu-id="6856b-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6856b-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="6856b-223">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6856b-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="6856b-224">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6856b-224">OUTPUTS</span></span>

### <span data-ttu-id="6856b-225">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6856b-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="6856b-226">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6856b-226">NOTES</span></span>
<span data-ttu-id="6856b-227">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="6856b-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="6856b-228">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6856b-228">RELATED LINKS</span></span>

[<span data-ttu-id="6856b-229">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6856b-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

