---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: fc992b427e0c07b1f9db634f9369c21917ec9556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765178"
---
# <span data-ttu-id="d76d3-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="d76d3-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="d76d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d76d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d76d3-103">Küme yapılandırma nesnesine küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="d76d3-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d76d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d76d3-104">SYNTAX</span></span>

### <span data-ttu-id="d76d3-105">CertificateFilePath (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d76d3-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d76d3-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d76d3-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d76d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d76d3-107">DESCRIPTION</span></span>
<span data-ttu-id="d76d3-108">**Add-AzureRmHDInsightClusterIdentity** cmdlet 'i, New-AzureRmHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine bir küme kimliği ekler.</span><span class="sxs-lookup"><span data-stu-id="d76d3-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d76d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d76d3-109">EXAMPLES</span></span>

### <span data-ttu-id="d76d3-110">Örnek 1: küme yapılandırma nesnesine küme kimliği bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="d76d3-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="d76d3-111">Bu komut, kümenin Azure Data Lake Store 'a erişmesine izin vererek-Hadoop-001 adlı kümeye küme kimliği bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="d76d3-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="d76d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d76d3-112">PARAMETERS</span></span>

### <span data-ttu-id="d76d3-113">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="d76d3-113">-AadTenantId</span></span>
<span data-ttu-id="d76d3-114">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d76d3-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d76d3-115">-CertificateFileContents</span></span>
<span data-ttu-id="d76d3-116">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d76d3-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d76d3-117">-CertificateFilePath</span></span>
<span data-ttu-id="d76d3-118">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d76d3-119">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d76d3-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d76d3-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d76d3-120">-CertificatePassword</span></span>
<span data-ttu-id="d76d3-121">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d76d3-122">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d76d3-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d76d3-123">-Config</span><span class="sxs-lookup"><span data-stu-id="d76d3-123">-Config</span></span>
<span data-ttu-id="d76d3-124">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d76d3-125">Bu nesne New-AzureRmHDInsightClusterConfig cmdlet tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d76d3-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="d76d3-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="d76d3-126">-ObjectId</span></span>
<span data-ttu-id="d76d3-127">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="d76d3-127">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="d76d3-128">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d76d3-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d76d3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76d3-129">-DefaultProfile</span></span>
<span data-ttu-id="d76d3-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d76d3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d76d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76d3-131">CommonParameters</span></span>
<span data-ttu-id="d76d3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d76d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76d3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d76d3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76d3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d76d3-134">INPUTS</span></span>

### <span data-ttu-id="d76d3-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d76d3-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="d76d3-136">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d76d3-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="d76d3-137">'Sine</span><span class="sxs-lookup"><span data-stu-id="d76d3-137">Guid</span></span>
<span data-ttu-id="d76d3-138">' ObjectID ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d76d3-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d76d3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d76d3-139">OUTPUTS</span></span>

### <span data-ttu-id="d76d3-140">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d76d3-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d76d3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d76d3-141">NOTES</span></span>

## <span data-ttu-id="d76d3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d76d3-142">RELATED LINKS</span></span>

[<span data-ttu-id="d76d3-143">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d76d3-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

