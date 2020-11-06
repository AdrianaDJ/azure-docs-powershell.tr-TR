---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: 1d81b5c528739fb012f90e6e112422c4e828c1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590283"
---
# <span data-ttu-id="a2f6b-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a2f6b-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="a2f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f6b-103">Küme yapılandırma nesnesine Azure depolama anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2f6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2f6b-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2f6b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f6b-106">**Add-AzureRmHDInsightStorage** cmdlet 'i, New-AzureRmHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight yapılandırma nesnesine bir Azure depolama hesabı girişi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a2f6b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="a2f6b-108">Örnek 1: küme yapılandırma nesnesine Azure depolama anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="a2f6b-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="a2f6b-109">Bu komut,-Hadoop-001 adlı HDInsight yapılandırmasına bir BLOB depolama hesabı girişi ekler.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="a2f6b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2f6b-110">PARAMETERS</span></span>

### <span data-ttu-id="a2f6b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="a2f6b-111">-Config</span></span>
<span data-ttu-id="a2f6b-112">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a2f6b-113">Bu nesne, **New-AzureRmHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="a2f6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f6b-114">-DefaultProfile</span></span>
<span data-ttu-id="a2f6b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a2f6b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2f6b-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2f6b-116">-StorageAccountKey</span></span>
<span data-ttu-id="a2f6b-117">Depolama hesabının yeni kümeye ekleneceği depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="a2f6b-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2f6b-118">-StorageAccountName</span></span>
<span data-ttu-id="a2f6b-119">Kümeye eklenecek depolama hesabının depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="a2f6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f6b-120">CommonParameters</span></span>
<span data-ttu-id="a2f6b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2f6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f6b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2f6b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f6b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2f6b-123">INPUTS</span></span>

### <span data-ttu-id="a2f6b-124">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a2f6b-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="a2f6b-125">Parametreler: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2f6b-125">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="a2f6b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2f6b-126">OUTPUTS</span></span>

### <span data-ttu-id="a2f6b-127">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a2f6b-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a2f6b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2f6b-128">NOTES</span></span>

## <span data-ttu-id="a2f6b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2f6b-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2f6b-130">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a2f6b-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


