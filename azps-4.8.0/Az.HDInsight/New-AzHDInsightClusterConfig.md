---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109075"
---
# <span data-ttu-id="4a5da-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4a5da-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="4a5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a5da-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5da-103">Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a5da-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4a5da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a5da-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a5da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a5da-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5da-106">**New-AzHDInsightClusterConfig** cmdlet 'i, bir Azure HDInsight küme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a5da-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="4a5da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a5da-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5da-108">Örnek 1: küme yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4a5da-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="4a5da-109">Bu komut, bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a5da-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="4a5da-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a5da-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5da-111">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="4a5da-111">-AadTenantId</span></span>
<span data-ttu-id="4a5da-112">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4a5da-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4a5da-113">-ApplicationId</span></span>
<span data-ttu-id="4a5da-114">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="4a5da-115">-Atandıdentity</span><span class="sxs-lookup"><span data-stu-id="4a5da-115">-AssignedIdentity</span></span>
<span data-ttu-id="4a5da-116">Atanan kimliği alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="4a5da-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4a5da-117">-CertificateFileContents</span></span>
<span data-ttu-id="4a5da-118">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4a5da-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4a5da-119">-CertificateFilePath</span></span>
<span data-ttu-id="4a5da-120">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4a5da-121">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a5da-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4a5da-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4a5da-122">-CertificatePassword</span></span>
<span data-ttu-id="4a5da-123">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4a5da-124">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a5da-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4a5da-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4a5da-125">-ClusterTier</span></span>
<span data-ttu-id="4a5da-126">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4a5da-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4a5da-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a5da-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="4a5da-128">Standard</span></span>
- <span data-ttu-id="4a5da-129">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="4a5da-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="4a5da-130">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="4a5da-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="4a5da-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4a5da-131">-ClusterType</span></span>
<span data-ttu-id="4a5da-132">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4a5da-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4a5da-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a5da-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="4a5da-134">Hadoop</span></span>
- <span data-ttu-id="4a5da-135">HBase</span><span class="sxs-lookup"><span data-stu-id="4a5da-135">HBase</span></span>
- <span data-ttu-id="4a5da-136">Fırtınası</span><span class="sxs-lookup"><span data-stu-id="4a5da-136">Storm</span></span>
- <span data-ttu-id="4a5da-137">Artırmak</span><span class="sxs-lookup"><span data-stu-id="4a5da-137">Spark</span></span>
- <span data-ttu-id="4a5da-138">INTERACTIVEKOVANı</span><span class="sxs-lookup"><span data-stu-id="4a5da-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="4a5da-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="4a5da-139">Kafka</span></span>
- <span data-ttu-id="4a5da-140">RServer</span><span class="sxs-lookup"><span data-stu-id="4a5da-140">RServer</span></span>

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

### <span data-ttu-id="4a5da-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5da-141">-DefaultProfile</span></span>
<span data-ttu-id="4a5da-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4a5da-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a5da-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4a5da-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4a5da-144">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="4a5da-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a5da-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4a5da-146">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="4a5da-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4a5da-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4a5da-148">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4a5da-149">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4a5da-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="4a5da-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4a5da-150">-EdgeNodeSize</span></span>
<span data-ttu-id="4a5da-151">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4a5da-152">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4a5da-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4a5da-153">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4a5da-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4a5da-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="4a5da-155">Şifreleme algoritmasını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-155">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a5da-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4a5da-156">-EncryptionAtHost</span></span>
<span data-ttu-id="4a5da-157">Ana bilgisayarda şifrelemeyi etkinleştirip etkinleştirmeyeceğinizi belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a5da-158">-Şifrelememe</span><span class="sxs-lookup"><span data-stu-id="4a5da-158">-EncryptionInTransit</span></span>
<span data-ttu-id="4a5da-159">İletimde şifrelemeyi etkinleştir 'in etkin olup olmadığını belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a5da-160">-Encryptionanahtaradı</span><span class="sxs-lookup"><span data-stu-id="4a5da-160">-EncryptionKeyName</span></span>
<span data-ttu-id="4a5da-161">Şifreleme anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="4a5da-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4a5da-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="4a5da-163">Şifreleme anahtarı sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="4a5da-164">-Şifrelemem</span><span class="sxs-lookup"><span data-stu-id="4a5da-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="4a5da-165">Şifreleme Kasası URI 'sini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="4a5da-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4a5da-166">-HeadNodeSize</span></span>
<span data-ttu-id="4a5da-167">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4a5da-168">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4a5da-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4a5da-169">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="4a5da-169">-HiveMetastore</span></span>
<span data-ttu-id="4a5da-170">Kovan meta verilerini depolamak için metasarı 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="4a5da-171">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a5da-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4a5da-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4a5da-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="4a5da-173">Desteklenen en düşük TLS sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="4a5da-174">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4a5da-174">-ObjectId</span></span>
<span data-ttu-id="4a5da-175">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4a5da-176">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a5da-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4a5da-177">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="4a5da-177">-OozieMetastore</span></span>
<span data-ttu-id="4a5da-178">Oozie meta verilerini depolamak için metaser 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="4a5da-179">Alternatif olarak **Add-AzHDInsightMetastore** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a5da-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="4a5da-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4a5da-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="4a5da-181">Giden erişim türünü genel ağa alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-181">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a5da-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4a5da-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="4a5da-183">Genel ağ erişim türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a5da-183">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a5da-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4a5da-184">-WorkerNodeSize</span></span>
<span data-ttu-id="4a5da-185">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4a5da-186">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4a5da-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4a5da-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4a5da-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4a5da-188">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4a5da-189">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4a5da-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4a5da-190">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4a5da-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4a5da-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5da-191">CommonParameters</span></span>
<span data-ttu-id="4a5da-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a5da-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5da-193">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a5da-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5da-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a5da-194">INPUTS</span></span>

### <span data-ttu-id="4a5da-195">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4a5da-195">None</span></span>

## <span data-ttu-id="4a5da-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a5da-196">OUTPUTS</span></span>

### <span data-ttu-id="4a5da-197">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4a5da-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4a5da-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a5da-198">NOTES</span></span>

## <span data-ttu-id="4a5da-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a5da-199">RELATED LINKS</span></span>

[<span data-ttu-id="4a5da-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="4a5da-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


