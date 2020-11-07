---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 9991829a70029366086a58020aa53f839db8b6c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753658"
---
# <span data-ttu-id="75f3f-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="75f3f-101">Update-AzActionRule</span></span>

## <span data-ttu-id="75f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="75f3f-103">Eylem kuralı özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75f3f-103">Updates action rule properties.</span></span>

## <span data-ttu-id="75f3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75f3f-104">SYNTAX</span></span>

### <span data-ttu-id="75f3f-105">ByNameSimplifiedPatch (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75f3f-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f3f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="75f3f-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f3f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="75f3f-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f3f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="75f3f-108">DESCRIPTION</span></span>
<span data-ttu-id="75f3f-109">**Update-AzActionRule** cmdlet güncelleştirme eylem kuralı Özellikler-durum ve Etiketler.</span><span class="sxs-lookup"><span data-stu-id="75f3f-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="75f3f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75f3f-110">EXAMPLES</span></span>

### <span data-ttu-id="75f3f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75f3f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="75f3f-112">Bu cmdlet eylem kuralını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="75f3f-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="75f3f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75f3f-113">PARAMETERS</span></span>

### <span data-ttu-id="75f3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f3f-114">-DefaultProfile</span></span>
<span data-ttu-id="75f3f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75f3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f3f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75f3f-116">-InputObject</span></span>
<span data-ttu-id="75f3f-117">Eylem kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="75f3f-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="75f3f-118">-Name</span></span>
<span data-ttu-id="75f3f-119">Eylem kuralı adı</span><span class="sxs-lookup"><span data-stu-id="75f3f-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f3f-120">-ResourceGroupName</span></span>
<span data-ttu-id="75f3f-121">Eylem kuralı adı</span><span class="sxs-lookup"><span data-stu-id="75f3f-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="75f3f-122">-ResourceId</span></span>
<span data-ttu-id="75f3f-123">Eylem kuralının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="75f3f-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-124">-Durum</span><span class="sxs-lookup"><span data-stu-id="75f3f-124">-Status</span></span>
<span data-ttu-id="75f3f-125">Eylem kuralı durumu</span><span class="sxs-lookup"><span data-stu-id="75f3f-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="75f3f-126">-Tag</span></span>
<span data-ttu-id="75f3f-127">Eylem kuralı etiketleri</span><span class="sxs-lookup"><span data-stu-id="75f3f-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f3f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="75f3f-128">-Confirm</span></span>
<span data-ttu-id="75f3f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75f3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f3f-130">-WhatIf</span></span>
<span data-ttu-id="75f3f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75f3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f3f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75f3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f3f-133">CommonParameters</span></span>
<span data-ttu-id="75f3f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75f3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f3f-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75f3f-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f3f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75f3f-136">INPUTS</span></span>

### <span data-ttu-id="75f3f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75f3f-137">System.String</span></span>

### <span data-ttu-id="75f3f-138">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="75f3f-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="75f3f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75f3f-139">OUTPUTS</span></span>

### <span data-ttu-id="75f3f-140">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="75f3f-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="75f3f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75f3f-141">NOTES</span></span>

## <span data-ttu-id="75f3f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75f3f-142">RELATED LINKS</span></span>
