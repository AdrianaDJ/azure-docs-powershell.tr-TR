---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: dc80b30e02901aaa56185270cb775d7b9ea1f106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104422"
---
# <span data-ttu-id="715b6-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="715b6-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="715b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="715b6-102">SYNOPSIS</span></span>
<span data-ttu-id="715b6-103">tetikleyiciyi kaldırır</span><span class="sxs-lookup"><span data-stu-id="715b6-103">removes a trigger</span></span>

## <span data-ttu-id="715b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="715b6-104">SYNTAX</span></span>

### <span data-ttu-id="715b6-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="715b6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="715b6-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="715b6-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="715b6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="715b6-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="715b6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="715b6-108">DESCRIPTION</span></span>
<span data-ttu-id="715b6-109">**Remove-AzDataShareTrigger** cmdlet 'i bir datashare tetikleyicisini kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="715b6-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="715b6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="715b6-110">EXAMPLES</span></span>

### <span data-ttu-id="715b6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="715b6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="715b6-112">Bu komutlar, Share aboneliği ile Share-Scripts</span><span class="sxs-lookup"><span data-stu-id="715b6-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="715b6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="715b6-113">PARAMETERS</span></span>

### <span data-ttu-id="715b6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="715b6-114">-AccountName</span></span>
<span data-ttu-id="715b6-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="715b6-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="715b6-116">-AsJob</span></span>
<span data-ttu-id="715b6-117">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="715b6-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715b6-118">-DefaultProfile</span></span>
<span data-ttu-id="715b6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="715b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="715b6-120">-InputObject</span></span>
<span data-ttu-id="715b6-121">Azure veri paylaşımı tetik nesnesi</span><span class="sxs-lookup"><span data-stu-id="715b6-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="715b6-122">-Name</span></span>
<span data-ttu-id="715b6-123">Azure veri paylaşımı tetik adı</span><span class="sxs-lookup"><span data-stu-id="715b6-123">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="715b6-124">-PassThru</span></span>
<span data-ttu-id="715b6-125">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="715b6-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="715b6-127">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="715b6-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="715b6-128">-ResourceId</span></span>
<span data-ttu-id="715b6-129">Azure veri paylaşımı tetikleyicisinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="715b6-129">The resource id of azure data share trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="715b6-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="715b6-131">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="715b6-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="715b6-132">-Confirm</span></span>
<span data-ttu-id="715b6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="715b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715b6-134">-WhatIf</span></span>
<span data-ttu-id="715b6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="715b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="715b6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="715b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715b6-137">CommonParameters</span></span>
<span data-ttu-id="715b6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="715b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715b6-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715b6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715b6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="715b6-140">INPUTS</span></span>

### <span data-ttu-id="715b6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="715b6-141">System.String</span></span>

### <span data-ttu-id="715b6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="715b6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="715b6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="715b6-143">OUTPUTS</span></span>

### <span data-ttu-id="715b6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="715b6-144">System.Boolean</span></span>

## <span data-ttu-id="715b6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="715b6-145">NOTES</span></span>

## <span data-ttu-id="715b6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="715b6-146">RELATED LINKS</span></span>
