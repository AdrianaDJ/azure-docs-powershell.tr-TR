---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: e4588f3799052cf9f397f846b635be4f525df930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590257"
---
# <span data-ttu-id="c6f3c-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c6f3c-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="c6f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f3c-103">Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6f3c-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f3c-106">**New-AzureRmHDInsightClusterConfig** cmdlet 'i, bir Azure HDInsight küme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c6f3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f3c-108">Örnek 1: küme yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6f3c-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="c6f3c-109">Bu komut, bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="c6f3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="c6f3c-111">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="c6f3c-111">-AadTenantId</span></span>
<span data-ttu-id="c6f3c-112">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c6f3c-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c6f3c-113">-CertificateFileContents</span></span>
<span data-ttu-id="c6f3c-114">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c6f3c-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c6f3c-115">-CertificateFilePath</span></span>
<span data-ttu-id="c6f3c-116">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c6f3c-117">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c6f3c-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c6f3c-118">-CertificatePassword</span></span>
<span data-ttu-id="c6f3c-119">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c6f3c-120">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c6f3c-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c6f3c-121">-ClusterTier</span></span>
<span data-ttu-id="c6f3c-122">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c6f3c-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6f3c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6f3c-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="c6f3c-124">Standard</span></span>
- <span data-ttu-id="c6f3c-125">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="c6f3c-126">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c6f3c-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="c6f3c-127">-ClusterType</span></span>
<span data-ttu-id="c6f3c-128">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c6f3c-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6f3c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6f3c-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="c6f3c-130">Hadoop</span></span>
- <span data-ttu-id="c6f3c-131">HBase</span><span class="sxs-lookup"><span data-stu-id="c6f3c-131">HBase</span></span>
- <span data-ttu-id="c6f3c-132">Fırtınası</span><span class="sxs-lookup"><span data-stu-id="c6f3c-132">Storm</span></span>
- <span data-ttu-id="c6f3c-133">Artırmak</span><span class="sxs-lookup"><span data-stu-id="c6f3c-133">Spark</span></span>

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

### <span data-ttu-id="c6f3c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f3c-134">-DefaultProfile</span></span>
<span data-ttu-id="c6f3c-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6f3c-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6f3c-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c6f3c-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c6f3c-137">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="c6f3c-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c6f3c-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c6f3c-139">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="c6f3c-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c6f3c-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="c6f3c-141">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="c6f3c-142">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="c6f3c-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c6f3c-143">-EdgeNodeSize</span></span>
<span data-ttu-id="c6f3c-144">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c6f3c-145">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-145">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c6f3c-146">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c6f3c-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c6f3c-147">-HeadNodeSize</span></span>
<span data-ttu-id="c6f3c-148">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c6f3c-149">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-149">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c6f3c-150">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="c6f3c-150">-HiveMetastore</span></span>
<span data-ttu-id="c6f3c-151">Kovan meta verilerini depolamak için metasarı 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="c6f3c-152">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-152">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c6f3c-153">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c6f3c-153">-ObjectId</span></span>
<span data-ttu-id="c6f3c-154">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c6f3c-155">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c6f3c-156">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="c6f3c-156">-OozieMetastore</span></span>
<span data-ttu-id="c6f3c-157">Oozie meta verilerini depolamak için metaser 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="c6f3c-158">Alternatif olarak **Add-AzureRmHDInsightMetastore** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-158">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="c6f3c-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c6f3c-159">-WorkerNodeSize</span></span>
<span data-ttu-id="c6f3c-160">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c6f3c-161">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-161">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c6f3c-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c6f3c-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c6f3c-163">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c6f3c-164">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-164">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c6f3c-165">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c6f3c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f3c-166">CommonParameters</span></span>
<span data-ttu-id="c6f3c-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6f3c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f3c-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f3c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f3c-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6f3c-169">INPUTS</span></span>

### <span data-ttu-id="c6f3c-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c6f3c-170">None</span></span>

## <span data-ttu-id="c6f3c-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6f3c-171">OUTPUTS</span></span>

### <span data-ttu-id="c6f3c-172">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c6f3c-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c6f3c-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6f3c-173">NOTES</span></span>

## <span data-ttu-id="c6f3c-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6f3c-174">RELATED LINKS</span></span>

[<span data-ttu-id="c6f3c-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c6f3c-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


