---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 035b21684c3d8fc64cee7ee78b7b4cb2adf21f01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751865"
---
# <span data-ttu-id="99d9e-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="99d9e-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="99d9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="99d9e-103">Küme yapılandırma nesnesine küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="99d9e-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="99d9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99d9e-104">SYNTAX</span></span>

### <span data-ttu-id="99d9e-105">CertificateFilePath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99d9e-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d9e-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="99d9e-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d9e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99d9e-107">DESCRIPTION</span></span>
<span data-ttu-id="99d9e-108">**Add-AzHDInsightClusterIdentity** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine bir küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="99d9e-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="99d9e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99d9e-109">EXAMPLES</span></span>

### <span data-ttu-id="99d9e-110">Örnek 1: küme yapılandırma nesnesine küme kimliği bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="99d9e-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="99d9e-111">Bu komut, kümenin Azure Data Lake Store 'a erişmesine izin vererek-Hadoop-001 adlı kümeye küme kimliği bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="99d9e-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="99d9e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99d9e-112">PARAMETERS</span></span>

### <span data-ttu-id="99d9e-113">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="99d9e-113">-AadTenantId</span></span>
<span data-ttu-id="99d9e-114">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99d9e-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="99d9e-115">-CertificateFileContents</span></span>
<span data-ttu-id="99d9e-116">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99d9e-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="99d9e-117">-CertificateFilePath</span></span>
<span data-ttu-id="99d9e-118">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="99d9e-119">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99d9e-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99d9e-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="99d9e-120">-CertificatePassword</span></span>
<span data-ttu-id="99d9e-121">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="99d9e-122">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99d9e-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99d9e-123">-Config</span><span class="sxs-lookup"><span data-stu-id="99d9e-123">-Config</span></span>
<span data-ttu-id="99d9e-124">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="99d9e-125">Bu nesne New-AzHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="99d9e-125">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="99d9e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d9e-126">-DefaultProfile</span></span>
<span data-ttu-id="99d9e-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99d9e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99d9e-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="99d9e-128">-ObjectId</span></span>
<span data-ttu-id="99d9e-129">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="99d9e-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="99d9e-130">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99d9e-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="99d9e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d9e-131">CommonParameters</span></span>
<span data-ttu-id="99d9e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99d9e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d9e-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d9e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d9e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99d9e-134">INPUTS</span></span>

### <span data-ttu-id="99d9e-135">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="99d9e-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="99d9e-136">System. Guid</span><span class="sxs-lookup"><span data-stu-id="99d9e-136">System.Guid</span></span>

## <span data-ttu-id="99d9e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99d9e-137">OUTPUTS</span></span>

### <span data-ttu-id="99d9e-138">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="99d9e-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="99d9e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99d9e-139">NOTES</span></span>

## <span data-ttu-id="99d9e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99d9e-140">RELATED LINKS</span></span>

[<span data-ttu-id="99d9e-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="99d9e-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


