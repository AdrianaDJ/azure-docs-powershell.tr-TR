---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: e52d838f0aa7ce901b8099710b38f570d4285a4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751822"
---
# <span data-ttu-id="4f27a-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f27a-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="4f27a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f27a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f27a-103">Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f27a-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="4f27a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f27a-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f27a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f27a-105">DESCRIPTION</span></span>
<span data-ttu-id="4f27a-106">**Remove-AzHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="4f27a-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="4f27a-107">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="4f27a-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="4f27a-108">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="4f27a-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="4f27a-109">Dış meta verileri 'nde depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="4f27a-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="4f27a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f27a-110">EXAMPLES</span></span>

### <span data-ttu-id="4f27a-111">Örnek 1: Azure HDInsight kümesini silme</span><span class="sxs-lookup"><span data-stu-id="4f27a-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="4f27a-112">Bu komut,-Hadoop-001 adlı kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f27a-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4f27a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f27a-113">PARAMETERS</span></span>

### <span data-ttu-id="4f27a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4f27a-114">-ClusterName</span></span>
<span data-ttu-id="4f27a-115">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f27a-115">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f27a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f27a-116">-DefaultProfile</span></span>
<span data-ttu-id="4f27a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f27a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f27a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f27a-118">-ResourceGroupName</span></span>
<span data-ttu-id="4f27a-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f27a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4f27a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f27a-120">CommonParameters</span></span>
<span data-ttu-id="4f27a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f27a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f27a-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f27a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f27a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f27a-123">INPUTS</span></span>

### <span data-ttu-id="4f27a-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f27a-124">None</span></span>

## <span data-ttu-id="4f27a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f27a-125">OUTPUTS</span></span>

### <span data-ttu-id="4f27a-126">Microsoft. Azure. Management. HDInsight. model. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="4f27a-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="4f27a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f27a-127">NOTES</span></span>

## <span data-ttu-id="4f27a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f27a-128">RELATED LINKS</span></span>

[<span data-ttu-id="4f27a-129">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f27a-129">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="4f27a-130">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f27a-130">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


