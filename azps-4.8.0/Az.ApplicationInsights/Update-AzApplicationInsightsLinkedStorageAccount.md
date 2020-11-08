---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110100"
---
# <span data-ttu-id="a040a-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a040a-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a040a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a040a-102">SYNOPSIS</span></span>
<span data-ttu-id="a040a-103">Application Insights bağlantılı depolama hesabını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a040a-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="a040a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a040a-104">SYNTAX</span></span>

### <span data-ttu-id="a040a-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a040a-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a040a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a040a-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a040a-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a040a-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a040a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a040a-108">DESCRIPTION</span></span>
<span data-ttu-id="a040a-109">Application Insights bağlantılı depolama hesabını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a040a-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="a040a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a040a-110">EXAMPLES</span></span>

### <span data-ttu-id="a040a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a040a-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="a040a-112">$Account ilişkilendirmek için "componentName" bileşeni altındaki bağlı depolama hesabını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="a040a-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="a040a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a040a-113">PARAMETERS</span></span>

### <span data-ttu-id="a040a-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a040a-114">-ComponentName</span></span>
<span data-ttu-id="a040a-115">Bileşen adı</span><span class="sxs-lookup"><span data-stu-id="a040a-115">Component Name</span></span>

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

### <span data-ttu-id="a040a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a040a-116">-DefaultProfile</span></span>
<span data-ttu-id="a040a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a040a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a040a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a040a-118">-InputObject</span></span>
<span data-ttu-id="a040a-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a040a-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a040a-120">-Linkedstorageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="a040a-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="a040a-121">Depolama hesabı RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a040a-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a040a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a040a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a040a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a040a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a040a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a040a-124">-ResourceId</span></span>
<span data-ttu-id="a040a-125">Bileşen RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a040a-125">Component ResourceId</span></span>

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

### <span data-ttu-id="a040a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a040a-126">-Confirm</span></span>
<span data-ttu-id="a040a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a040a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a040a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a040a-128">-WhatIf</span></span>
<span data-ttu-id="a040a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a040a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a040a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a040a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a040a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a040a-131">CommonParameters</span></span>
<span data-ttu-id="a040a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a040a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a040a-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a040a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a040a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a040a-134">INPUTS</span></span>

### <span data-ttu-id="a040a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a040a-135">System.String</span></span>

### <span data-ttu-id="a040a-136">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a040a-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a040a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a040a-137">OUTPUTS</span></span>

### <span data-ttu-id="a040a-138">Microsoft. Azure. Commands. ApplicationInsights. model. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a040a-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a040a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a040a-139">NOTES</span></span>

## <span data-ttu-id="a040a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a040a-140">RELATED LINKS</span></span>
