---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 6815e697376f51d70782885485541debb209ecf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751805"
---
# <span data-ttu-id="b6c52-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="b6c52-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="b6c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6c52-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c52-103">Küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6c52-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="b6c52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6c52-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6c52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6c52-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c52-106">**Set-AzHDInsightDefaultStorage** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6c52-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="b6c52-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6c52-107">EXAMPLES</span></span>

### <span data-ttu-id="b6c52-108">Örnek 1: küme yapılandırma nesnesi için varsayılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6c52-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="b6c52-109">Bu komut, küme yapılandırma nesnesi için varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6c52-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="b6c52-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6c52-110">PARAMETERS</span></span>

### <span data-ttu-id="b6c52-111">-Config</span><span class="sxs-lookup"><span data-stu-id="b6c52-111">-Config</span></span>
<span data-ttu-id="b6c52-112">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6c52-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b6c52-113">Bu nesne, **New-AzHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b6c52-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="b6c52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c52-114">-DefaultProfile</span></span>
<span data-ttu-id="b6c52-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6c52-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c52-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b6c52-116">-StorageAccountKey</span></span>
<span data-ttu-id="b6c52-117">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6c52-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c52-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6c52-118">-StorageAccountName</span></span>
<span data-ttu-id="b6c52-119">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6c52-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="b6c52-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b6c52-120">-StorageAccountType</span></span>
<span data-ttu-id="b6c52-121">Varsayılan depolama hesabının türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6c52-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="b6c52-122">Varsayılan olarak AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b6c52-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c52-123">CommonParameters</span></span>
<span data-ttu-id="b6c52-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6c52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c52-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c52-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c52-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6c52-126">INPUTS</span></span>

### <span data-ttu-id="b6c52-127">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b6c52-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b6c52-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6c52-128">OUTPUTS</span></span>

### <span data-ttu-id="b6c52-129">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b6c52-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b6c52-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6c52-130">NOTES</span></span>

## <span data-ttu-id="b6c52-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6c52-131">RELATED LINKS</span></span>
