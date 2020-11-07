---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: aba2f1d2b5162e84c4765939195ce64214161a79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764411"
---
# <span data-ttu-id="45ff8-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="45ff8-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="45ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="45ff8-103">Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45ff8-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45ff8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45ff8-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45ff8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="45ff8-106">**Remove-AzureRmHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="45ff8-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="45ff8-107">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="45ff8-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="45ff8-108">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="45ff8-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="45ff8-109">Dış meta verileri 'nde depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="45ff8-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="45ff8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="45ff8-111">Örnek 1: Azure HDInsight kümesini silme</span><span class="sxs-lookup"><span data-stu-id="45ff8-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="45ff8-112">Bu komut,-Hadoop-001 adlı kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45ff8-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="45ff8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45ff8-113">PARAMETERS</span></span>

### <span data-ttu-id="45ff8-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="45ff8-114">-ClusterName</span></span>
<span data-ttu-id="45ff8-115">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45ff8-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="45ff8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ff8-116">-DefaultProfile</span></span>
<span data-ttu-id="45ff8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45ff8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45ff8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ff8-118">-ResourceGroupName</span></span>
<span data-ttu-id="45ff8-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45ff8-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="45ff8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ff8-120">CommonParameters</span></span>
<span data-ttu-id="45ff8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45ff8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ff8-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ff8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ff8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45ff8-123">INPUTS</span></span>

### <span data-ttu-id="45ff8-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="45ff8-124">None</span></span>

## <span data-ttu-id="45ff8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45ff8-125">OUTPUTS</span></span>

### <span data-ttu-id="45ff8-126">Microsoft. Azure. Management. HDInsight. model. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="45ff8-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="45ff8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45ff8-127">NOTES</span></span>

## <span data-ttu-id="45ff8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45ff8-128">RELATED LINKS</span></span>

[<span data-ttu-id="45ff8-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="45ff8-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="45ff8-130">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="45ff8-130">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


