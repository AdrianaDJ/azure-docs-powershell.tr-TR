---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274029"
---
# <span data-ttu-id="f0d7a-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="f0d7a-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="f0d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d7a-103">Kümeyi Sil</span><span class="sxs-lookup"><span data-stu-id="f0d7a-103">Delete cluster</span></span>

## <span data-ttu-id="f0d7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0d7a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d7a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0d7a-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d7a-106">Kümeyi Sil, yalnızca sağlama durumu "başarılı" olan kümelere Uygula</span><span class="sxs-lookup"><span data-stu-id="f0d7a-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="f0d7a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0d7a-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d7a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0d7a-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="f0d7a-109">Kümeyi Sil</span><span class="sxs-lookup"><span data-stu-id="f0d7a-109">Delete cluster</span></span>

## <span data-ttu-id="f0d7a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0d7a-110">PARAMETERS</span></span>

### <span data-ttu-id="f0d7a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f0d7a-111">-AsJob</span></span>
<span data-ttu-id="f0d7a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f0d7a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0d7a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f0d7a-113">-ClusterName</span></span>
<span data-ttu-id="f0d7a-114">Küme adı.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d7a-115">-DefaultProfile</span></span>
<span data-ttu-id="f0d7a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d7a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d7a-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0d7a-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-118">The resource group name.</span></span>

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

### <span data-ttu-id="f0d7a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0d7a-119">-Confirm</span></span>
<span data-ttu-id="f0d7a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d7a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d7a-121">-WhatIf</span></span>
<span data-ttu-id="f0d7a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d7a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d7a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d7a-124">CommonParameters</span></span>
<span data-ttu-id="f0d7a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d7a-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0d7a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d7a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0d7a-127">INPUTS</span></span>

### <span data-ttu-id="f0d7a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d7a-128">System.String</span></span>

## <span data-ttu-id="f0d7a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0d7a-129">OUTPUTS</span></span>

### <span data-ttu-id="f0d7a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0d7a-130">System.Boolean</span></span>

## <span data-ttu-id="f0d7a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0d7a-131">NOTES</span></span>

## <span data-ttu-id="f0d7a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0d7a-132">RELATED LINKS</span></span>
