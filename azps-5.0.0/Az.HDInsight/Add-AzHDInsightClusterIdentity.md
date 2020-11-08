---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 4d791faf320285e5392eb9edd523447df02c1984
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275399"
---
# <span data-ttu-id="1048b-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="1048b-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="1048b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1048b-102">SYNOPSIS</span></span>
<span data-ttu-id="1048b-103">Küme yapılandırma nesnesine küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="1048b-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="1048b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1048b-104">SYNTAX</span></span>

### <span data-ttu-id="1048b-105">CertificateFilePath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1048b-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1048b-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1048b-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1048b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1048b-107">DESCRIPTION</span></span>
<span data-ttu-id="1048b-108">**Add-AzHDInsightClusterIdentity** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine bir küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="1048b-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="1048b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1048b-109">EXAMPLES</span></span>

### <span data-ttu-id="1048b-110">Örnek 1: küme yapılandırma nesnesine küme kimliği bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="1048b-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="1048b-111">Bu komut, kümenin Azure Data Lake Store 'a erişmesine izin vererek-Hadoop-001 adlı kümeye küme kimliği bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="1048b-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="1048b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1048b-112">PARAMETERS</span></span>

### <span data-ttu-id="1048b-113">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="1048b-113">-AadTenantId</span></span>
<span data-ttu-id="1048b-114">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1048b-115">-ApplicationId</span></span>
<span data-ttu-id="1048b-116">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="1048b-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="1048b-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1048b-117">-CertificateFileContents</span></span>
<span data-ttu-id="1048b-118">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1048b-119">-CertificateFilePath</span></span>
<span data-ttu-id="1048b-120">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1048b-121">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1048b-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1048b-122">-CertificatePassword</span></span>
<span data-ttu-id="1048b-123">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1048b-124">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1048b-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-125">-Config</span><span class="sxs-lookup"><span data-stu-id="1048b-125">-Config</span></span>
<span data-ttu-id="1048b-126">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="1048b-127">Bu nesne New-AzHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1048b-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1048b-128">-DefaultProfile</span></span>
<span data-ttu-id="1048b-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1048b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1048b-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="1048b-130">-ObjectId</span></span>
<span data-ttu-id="1048b-131">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="1048b-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="1048b-132">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1048b-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1048b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1048b-133">CommonParameters</span></span>
<span data-ttu-id="1048b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1048b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1048b-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1048b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1048b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1048b-136">INPUTS</span></span>

### <span data-ttu-id="1048b-137">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1048b-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="1048b-138">System. Guid</span><span class="sxs-lookup"><span data-stu-id="1048b-138">System.Guid</span></span>

## <span data-ttu-id="1048b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1048b-139">OUTPUTS</span></span>

### <span data-ttu-id="1048b-140">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1048b-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1048b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1048b-141">NOTES</span></span>

## <span data-ttu-id="1048b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1048b-142">RELATED LINKS</span></span>

[<span data-ttu-id="1048b-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1048b-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


