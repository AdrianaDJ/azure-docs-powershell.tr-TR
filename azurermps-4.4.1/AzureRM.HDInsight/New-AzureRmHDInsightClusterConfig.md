---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594690"
---
# <span data-ttu-id="e3416-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3416-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="e3416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3416-102">SYNOPSIS</span></span>
<span data-ttu-id="e3416-103">Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3416-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3416-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3416-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3416-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3416-105">DESCRIPTION</span></span>
<span data-ttu-id="e3416-106">**New-AzureRmHDInsightClusterConfig** cmdlet 'i, bir Azure HDInsight küme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3416-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e3416-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3416-107">EXAMPLES</span></span>

### <span data-ttu-id="e3416-108">Örnek 1: küme yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3416-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="e3416-109">Bu komut, bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3416-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="e3416-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3416-110">PARAMETERS</span></span>

### <span data-ttu-id="e3416-111">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="e3416-111">-AadTenantId</span></span>
<span data-ttu-id="e3416-112">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3416-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e3416-113">-CertificateFileContents</span></span>
<span data-ttu-id="e3416-114">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3416-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e3416-115">-CertificateFilePath</span></span>
<span data-ttu-id="e3416-116">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3416-117">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3416-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3416-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e3416-118">-CertificatePassword</span></span>
<span data-ttu-id="e3416-119">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3416-120">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3416-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3416-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e3416-121">-ClusterTier</span></span>
<span data-ttu-id="e3416-122">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e3416-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e3416-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3416-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="e3416-124">Standard</span></span>
- <span data-ttu-id="e3416-125">Min</span><span class="sxs-lookup"><span data-stu-id="e3416-125">Premium</span></span>

<span data-ttu-id="e3416-126">Varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="e3416-126">The default value is Standard.</span></span>
<span data-ttu-id="e3416-127">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="e3416-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="e3416-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e3416-128">-ClusterType</span></span>
<span data-ttu-id="e3416-129">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e3416-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e3416-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3416-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="e3416-131">Hadoop</span></span>
- <span data-ttu-id="e3416-132">HBase</span><span class="sxs-lookup"><span data-stu-id="e3416-132">HBase</span></span>
- <span data-ttu-id="e3416-133">Fırtınası</span><span class="sxs-lookup"><span data-stu-id="e3416-133">Storm</span></span>
- <span data-ttu-id="e3416-134">Artırmak</span><span class="sxs-lookup"><span data-stu-id="e3416-134">Spark</span></span>

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

### <span data-ttu-id="e3416-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e3416-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="e3416-136">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="e3416-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3416-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="e3416-138">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="e3416-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e3416-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="e3416-140">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="e3416-141">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="e3416-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="e3416-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3416-142">-EdgeNodeSize</span></span>
<span data-ttu-id="e3416-143">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e3416-144">Kabul edilebilir VM boyutlarında Get-AzureRmVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="e3416-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e3416-145">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e3416-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e3416-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3416-146">-HeadNodeSize</span></span>
<span data-ttu-id="e3416-147">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e3416-148">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="e3416-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e3416-149">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="e3416-149">-HiveMetastore</span></span>
<span data-ttu-id="e3416-150">Kovan meta verilerini depolamak için metasarı 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="e3416-151">Alternatif olarak Add-AzureRmHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3416-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e3416-152">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e3416-152">-ObjectId</span></span>
<span data-ttu-id="e3416-153">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e3416-154">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3416-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e3416-155">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="e3416-155">-OozieMetastore</span></span>
<span data-ttu-id="e3416-156">Oozie meta verilerini depolamak için metaser 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="e3416-157">Alternatif olarak **Add-AzureRmHDInsightMetastore** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3416-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="e3416-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3416-158">-WorkerNodeSize</span></span>
<span data-ttu-id="e3416-159">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e3416-160">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="e3416-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e3416-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e3416-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e3416-162">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3416-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e3416-163">Kabul edilebilir VM boyutlarında Get-AzureRMVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="e3416-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e3416-164">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e3416-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e3416-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3416-165">-DefaultProfile</span></span>
<span data-ttu-id="e3416-166">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3416-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3416-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3416-167">CommonParameters</span></span>
<span data-ttu-id="e3416-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3416-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3416-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3416-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3416-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3416-170">INPUTS</span></span>

## <span data-ttu-id="e3416-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3416-171">OUTPUTS</span></span>

### <span data-ttu-id="e3416-172">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e3416-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e3416-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3416-173">NOTES</span></span>

## <span data-ttu-id="e3416-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3416-174">RELATED LINKS</span></span>

[<span data-ttu-id="e3416-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e3416-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


