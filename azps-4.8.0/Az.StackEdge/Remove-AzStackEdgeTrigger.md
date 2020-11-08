---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268685"
---
# <span data-ttu-id="6153f-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6153f-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="6153f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6153f-102">SYNOPSIS</span></span>
<span data-ttu-id="6153f-103">Cihazda varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6153f-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="6153f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6153f-104">SYNTAX</span></span>

### <span data-ttu-id="6153f-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6153f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6153f-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6153f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6153f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6153f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6153f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6153f-108">DESCRIPTION</span></span>
<span data-ttu-id="6153f-109">**Remove-AzStackEdgeTrigger** cmdlet 'ı, yığın uç cihazında varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6153f-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="6153f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6153f-110">EXAMPLES</span></span>

### <span data-ttu-id="6153f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6153f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="6153f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6153f-112">PARAMETERS</span></span>

### <span data-ttu-id="6153f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6153f-113">-AsJob</span></span>
<span data-ttu-id="6153f-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6153f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6153f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6153f-115">-DefaultProfile</span></span>
<span data-ttu-id="6153f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6153f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6153f-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="6153f-117">-DeviceName</span></span>
<span data-ttu-id="6153f-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="6153f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6153f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6153f-119">-InputObject</span></span>
<span data-ttu-id="6153f-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6153f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6153f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6153f-121">-Name</span></span>
<span data-ttu-id="6153f-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="6153f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6153f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6153f-123">-PassThru</span></span>
<span data-ttu-id="6153f-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="6153f-124">returns true if successful</span></span>

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

### <span data-ttu-id="6153f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6153f-125">-ResourceGroupName</span></span>
<span data-ttu-id="6153f-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6153f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6153f-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6153f-127">-ResourceId</span></span>
<span data-ttu-id="6153f-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6153f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6153f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6153f-129">-Confirm</span></span>
<span data-ttu-id="6153f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6153f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6153f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6153f-131">-WhatIf</span></span>
<span data-ttu-id="6153f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6153f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6153f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6153f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6153f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6153f-134">CommonParameters</span></span>
<span data-ttu-id="6153f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6153f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6153f-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6153f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6153f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6153f-137">INPUTS</span></span>

### <span data-ttu-id="6153f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6153f-138">System.String</span></span>

### <span data-ttu-id="6153f-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="6153f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="6153f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6153f-140">OUTPUTS</span></span>

### <span data-ttu-id="6153f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6153f-141">System.Boolean</span></span>

## <span data-ttu-id="6153f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6153f-142">NOTES</span></span>

## <span data-ttu-id="6153f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6153f-143">RELATED LINKS</span></span>
