---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: a0c534042df15d4ef999b47a5e468b1e13a8d14f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764840"
---
# <span data-ttu-id="3edcb-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="3edcb-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="3edcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3edcb-102">SYNOPSIS</span></span>
<span data-ttu-id="3edcb-103">Küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3edcb-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edcb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3edcb-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3edcb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3edcb-105">DESCRIPTION</span></span>
<span data-ttu-id="3edcb-106">**Set-AzureRmHDInsightDefaultStorage** cmdlet 'i, New-AzureRmHDInsightClusterConfig cmdlet 'i tarafından oluşturulan Azure HDInsight küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3edcb-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3edcb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3edcb-107">EXAMPLES</span></span>

### <span data-ttu-id="3edcb-108">Örnek 1: küme yapılandırma nesnesi için varsayılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="3edcb-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="3edcb-109">Bu komut, küme yapılandırma nesnesi için varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3edcb-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="3edcb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3edcb-110">PARAMETERS</span></span>

### <span data-ttu-id="3edcb-111">-Config</span><span class="sxs-lookup"><span data-stu-id="3edcb-111">-Config</span></span>
<span data-ttu-id="3edcb-112">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3edcb-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3edcb-113">Bu nesne, **New-AzureRmHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3edcb-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="3edcb-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3edcb-114">-StorageAccountKey</span></span>
<span data-ttu-id="3edcb-115">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3edcb-115">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3edcb-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3edcb-116">-StorageAccountName</span></span>
<span data-ttu-id="3edcb-117">HDInsight kümesinin kullanacağı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3edcb-117">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3edcb-118">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3edcb-118">-StorageAccountType</span></span>
<span data-ttu-id="3edcb-119">Varsayılan depolama hesabının türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3edcb-119">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="3edcb-120">Varsayılan olarak AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3edcb-120">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="3edcb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edcb-121">-DefaultProfile</span></span>
<span data-ttu-id="3edcb-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3edcb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3edcb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edcb-123">CommonParameters</span></span>
<span data-ttu-id="3edcb-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3edcb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edcb-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3edcb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edcb-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3edcb-126">INPUTS</span></span>

### <span data-ttu-id="3edcb-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3edcb-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="3edcb-128">Parametre ' config ', ardışık düzenin ' AzureHDInsightConfig ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3edcb-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="3edcb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3edcb-129">OUTPUTS</span></span>

### <span data-ttu-id="3edcb-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3edcb-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3edcb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3edcb-131">NOTES</span></span>

## <span data-ttu-id="3edcb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3edcb-132">RELATED LINKS</span></span>

