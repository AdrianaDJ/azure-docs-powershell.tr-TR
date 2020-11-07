---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938495"
---
# <span data-ttu-id="2cdd0-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2cdd0-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="2cdd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdd0-103">Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="2cdd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cdd0-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cdd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cdd0-105">DESCRIPTION</span></span>
<span data-ttu-id="2cdd0-106">**New-AzHDInsightClusterConfig** cmdlet 'i, bir Azure HDInsight küme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="2cdd0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cdd0-107">EXAMPLES</span></span>

### <span data-ttu-id="2cdd0-108">Örnek 1: küme yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2cdd0-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="2cdd0-109">Bu komut, bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="2cdd0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cdd0-110">PARAMETERS</span></span>

### <span data-ttu-id="2cdd0-111">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="2cdd0-111">-AadTenantId</span></span>
<span data-ttu-id="2cdd0-112">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2cdd0-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2cdd0-113">-ApplicationId</span></span>
<span data-ttu-id="2cdd0-114">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="2cdd0-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="2cdd0-115">-CertificateFileContents</span></span>
<span data-ttu-id="2cdd0-116">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdd0-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="2cdd0-117">-CertificateFilePath</span></span>
<span data-ttu-id="2cdd0-118">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2cdd0-119">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2cdd0-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2cdd0-120">-CertificatePassword</span></span>
<span data-ttu-id="2cdd0-121">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2cdd0-122">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2cdd0-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="2cdd0-123">-ClusterTier</span></span>
<span data-ttu-id="2cdd0-124">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="2cdd0-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2cdd0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2cdd0-126">Ardından</span><span class="sxs-lookup"><span data-stu-id="2cdd0-126">Standard</span></span>
- <span data-ttu-id="2cdd0-127">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="2cdd0-128">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="2cdd0-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2cdd0-129">-ClusterType</span></span>
<span data-ttu-id="2cdd0-130">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="2cdd0-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2cdd0-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2cdd0-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="2cdd0-132">Hadoop</span></span>
- <span data-ttu-id="2cdd0-133">HBase</span><span class="sxs-lookup"><span data-stu-id="2cdd0-133">HBase</span></span>
- <span data-ttu-id="2cdd0-134">Fırtınası</span><span class="sxs-lookup"><span data-stu-id="2cdd0-134">Storm</span></span>
- <span data-ttu-id="2cdd0-135">Artırmak</span><span class="sxs-lookup"><span data-stu-id="2cdd0-135">Spark</span></span>
- <span data-ttu-id="2cdd0-136">INTERACTIVEKOVANı</span><span class="sxs-lookup"><span data-stu-id="2cdd0-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="2cdd0-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="2cdd0-137">Kafka</span></span>
- <span data-ttu-id="2cdd0-138">RServer</span><span class="sxs-lookup"><span data-stu-id="2cdd0-138">RServer</span></span>

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

### <span data-ttu-id="2cdd0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdd0-139">-DefaultProfile</span></span>
<span data-ttu-id="2cdd0-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2cdd0-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cdd0-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2cdd0-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="2cdd0-142">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="2cdd0-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2cdd0-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="2cdd0-144">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="2cdd0-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2cdd0-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="2cdd0-146">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="2cdd0-147">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdd0-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="2cdd0-148">-EdgeNodeSize</span></span>
<span data-ttu-id="2cdd0-149">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="2cdd0-150">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="2cdd0-151">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="2cdd0-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="2cdd0-152">-HeadNodeSize</span></span>
<span data-ttu-id="2cdd0-153">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="2cdd0-154">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="2cdd0-155">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="2cdd0-155">-HiveMetastore</span></span>
<span data-ttu-id="2cdd0-156">Kovan meta verilerini depolamak için metasarı 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="2cdd0-157">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="2cdd0-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2cdd0-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="2cdd0-159">Desteklenen en düşük TLS sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="2cdd0-160">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="2cdd0-160">-ObjectId</span></span>
<span data-ttu-id="2cdd0-161">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="2cdd0-162">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2cdd0-163">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="2cdd0-163">-OozieMetastore</span></span>
<span data-ttu-id="2cdd0-164">Oozie meta verilerini depolamak için metaser 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="2cdd0-165">Alternatif olarak **Add-AzHDInsightMetastore** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="2cdd0-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="2cdd0-166">-WorkerNodeSize</span></span>
<span data-ttu-id="2cdd0-167">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="2cdd0-168">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="2cdd0-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="2cdd0-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="2cdd0-170">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="2cdd0-171">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="2cdd0-172">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="2cdd0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdd0-173">CommonParameters</span></span>
<span data-ttu-id="2cdd0-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdd0-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2cdd0-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdd0-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cdd0-176">INPUTS</span></span>

### <span data-ttu-id="2cdd0-177">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2cdd0-177">None</span></span>

## <span data-ttu-id="2cdd0-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cdd0-178">OUTPUTS</span></span>

### <span data-ttu-id="2cdd0-179">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2cdd0-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2cdd0-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cdd0-180">NOTES</span></span>

## <span data-ttu-id="2cdd0-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cdd0-181">RELATED LINKS</span></span>

[<span data-ttu-id="2cdd0-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="2cdd0-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


