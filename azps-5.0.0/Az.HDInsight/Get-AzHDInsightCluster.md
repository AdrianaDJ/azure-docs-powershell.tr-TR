---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275377"
---
# <span data-ttu-id="225a2-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="225a2-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="225a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="225a2-102">SYNOPSIS</span></span>
<span data-ttu-id="225a2-103">Geçerli abonelikle ilişkilendirilmiş tüm Azure HDInsight kümelerini veya belirli bir kaynak grubunu alır ve listeler.</span><span class="sxs-lookup"><span data-stu-id="225a2-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="225a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="225a2-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="225a2-105">DESCRIPTION</span></span>
<span data-ttu-id="225a2-106">**Get-AzHDInsightCluster** cmdlet 'i geçerli aboneliğin Azure HDInsight hizmeti kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="225a2-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="225a2-107">Belirli bir kümenin ayrıntılarını almak için *clustername* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="225a2-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="225a2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="225a2-108">EXAMPLES</span></span>

### <span data-ttu-id="225a2-109">Örnek 1: tüm Azure HDInsight kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="225a2-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="225a2-110">Bu komut tüm Azure HDInsight kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="225a2-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="225a2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="225a2-111">PARAMETERS</span></span>

### <span data-ttu-id="225a2-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="225a2-112">-ClusterName</span></span>
<span data-ttu-id="225a2-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="225a2-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225a2-114">-DefaultProfile</span></span>
<span data-ttu-id="225a2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="225a2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="225a2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225a2-116">-ResourceGroupName</span></span>
<span data-ttu-id="225a2-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="225a2-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225a2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225a2-118">CommonParameters</span></span>
<span data-ttu-id="225a2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="225a2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225a2-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="225a2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225a2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="225a2-121">INPUTS</span></span>

### <span data-ttu-id="225a2-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="225a2-122">None</span></span>

## <span data-ttu-id="225a2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="225a2-123">OUTPUTS</span></span>

### <span data-ttu-id="225a2-124">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="225a2-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="225a2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="225a2-125">NOTES</span></span>

## <span data-ttu-id="225a2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="225a2-126">RELATED LINKS</span></span>

[<span data-ttu-id="225a2-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="225a2-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="225a2-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="225a2-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


