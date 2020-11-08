---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277841"
---
# <span data-ttu-id="8a47b-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8a47b-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="8a47b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a47b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a47b-103">Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a47b-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8a47b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a47b-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a47b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a47b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a47b-106">**New-AzHDInsightClusterConfig** cmdlet 'i, bir Azure HDInsight küme yapılandırmasını açıklayan kalıcı olmayan bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a47b-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8a47b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a47b-107">EXAMPLES</span></span>

### <span data-ttu-id="8a47b-108">Örnek 1: küme yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a47b-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="8a47b-109">Bu komut, bir küme yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a47b-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="8a47b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a47b-110">PARAMETERS</span></span>

### <span data-ttu-id="8a47b-111">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="8a47b-111">-AadTenantId</span></span>
<span data-ttu-id="8a47b-112">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8a47b-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8a47b-113">-ApplicationId</span></span>
<span data-ttu-id="8a47b-114">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="8a47b-115">-Atandıdentity</span><span class="sxs-lookup"><span data-stu-id="8a47b-115">-AssignedIdentity</span></span>
<span data-ttu-id="8a47b-116">Atanan kimliği alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="8a47b-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8a47b-117">-CertificateFileContents</span></span>
<span data-ttu-id="8a47b-118">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8a47b-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8a47b-119">-CertificateFilePath</span></span>
<span data-ttu-id="8a47b-120">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8a47b-121">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8a47b-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8a47b-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8a47b-122">-CertificatePassword</span></span>
<span data-ttu-id="8a47b-123">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8a47b-124">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8a47b-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8a47b-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="8a47b-125">-ClusterTier</span></span>
<span data-ttu-id="8a47b-126">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="8a47b-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a47b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a47b-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="8a47b-128">Standard</span></span>
- <span data-ttu-id="8a47b-129">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="8a47b-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="8a47b-130">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="8a47b-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="8a47b-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8a47b-131">-ClusterType</span></span>
<span data-ttu-id="8a47b-132">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="8a47b-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a47b-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a47b-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="8a47b-134">Hadoop</span></span>
- <span data-ttu-id="8a47b-135">HBase</span><span class="sxs-lookup"><span data-stu-id="8a47b-135">HBase</span></span>
- <span data-ttu-id="8a47b-136">Fırtınası</span><span class="sxs-lookup"><span data-stu-id="8a47b-136">Storm</span></span>
- <span data-ttu-id="8a47b-137">Artırmak</span><span class="sxs-lookup"><span data-stu-id="8a47b-137">Spark</span></span>
- <span data-ttu-id="8a47b-138">INTERACTIVEKOVANı</span><span class="sxs-lookup"><span data-stu-id="8a47b-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="8a47b-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="8a47b-139">Kafka</span></span>
- <span data-ttu-id="8a47b-140">RServer</span><span class="sxs-lookup"><span data-stu-id="8a47b-140">RServer</span></span>

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

### <span data-ttu-id="8a47b-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a47b-141">-DefaultProfile</span></span>
<span data-ttu-id="8a47b-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8a47b-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a47b-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="8a47b-143">-EdgeNodeSize</span></span>
<span data-ttu-id="8a47b-144">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="8a47b-145">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="8a47b-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="8a47b-146">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="8a47b-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8a47b-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="8a47b-148">Şifreleme algoritmasını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="8a47b-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="8a47b-149">-EncryptionAtHost</span></span>
<span data-ttu-id="8a47b-150">Ana bilgisayarda şifrelemeyi etkinleştirip etkinleştirmeyeceğinizi belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="8a47b-151">-Şifrelememe</span><span class="sxs-lookup"><span data-stu-id="8a47b-151">-EncryptionInTransit</span></span>
<span data-ttu-id="8a47b-152">İletimde şifrelemeyi etkinleştir 'in etkin olup olmadığını belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="8a47b-153">-Encryptionanahtaradı</span><span class="sxs-lookup"><span data-stu-id="8a47b-153">-EncryptionKeyName</span></span>
<span data-ttu-id="8a47b-154">Şifreleme anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="8a47b-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8a47b-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="8a47b-156">Şifreleme anahtarı sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="8a47b-157">-Şifrelemem</span><span class="sxs-lookup"><span data-stu-id="8a47b-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="8a47b-158">Şifreleme Kasası URI 'sini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="8a47b-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="8a47b-159">-HeadNodeSize</span></span>
<span data-ttu-id="8a47b-160">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="8a47b-161">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="8a47b-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8a47b-162">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="8a47b-162">-HiveMetastore</span></span>
<span data-ttu-id="8a47b-163">Kovan meta verilerini depolamak için metasarı 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="8a47b-164">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a47b-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="8a47b-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8a47b-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="8a47b-166">Desteklenen en düşük TLS sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="8a47b-167">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8a47b-167">-ObjectId</span></span>
<span data-ttu-id="8a47b-168">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="8a47b-169">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8a47b-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8a47b-170">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="8a47b-170">-OozieMetastore</span></span>
<span data-ttu-id="8a47b-171">Oozie meta verilerini depolamak için metaser 'ı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="8a47b-172">Alternatif olarak **Add-AzHDInsightMetastore** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a47b-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="8a47b-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8a47b-173">-StorageAccountKey</span></span>
<span data-ttu-id="8a47b-174">Depolama hesabı erişim anahtarını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="8a47b-175">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="8a47b-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="8a47b-176">Depolama hesabı kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="8a47b-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8a47b-177">-StorageAccountType</span></span>
<span data-ttu-id="8a47b-178">Varsayılan depolama hesabının türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8a47b-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a47b-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="8a47b-179">-WorkerNodeSize</span></span>
<span data-ttu-id="8a47b-180">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="8a47b-181">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="8a47b-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8a47b-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="8a47b-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="8a47b-183">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="8a47b-184">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="8a47b-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="8a47b-185">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="8a47b-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="8a47b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a47b-186">CommonParameters</span></span>
<span data-ttu-id="8a47b-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a47b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a47b-188">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8a47b-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a47b-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a47b-189">INPUTS</span></span>

### <span data-ttu-id="8a47b-190">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a47b-190">None</span></span>

## <span data-ttu-id="8a47b-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a47b-191">OUTPUTS</span></span>

### <span data-ttu-id="8a47b-192">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8a47b-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8a47b-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a47b-193">NOTES</span></span>

## <span data-ttu-id="8a47b-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a47b-194">RELATED LINKS</span></span>

[<span data-ttu-id="8a47b-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="8a47b-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


