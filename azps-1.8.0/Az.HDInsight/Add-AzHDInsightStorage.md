---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 1a1b11c80df44b30fde7da9353effeb548e73bfe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916643"
---
# <span data-ttu-id="ab334-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ab334-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="ab334-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab334-102">SYNOPSIS</span></span>
<span data-ttu-id="ab334-103">Küme yapılandırma nesnesine Azure depolama anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="ab334-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="ab334-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab334-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab334-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab334-105">DESCRIPTION</span></span>
<span data-ttu-id="ab334-106">**Add-AzHDInsightStorage** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine bir Azure depolama hesabı girişi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab334-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ab334-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab334-107">EXAMPLES</span></span>

### <span data-ttu-id="ab334-108">Örnek 1: küme yapılandırma nesnesine Azure depolama anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="ab334-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="ab334-109">Bu komut,-Hadoop-001 adlı HDInsight yapılandırmasına bir BLOB depolama hesabı girişi ekler.</span><span class="sxs-lookup"><span data-stu-id="ab334-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="ab334-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab334-110">PARAMETERS</span></span>

### <span data-ttu-id="ab334-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ab334-111">-Config</span></span>
<span data-ttu-id="ab334-112">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab334-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ab334-113">Bu nesne, **New-AzHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ab334-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ab334-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab334-114">-DefaultProfile</span></span>
<span data-ttu-id="ab334-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ab334-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab334-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ab334-116">-StorageAccountKey</span></span>
<span data-ttu-id="ab334-117">Depolama hesabının yeni kümeye ekleneceği depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab334-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="ab334-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ab334-118">-StorageAccountName</span></span>
<span data-ttu-id="ab334-119">Kümeye eklenecek depolama hesabının depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab334-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="ab334-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab334-120">CommonParameters</span></span>
<span data-ttu-id="ab334-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab334-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab334-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab334-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab334-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab334-123">INPUTS</span></span>

### <span data-ttu-id="ab334-124">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ab334-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ab334-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab334-125">OUTPUTS</span></span>

### <span data-ttu-id="ab334-126">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ab334-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ab334-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab334-127">NOTES</span></span>

## <span data-ttu-id="ab334-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab334-128">RELATED LINKS</span></span>

[<span data-ttu-id="ab334-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ab334-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


