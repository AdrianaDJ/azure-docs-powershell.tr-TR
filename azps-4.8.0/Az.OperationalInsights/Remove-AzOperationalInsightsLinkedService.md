---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265856"
---
# <span data-ttu-id="42c3a-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="42c3a-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="42c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="42c3a-103">Çalışma alanı için hizmeti bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="42c3a-103">Unlink service for workspace</span></span>

## <span data-ttu-id="42c3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42c3a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42c3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="42c3a-106">Çalışma alanı için hizmeti bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="42c3a-106">Unlink service for workspace</span></span>

## <span data-ttu-id="42c3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="42c3a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42c3a-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="42c3a-109">Çalışma alanı için bağlı hizmetin bağlantısını kes</span><span class="sxs-lookup"><span data-stu-id="42c3a-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="42c3a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42c3a-110">PARAMETERS</span></span>

### <span data-ttu-id="42c3a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="42c3a-111">-AsJob</span></span>
<span data-ttu-id="42c3a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="42c3a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42c3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c3a-113">-DefaultProfile</span></span>
<span data-ttu-id="42c3a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42c3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c3a-115">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="42c3a-115">-LinkedServiceName</span></span>
<span data-ttu-id="42c3a-116">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="42c3a-116">The Workspace name.</span></span>

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

### <span data-ttu-id="42c3a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c3a-117">-ResourceGroupName</span></span>
<span data-ttu-id="42c3a-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42c3a-118">The resource group name.</span></span>

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

### <span data-ttu-id="42c3a-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="42c3a-119">-WorkspaceName</span></span>
<span data-ttu-id="42c3a-120">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="42c3a-120">The Workspace name.</span></span>

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

### <span data-ttu-id="42c3a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="42c3a-121">-Confirm</span></span>
<span data-ttu-id="42c3a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42c3a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c3a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c3a-123">-WhatIf</span></span>
<span data-ttu-id="42c3a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42c3a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c3a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42c3a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c3a-126">CommonParameters</span></span>
<span data-ttu-id="42c3a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42c3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c3a-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42c3a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c3a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42c3a-129">INPUTS</span></span>

### <span data-ttu-id="42c3a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="42c3a-130">System.String</span></span>

## <span data-ttu-id="42c3a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42c3a-131">OUTPUTS</span></span>

### <span data-ttu-id="42c3a-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42c3a-132">System.Boolean</span></span>

## <span data-ttu-id="42c3a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42c3a-133">NOTES</span></span>

## <span data-ttu-id="42c3a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42c3a-134">RELATED LINKS</span></span>
