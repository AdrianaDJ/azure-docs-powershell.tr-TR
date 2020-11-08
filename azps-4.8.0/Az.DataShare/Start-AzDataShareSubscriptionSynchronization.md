---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274562"
---
# <span data-ttu-id="c6061-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="c6061-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="c6061-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6061-102">SYNOPSIS</span></span>
<span data-ttu-id="c6061-103">Bir paylaşım aboneliği için eşitlemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="c6061-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="c6061-104">Bir paylaşım aboneliği, kaynak kimliği veya adını kullanarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c6061-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="c6061-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6061-105">SYNTAX</span></span>

### <span data-ttu-id="c6061-106">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6061-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6061-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c6061-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6061-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6061-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6061-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6061-109">DESCRIPTION</span></span>
<span data-ttu-id="c6061-110">**Start-AzDataShareSubscriptionSynchronization** cmdlet 'i, bir paylaşım aboneliği için eşitleme başlatır</span><span class="sxs-lookup"><span data-stu-id="c6061-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="c6061-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6061-111">EXAMPLES</span></span>

### <span data-ttu-id="c6061-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6061-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="c6061-113">Bu komut, hesap WikiAds 'daki AdsShareSubscription adlı bir paylaşım için eşitlemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="c6061-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="c6061-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6061-114">PARAMETERS</span></span>

### <span data-ttu-id="c6061-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6061-115">-AccountName</span></span>
<span data-ttu-id="c6061-116">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="c6061-116">Azure data share account name</span></span>

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

### <span data-ttu-id="c6061-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="c6061-117">-AsJob</span></span>
<span data-ttu-id="c6061-118">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c6061-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c6061-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6061-119">-DefaultProfile</span></span>
<span data-ttu-id="c6061-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6061-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6061-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6061-121">-InputObject</span></span>
<span data-ttu-id="c6061-122">Azure veri paylaşımı abonelik nesnesi</span><span class="sxs-lookup"><span data-stu-id="c6061-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="c6061-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6061-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6061-124">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c6061-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c6061-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c6061-125">-ResourceId</span></span>
<span data-ttu-id="c6061-126">Azure Share aboneliğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c6061-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="c6061-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c6061-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="c6061-128">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="c6061-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c6061-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="c6061-129">-SynchronizationMode</span></span>
<span data-ttu-id="c6061-130">Eşitleme modu (FullSync veya artımlı)</span><span class="sxs-lookup"><span data-stu-id="c6061-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="c6061-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6061-131">-Confirm</span></span>
<span data-ttu-id="c6061-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6061-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6061-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6061-133">-WhatIf</span></span>
<span data-ttu-id="c6061-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6061-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6061-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6061-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6061-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6061-136">CommonParameters</span></span>
<span data-ttu-id="c6061-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6061-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6061-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c6061-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6061-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6061-139">INPUTS</span></span>

### <span data-ttu-id="c6061-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c6061-140">System.String</span></span>

### <span data-ttu-id="c6061-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c6061-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="c6061-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6061-142">OUTPUTS</span></span>

### <span data-ttu-id="c6061-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="c6061-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="c6061-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6061-144">NOTES</span></span>

## <span data-ttu-id="c6061-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6061-145">RELATED LINKS</span></span>
