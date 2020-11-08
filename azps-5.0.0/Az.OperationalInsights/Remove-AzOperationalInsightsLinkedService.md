---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277573"
---
# <span data-ttu-id="e88dc-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="e88dc-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="e88dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e88dc-103">Çalışma alanı için hizmeti bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="e88dc-103">Unlink service for workspace</span></span>

## <span data-ttu-id="e88dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e88dc-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e88dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e88dc-105">DESCRIPTION</span></span>
<span data-ttu-id="e88dc-106">Çalışma alanı için hizmeti bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="e88dc-106">Unlink service for workspace</span></span>

## <span data-ttu-id="e88dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e88dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e88dc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e88dc-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="e88dc-109">Çalışma alanı için bağlı hizmetin bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="e88dc-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="e88dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e88dc-110">PARAMETERS</span></span>

### <span data-ttu-id="e88dc-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e88dc-111">-AsJob</span></span>
<span data-ttu-id="e88dc-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e88dc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e88dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88dc-113">-DefaultProfile</span></span>
<span data-ttu-id="e88dc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e88dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88dc-115">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="e88dc-115">-LinkedServiceName</span></span>
<span data-ttu-id="e88dc-116">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e88dc-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="e88dc-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e88dc-118">The resource group name.</span></span>

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

### <span data-ttu-id="e88dc-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e88dc-119">-WorkspaceName</span></span>
<span data-ttu-id="e88dc-120">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e88dc-120">The Workspace name.</span></span>

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

### <span data-ttu-id="e88dc-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e88dc-121">-Confirm</span></span>
<span data-ttu-id="e88dc-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e88dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88dc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88dc-123">-WhatIf</span></span>
<span data-ttu-id="e88dc-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e88dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88dc-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e88dc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88dc-126">CommonParameters</span></span>
<span data-ttu-id="e88dc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e88dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88dc-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e88dc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88dc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e88dc-129">INPUTS</span></span>

### <span data-ttu-id="e88dc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e88dc-130">System.String</span></span>

## <span data-ttu-id="e88dc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e88dc-131">OUTPUTS</span></span>

### <span data-ttu-id="e88dc-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e88dc-132">System.Boolean</span></span>

## <span data-ttu-id="e88dc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e88dc-133">NOTES</span></span>

## <span data-ttu-id="e88dc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e88dc-134">RELATED LINKS</span></span>
