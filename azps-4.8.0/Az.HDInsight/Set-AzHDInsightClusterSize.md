---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108252"
---
# <span data-ttu-id="f7a84-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="f7a84-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="f7a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7a84-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a84-103">Belirtilen kümede çalışan düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f7a84-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="f7a84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7a84-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7a84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7a84-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a84-106">**Set-AzHDInsightClusterSize** cmdlet 'i belirtilen bir Azure HDInsight kümesindeki çalışan düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f7a84-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f7a84-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7a84-107">EXAMPLES</span></span>

### <span data-ttu-id="f7a84-108">Örnek 1: belirtilen kümenin boyutunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="f7a84-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="f7a84-109">Bu komut,-Hadoop-001 adlı kümenin boyutunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f7a84-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f7a84-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7a84-110">PARAMETERS</span></span>

### <span data-ttu-id="f7a84-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f7a84-111">-ClusterName</span></span>
<span data-ttu-id="f7a84-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7a84-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f7a84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a84-113">-DefaultProfile</span></span>
<span data-ttu-id="f7a84-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f7a84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7a84-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a84-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7a84-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7a84-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7a84-117">-Targetınstancecount</span><span class="sxs-lookup"><span data-stu-id="f7a84-117">-TargetInstanceCount</span></span>
<span data-ttu-id="f7a84-118">Kümedeki çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7a84-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7a84-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a84-119">CommonParameters</span></span>
<span data-ttu-id="f7a84-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7a84-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a84-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a84-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a84-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7a84-122">INPUTS</span></span>

### <span data-ttu-id="f7a84-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f7a84-123">None</span></span>

## <span data-ttu-id="f7a84-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7a84-124">OUTPUTS</span></span>

### <span data-ttu-id="f7a84-125">Microsoft. Azure. Management. HDInsight. modeller. Cluster</span><span class="sxs-lookup"><span data-stu-id="f7a84-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="f7a84-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7a84-126">NOTES</span></span>

## <span data-ttu-id="f7a84-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7a84-127">RELATED LINKS</span></span>
