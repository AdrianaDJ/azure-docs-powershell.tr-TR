---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 075c8e7604ab800e8f1065ff4d025b105d8effc3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932401"
---
# <span data-ttu-id="79710-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="79710-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="79710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79710-102">SYNOPSIS</span></span>
<span data-ttu-id="79710-103">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="79710-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="79710-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79710-104">SYNTAX</span></span>

### <span data-ttu-id="79710-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79710-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79710-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="79710-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79710-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="79710-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79710-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79710-108">DESCRIPTION</span></span>
<span data-ttu-id="79710-109">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="79710-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="79710-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79710-110">EXAMPLES</span></span>

### <span data-ttu-id="79710-111">SignalR hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="79710-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="79710-112">Kanaldan tüm SignalR hizmetini kaldır</span><span class="sxs-lookup"><span data-stu-id="79710-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="79710-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79710-113">PARAMETERS</span></span>

### <span data-ttu-id="79710-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="79710-114">-AsJob</span></span>
<span data-ttu-id="79710-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="79710-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79710-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79710-116">-DefaultProfile</span></span>
<span data-ttu-id="79710-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79710-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79710-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79710-118">-InputObject</span></span>
<span data-ttu-id="79710-119">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="79710-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="79710-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="79710-120">-Name</span></span>
<span data-ttu-id="79710-121">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="79710-121">SignalR service name.</span></span>

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

### <span data-ttu-id="79710-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="79710-122">-PassThru</span></span>
<span data-ttu-id="79710-123">Kaldırma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="79710-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79710-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79710-124">-ResourceGroupName</span></span>
<span data-ttu-id="79710-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="79710-125">Resource group name.</span></span>

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

### <span data-ttu-id="79710-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="79710-126">-ResourceId</span></span>
<span data-ttu-id="79710-127">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="79710-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="79710-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="79710-128">-Confirm</span></span>
<span data-ttu-id="79710-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79710-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79710-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79710-130">-WhatIf</span></span>
<span data-ttu-id="79710-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79710-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79710-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79710-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79710-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79710-133">CommonParameters</span></span>
<span data-ttu-id="79710-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79710-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79710-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79710-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79710-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79710-136">INPUTS</span></span>

### <span data-ttu-id="79710-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79710-137">System.String</span></span>
### <span data-ttu-id="79710-138">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="79710-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="79710-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79710-139">OUTPUTS</span></span>

### <span data-ttu-id="79710-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79710-140">System.Boolean</span></span>
## <span data-ttu-id="79710-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79710-141">NOTES</span></span>

## <span data-ttu-id="79710-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79710-142">RELATED LINKS</span></span>