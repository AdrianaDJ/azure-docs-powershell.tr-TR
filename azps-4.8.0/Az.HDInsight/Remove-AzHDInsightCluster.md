---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109063"
---
# <span data-ttu-id="d3789-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3789-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="d3789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3789-102">SYNOPSIS</span></span>
<span data-ttu-id="d3789-103">Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3789-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="d3789-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3789-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3789-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3789-105">DESCRIPTION</span></span>
<span data-ttu-id="d3789-106">**Remove-AzHDInsightCluster** cmdlet 'i, belirtilen HDInsight hizmet kümesini abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="d3789-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="d3789-107">Bu işlem, kümedeki Hadoop Dağıtılmış dosya sisteminde (".) depolanan verileri de siler.</span><span class="sxs-lookup"><span data-stu-id="d3789-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="d3789-108">İlişkili Azure depolama hesabında depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="d3789-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="d3789-109">Dış meta verileri 'nde depolanan veriler silinmez.</span><span class="sxs-lookup"><span data-stu-id="d3789-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="d3789-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3789-110">EXAMPLES</span></span>

### <span data-ttu-id="d3789-111">Örnek 1: Azure HDInsight kümesini silme</span><span class="sxs-lookup"><span data-stu-id="d3789-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="d3789-112">Bu komut,-Hadoop-001 adlı kümeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3789-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d3789-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3789-113">PARAMETERS</span></span>

### <span data-ttu-id="d3789-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d3789-114">-ClusterName</span></span>
<span data-ttu-id="d3789-115">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3789-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d3789-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3789-116">-DefaultProfile</span></span>
<span data-ttu-id="d3789-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3789-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3789-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3789-118">-ResourceGroupName</span></span>
<span data-ttu-id="d3789-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3789-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d3789-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d3789-120">-PassThru</span></span>
<span data-ttu-id="d3789-121">Geçiş varsa, sonucun çıktısını alırsınız</span><span class="sxs-lookup"><span data-stu-id="d3789-121">If PassThru is present, output the result</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3789-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3789-122">CommonParameters</span></span>
<span data-ttu-id="d3789-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3789-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3789-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3789-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3789-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3789-125">INPUTS</span></span>

### <span data-ttu-id="d3789-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3789-126">None</span></span>
## <span data-ttu-id="d3789-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3789-127">OUTPUTS</span></span>

### <span data-ttu-id="d3789-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3789-128">System.Boolean</span></span>
## <span data-ttu-id="d3789-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3789-129">NOTES</span></span>

## <span data-ttu-id="d3789-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3789-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3789-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3789-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="d3789-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3789-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


