---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320238"
---
# <span data-ttu-id="68bb7-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="68bb7-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="68bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="68bb7-103">Bir paylaşım aboneliği için sürekli eşitlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="68bb7-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="68bb7-104">Bir paylaşım aboneliği, kaynak kimliği veya adını kullanarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="68bb7-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="68bb7-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68bb7-105">SYNTAX</span></span>

### <span data-ttu-id="68bb7-106">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68bb7-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68bb7-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="68bb7-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68bb7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68bb7-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68bb7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="68bb7-109">DESCRIPTION</span></span>
<span data-ttu-id="68bb7-110">**Stop-AzDataShareSubscriptionSynchronization** cmdlet 'i, bir paylaşım aboneliği için sürekli eşitlemeyi durdurur</span><span class="sxs-lookup"><span data-stu-id="68bb7-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="68bb7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68bb7-111">EXAMPLES</span></span>

### <span data-ttu-id="68bb7-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68bb7-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="68bb7-113">Kimlik-20a4416b-b33b-4539-a908-71dc8ef698fb ile tanımlanan sürekli eşitlemeyi durdurur</span><span class="sxs-lookup"><span data-stu-id="68bb7-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="68bb7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68bb7-114">PARAMETERS</span></span>

### <span data-ttu-id="68bb7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68bb7-115">-AccountName</span></span>
<span data-ttu-id="68bb7-116">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="68bb7-116">Azure data share account name</span></span>

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

### <span data-ttu-id="68bb7-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="68bb7-117">-AsJob</span></span>
<span data-ttu-id="68bb7-118">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="68bb7-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="68bb7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68bb7-119">-DefaultProfile</span></span>
<span data-ttu-id="68bb7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68bb7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68bb7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68bb7-121">-InputObject</span></span>
<span data-ttu-id="68bb7-122">Azure veri paylaşımı abonelik nesnesi</span><span class="sxs-lookup"><span data-stu-id="68bb7-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68bb7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68bb7-123">-ResourceGroupName</span></span>
<span data-ttu-id="68bb7-124">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="68bb7-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="68bb7-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="68bb7-125">-ResourceId</span></span>
<span data-ttu-id="68bb7-126">Azure Share aboneliğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="68bb7-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="68bb7-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="68bb7-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="68bb7-128">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="68bb7-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="68bb7-129">-Synchronizationıd</span><span class="sxs-lookup"><span data-stu-id="68bb7-129">-SynchronizationId</span></span>
<span data-ttu-id="68bb7-130">Durdurulması gereken eşitleme kimliği</span><span class="sxs-lookup"><span data-stu-id="68bb7-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68bb7-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="68bb7-131">-Confirm</span></span>
<span data-ttu-id="68bb7-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68bb7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68bb7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68bb7-133">-WhatIf</span></span>
<span data-ttu-id="68bb7-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68bb7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68bb7-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68bb7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68bb7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68bb7-136">CommonParameters</span></span>
<span data-ttu-id="68bb7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68bb7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68bb7-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68bb7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68bb7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68bb7-139">INPUTS</span></span>

### <span data-ttu-id="68bb7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="68bb7-140">System.String</span></span>

### <span data-ttu-id="68bb7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="68bb7-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="68bb7-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68bb7-142">OUTPUTS</span></span>

### <span data-ttu-id="68bb7-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="68bb7-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="68bb7-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68bb7-144">NOTES</span></span>

## <span data-ttu-id="68bb7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68bb7-145">RELATED LINKS</span></span>
