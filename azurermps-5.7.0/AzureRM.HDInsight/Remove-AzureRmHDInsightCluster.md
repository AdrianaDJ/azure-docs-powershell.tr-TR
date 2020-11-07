---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763055"
---
# <span data-ttu-id="61c62-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="61c62-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="61c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61c62-102">SYNOPSIS</span></span>
<span data-ttu-id="61c62-103">Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61c62-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61c62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61c62-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61c62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61c62-105">DESCRIPTION</span></span>
<span data-ttu-id="61c62-106">**Remove-AzureRmHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="61c62-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="61c62-107">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="61c62-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="61c62-108">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="61c62-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="61c62-109">Dış meta verileri 'nde depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="61c62-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="61c62-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61c62-110">EXAMPLES</span></span>

### <span data-ttu-id="61c62-111">Örnek 1: Azure HDInsight kümesini silme</span><span class="sxs-lookup"><span data-stu-id="61c62-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="61c62-112">Bu komut,-Hadoop-001 adlı kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61c62-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="61c62-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61c62-113">PARAMETERS</span></span>

### <span data-ttu-id="61c62-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61c62-114">-ClusterName</span></span>
<span data-ttu-id="61c62-115">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c62-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c62-116">-DefaultProfile</span></span>
<span data-ttu-id="61c62-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61c62-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c62-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c62-118">-ResourceGroupName</span></span>
<span data-ttu-id="61c62-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61c62-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c62-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c62-120">CommonParameters</span></span>
<span data-ttu-id="61c62-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61c62-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c62-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c62-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c62-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61c62-123">INPUTS</span></span>

### <span data-ttu-id="61c62-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61c62-124">None</span></span>
<span data-ttu-id="61c62-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="61c62-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61c62-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61c62-126">OUTPUTS</span></span>

### <span data-ttu-id="61c62-127">Microsoft. Azure. Management. HDInsight. model. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="61c62-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="61c62-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61c62-128">NOTES</span></span>

## <span data-ttu-id="61c62-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61c62-129">RELATED LINKS</span></span>

[<span data-ttu-id="61c62-130">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="61c62-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="61c62-131">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="61c62-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


