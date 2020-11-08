---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104227"
---
# <span data-ttu-id="f3945-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="f3945-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="f3945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3945-102">SYNOPSIS</span></span>
<span data-ttu-id="f3945-103">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="f3945-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f3945-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3945-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3945-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3945-105">DESCRIPTION</span></span>
<span data-ttu-id="f3945-106">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="f3945-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f3945-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3945-107">EXAMPLES</span></span>

### <span data-ttu-id="f3945-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3945-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="f3945-109">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="f3945-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="f3945-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3945-110">PARAMETERS</span></span>

### <span data-ttu-id="f3945-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f3945-111">-AsJob</span></span>
<span data-ttu-id="f3945-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f3945-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3945-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3945-113">-DefaultProfile</span></span>
<span data-ttu-id="f3945-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3945-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3945-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f3945-115">-ProviderName</span></span>
<span data-ttu-id="f3945-116">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="f3945-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3945-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3945-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f3945-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3945-119">-ResourceName</span></span>
<span data-ttu-id="f3945-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f3945-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f3945-121">-ResourceParentName</span></span>
<span data-ttu-id="f3945-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f3945-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f3945-123">-ResourceParentType</span></span>
<span data-ttu-id="f3945-124">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="f3945-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3945-125">-ResourceType</span></span>
<span data-ttu-id="f3945-126">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="f3945-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3945-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3945-127">-Confirm</span></span>
<span data-ttu-id="f3945-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3945-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3945-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3945-129">-WhatIf</span></span>
<span data-ttu-id="f3945-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3945-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3945-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3945-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3945-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3945-132">CommonParameters</span></span>
<span data-ttu-id="f3945-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3945-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3945-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f3945-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3945-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3945-135">INPUTS</span></span>

### <span data-ttu-id="f3945-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f3945-136">System.String</span></span>

## <span data-ttu-id="f3945-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3945-137">OUTPUTS</span></span>

### <span data-ttu-id="f3945-138">Microsoft. Azure. Commands. Maintenance. modeller. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="f3945-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="f3945-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3945-139">NOTES</span></span>

## <span data-ttu-id="f3945-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3945-140">RELATED LINKS</span></span>
