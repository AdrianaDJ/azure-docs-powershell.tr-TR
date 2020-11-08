---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273727"
---
# <span data-ttu-id="fab2b-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fab2b-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="fab2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab2b-102">SYNOPSIS</span></span>
<span data-ttu-id="fab2b-103">Application Insights bağlantılı depolama hesabını silme</span><span class="sxs-lookup"><span data-stu-id="fab2b-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="fab2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fab2b-104">SYNTAX</span></span>

### <span data-ttu-id="fab2b-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fab2b-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab2b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fab2b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab2b-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fab2b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab2b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fab2b-108">DESCRIPTION</span></span>
<span data-ttu-id="fab2b-109">Application Insights bağlantılı depolama hesabını silme</span><span class="sxs-lookup"><span data-stu-id="fab2b-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="fab2b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fab2b-110">EXAMPLES</span></span>

### <span data-ttu-id="fab2b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fab2b-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="fab2b-112">Application Insights bileşeniyle ilişkilendirilmiş bağlantılı depolama hesabını silme "componentName"</span><span class="sxs-lookup"><span data-stu-id="fab2b-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="fab2b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fab2b-113">PARAMETERS</span></span>

### <span data-ttu-id="fab2b-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="fab2b-114">-ComponentName</span></span>
<span data-ttu-id="fab2b-115">Bileşen adı</span><span class="sxs-lookup"><span data-stu-id="fab2b-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab2b-116">-DefaultProfile</span></span>
<span data-ttu-id="fab2b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fab2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab2b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab2b-118">-InputObject</span></span>
<span data-ttu-id="fab2b-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fab2b-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab2b-120">-ResourceGroupName</span></span>
<span data-ttu-id="fab2b-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fab2b-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fab2b-122">-ResourceId</span></span>
<span data-ttu-id="fab2b-123">Bileşen RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fab2b-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="fab2b-124">-Confirm</span></span>
<span data-ttu-id="fab2b-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fab2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab2b-126">-WhatIf</span></span>
<span data-ttu-id="fab2b-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fab2b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab2b-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fab2b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab2b-129">CommonParameters</span></span>
<span data-ttu-id="fab2b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fab2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab2b-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fab2b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab2b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fab2b-132">INPUTS</span></span>

### <span data-ttu-id="fab2b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fab2b-133">System.String</span></span>

### <span data-ttu-id="fab2b-134">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fab2b-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="fab2b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fab2b-135">OUTPUTS</span></span>

### <span data-ttu-id="fab2b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fab2b-136">System.Boolean</span></span>

## <span data-ttu-id="fab2b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fab2b-137">NOTES</span></span>

## <span data-ttu-id="fab2b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fab2b-138">RELATED LINKS</span></span>
