---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 01dfcbbc9a8996ff351ecc9d88c688c96be345d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594044"
---
# <span data-ttu-id="55181-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="55181-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="55181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55181-102">SYNOPSIS</span></span>
<span data-ttu-id="55181-103">Belirtilen kümede çalışan düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55181-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55181-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55181-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55181-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55181-105">DESCRIPTION</span></span>
<span data-ttu-id="55181-106">**Set-AzureRmHDInsightClusterSize** cmdlet 'i belirtilen bir Azure HDInsight kümesindeki çalışan düğümü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55181-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="55181-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55181-107">EXAMPLES</span></span>

### <span data-ttu-id="55181-108">Örnek 1: belirtilen kümenin boyutunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="55181-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="55181-109">Bu komut,-Hadoop-001 adlı kümenin boyutunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55181-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="55181-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55181-110">PARAMETERS</span></span>

### <span data-ttu-id="55181-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="55181-111">-ClusterName</span></span>
<span data-ttu-id="55181-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55181-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="55181-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55181-113">-DefaultProfile</span></span>
<span data-ttu-id="55181-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="55181-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55181-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55181-115">-ResourceGroupName</span></span>
<span data-ttu-id="55181-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55181-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="55181-117">-Targetınstancecount</span><span class="sxs-lookup"><span data-stu-id="55181-117">-TargetInstanceCount</span></span>
<span data-ttu-id="55181-118">Kümedeki çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55181-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="55181-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55181-119">CommonParameters</span></span>
<span data-ttu-id="55181-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55181-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55181-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55181-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55181-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55181-122">INPUTS</span></span>

### <span data-ttu-id="55181-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55181-123">None</span></span>

## <span data-ttu-id="55181-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55181-124">OUTPUTS</span></span>

### <span data-ttu-id="55181-125">Microsoft. Azure. Management. HDInsight. modeller. Cluster</span><span class="sxs-lookup"><span data-stu-id="55181-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="55181-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55181-126">NOTES</span></span>

## <span data-ttu-id="55181-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55181-127">RELATED LINKS</span></span>
