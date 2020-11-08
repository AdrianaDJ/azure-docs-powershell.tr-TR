---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277699"
---
# <span data-ttu-id="b0328-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="b0328-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="b0328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0328-102">SYNOPSIS</span></span>
<span data-ttu-id="b0328-103">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="b0328-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="b0328-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0328-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0328-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0328-105">DESCRIPTION</span></span>
<span data-ttu-id="b0328-106">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="b0328-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="b0328-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0328-107">EXAMPLES</span></span>

### <span data-ttu-id="b0328-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b0328-108">Example 1</span></span>
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

<span data-ttu-id="b0328-109">Bakım güncelleştirmelerini kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="b0328-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="b0328-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0328-110">PARAMETERS</span></span>

### <span data-ttu-id="b0328-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b0328-111">-AsJob</span></span>
<span data-ttu-id="b0328-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b0328-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0328-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0328-113">-DefaultProfile</span></span>
<span data-ttu-id="b0328-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0328-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0328-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="b0328-115">-ProviderName</span></span>
<span data-ttu-id="b0328-116">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="b0328-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="b0328-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0328-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0328-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b0328-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="b0328-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b0328-119">-ResourceName</span></span>
<span data-ttu-id="b0328-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b0328-120">The resource name.</span></span>

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

### <span data-ttu-id="b0328-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b0328-121">-ResourceParentName</span></span>
<span data-ttu-id="b0328-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b0328-122">The parent resource name.</span></span>

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

### <span data-ttu-id="b0328-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b0328-123">-ResourceParentType</span></span>
<span data-ttu-id="b0328-124">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="b0328-124">The parent resource type.</span></span>

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

### <span data-ttu-id="b0328-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b0328-125">-ResourceType</span></span>
<span data-ttu-id="b0328-126">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="b0328-126">The resource type.</span></span>

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

### <span data-ttu-id="b0328-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0328-127">-Confirm</span></span>
<span data-ttu-id="b0328-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0328-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0328-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0328-129">-WhatIf</span></span>
<span data-ttu-id="b0328-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0328-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0328-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0328-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0328-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0328-132">CommonParameters</span></span>
<span data-ttu-id="b0328-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0328-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0328-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b0328-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0328-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0328-135">INPUTS</span></span>

### <span data-ttu-id="b0328-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b0328-136">System.String</span></span>

## <span data-ttu-id="b0328-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0328-137">OUTPUTS</span></span>

### <span data-ttu-id="b0328-138">Microsoft. Azure. Commands. Maintenance. modeller. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="b0328-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="b0328-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0328-139">NOTES</span></span>

## <span data-ttu-id="b0328-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0328-140">RELATED LINKS</span></span>
