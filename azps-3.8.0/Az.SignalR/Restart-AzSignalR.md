---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 7fde60c0bd1f400dd332782b6fbb9a92fefae4a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096801"
---
# <span data-ttu-id="f39e4-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="f39e4-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="f39e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f39e4-103">Bir SignalR hizmetini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="f39e4-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="f39e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f39e4-104">SYNTAX</span></span>

### <span data-ttu-id="f39e4-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f39e4-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39e4-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f39e4-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39e4-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f39e4-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39e4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f39e4-108">DESCRIPTION</span></span>
<span data-ttu-id="f39e4-109">Bir SignalR hizmetini yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="f39e4-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="f39e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f39e4-110">EXAMPLES</span></span>

### <span data-ttu-id="f39e4-111">Belirli bir SignalR hizmetini yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="f39e4-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="f39e4-112">Varsayılan kaynak grubu \` set-AzDefault-ResourceGroupName myResourceGroup ile ayarlanabilir \` .</span><span class="sxs-lookup"><span data-stu-id="f39e4-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="f39e4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f39e4-113">PARAMETERS</span></span>

### <span data-ttu-id="f39e4-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f39e4-114">-AsJob</span></span>
<span data-ttu-id="f39e4-115">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f39e4-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="f39e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39e4-116">-DefaultProfile</span></span>
<span data-ttu-id="f39e4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f39e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f39e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f39e4-118">-InputObject</span></span>
<span data-ttu-id="f39e4-119">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f39e4-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f39e4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f39e4-120">-Name</span></span>
<span data-ttu-id="f39e4-121">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="f39e4-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="f39e4-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f39e4-122">-PassThru</span></span>
<span data-ttu-id="f39e4-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f39e4-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f39e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f39e4-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f39e4-125">The resource group name.</span></span>
<span data-ttu-id="f39e4-126">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f39e4-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="f39e4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f39e4-127">-ResourceId</span></span>
<span data-ttu-id="f39e4-128">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f39e4-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f39e4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f39e4-129">-Confirm</span></span>
<span data-ttu-id="f39e4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f39e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39e4-131">-WhatIf</span></span>
<span data-ttu-id="f39e4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f39e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39e4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f39e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39e4-134">CommonParameters</span></span>
<span data-ttu-id="f39e4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f39e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39e4-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f39e4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39e4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f39e4-137">INPUTS</span></span>

### <span data-ttu-id="f39e4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f39e4-138">System.String</span></span>

### <span data-ttu-id="f39e4-139">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f39e4-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f39e4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f39e4-140">OUTPUTS</span></span>

### <span data-ttu-id="f39e4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f39e4-141">System.Boolean</span></span>

## <span data-ttu-id="f39e4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f39e4-142">NOTES</span></span>

## <span data-ttu-id="f39e4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f39e4-143">RELATED LINKS</span></span>