---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 1812a51492b834df4152d492960444c12d2bccc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933172"
---
# <span data-ttu-id="bb57f-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="bb57f-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="bb57f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb57f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb57f-103">Bir SignalR hizmetini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="bb57f-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="bb57f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb57f-104">SYNTAX</span></span>

### <span data-ttu-id="bb57f-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb57f-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb57f-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bb57f-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb57f-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="bb57f-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb57f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb57f-108">DESCRIPTION</span></span>
<span data-ttu-id="bb57f-109">Bir SignalR hizmetini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="bb57f-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="bb57f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb57f-110">EXAMPLES</span></span>

### <span data-ttu-id="bb57f-111">Belirli bir SignalR hizmetini yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="bb57f-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="bb57f-112">Varsayılan kaynak grubu \` set-AzDefault-ResourceGroupName myResourceGroup ile ayarlanabilir \` .</span><span class="sxs-lookup"><span data-stu-id="bb57f-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="bb57f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb57f-113">PARAMETERS</span></span>

### <span data-ttu-id="bb57f-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="bb57f-114">-AsJob</span></span>
<span data-ttu-id="bb57f-115">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="bb57f-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="bb57f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb57f-116">-DefaultProfile</span></span>
<span data-ttu-id="bb57f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb57f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb57f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb57f-118">-InputObject</span></span>
<span data-ttu-id="bb57f-119">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bb57f-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb57f-120">-Name</span></span>
<span data-ttu-id="bb57f-121">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="bb57f-121">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb57f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb57f-122">-PassThru</span></span>
<span data-ttu-id="bb57f-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="bb57f-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bb57f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb57f-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb57f-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bb57f-125">The resource group name.</span></span>
<span data-ttu-id="bb57f-126">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="bb57f-126">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb57f-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb57f-127">-ResourceId</span></span>
<span data-ttu-id="bb57f-128">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb57f-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb57f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb57f-129">-Confirm</span></span>
<span data-ttu-id="bb57f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb57f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb57f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb57f-131">-WhatIf</span></span>
<span data-ttu-id="bb57f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb57f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb57f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb57f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb57f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb57f-134">CommonParameters</span></span>
<span data-ttu-id="bb57f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb57f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb57f-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb57f-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb57f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb57f-137">INPUTS</span></span>

### <span data-ttu-id="bb57f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb57f-138">System.String</span></span>

### <span data-ttu-id="bb57f-139">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="bb57f-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="bb57f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb57f-140">OUTPUTS</span></span>

### <span data-ttu-id="bb57f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb57f-141">System.Boolean</span></span>

## <span data-ttu-id="bb57f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb57f-142">NOTES</span></span>

## <span data-ttu-id="bb57f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb57f-143">RELATED LINKS</span></span>