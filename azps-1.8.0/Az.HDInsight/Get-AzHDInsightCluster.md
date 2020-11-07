---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 8b15a93ee576af683cb2ebfffa621937a2ebba78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916639"
---
# <span data-ttu-id="b2748-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b2748-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="b2748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2748-102">SYNOPSIS</span></span>
<span data-ttu-id="b2748-103">Geçerli abonelikle ilişkilendirilmiş tüm Azure HDInsight kümelerini veya belirli bir kaynak grubunu alır ve listeler.</span><span class="sxs-lookup"><span data-stu-id="b2748-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="b2748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2748-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2748-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2748-105">DESCRIPTION</span></span>
<span data-ttu-id="b2748-106">**Get-AzHDInsightCluster** cmdlet 'i geçerli aboneliğin Azure HDInsight hizmeti kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b2748-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="b2748-107">Belirli bir kümenin ayrıntılarını almak için *clustername* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b2748-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="b2748-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2748-108">EXAMPLES</span></span>

### <span data-ttu-id="b2748-109">Örnek 1: tüm Azure HDInsight kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="b2748-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="b2748-110">Bu komut tüm Azure HDInsight kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b2748-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="b2748-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2748-111">PARAMETERS</span></span>

### <span data-ttu-id="b2748-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b2748-112">-ClusterName</span></span>
<span data-ttu-id="b2748-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2748-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b2748-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2748-114">-DefaultProfile</span></span>
<span data-ttu-id="b2748-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b2748-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2748-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2748-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2748-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2748-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b2748-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2748-118">CommonParameters</span></span>
<span data-ttu-id="b2748-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2748-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2748-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2748-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2748-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2748-121">INPUTS</span></span>

### <span data-ttu-id="b2748-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b2748-122">None</span></span>

## <span data-ttu-id="b2748-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2748-123">OUTPUTS</span></span>

### <span data-ttu-id="b2748-124">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b2748-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="b2748-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2748-125">NOTES</span></span>

## <span data-ttu-id="b2748-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2748-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2748-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b2748-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="b2748-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b2748-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

