---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277528"
---
# <span data-ttu-id="1e536-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="1e536-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="1e536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e536-102">SYNOPSIS</span></span>
<span data-ttu-id="1e536-103">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1e536-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="1e536-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e536-104">SYNTAX</span></span>

### <span data-ttu-id="1e536-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e536-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e536-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1e536-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e536-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="1e536-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e536-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e536-108">DESCRIPTION</span></span>
<span data-ttu-id="1e536-109">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="1e536-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="1e536-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e536-110">EXAMPLES</span></span>

### <span data-ttu-id="1e536-111">SignalR hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1e536-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="1e536-112">Kanaldan tüm SignalR hizmetini kaldır</span><span class="sxs-lookup"><span data-stu-id="1e536-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="1e536-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e536-113">PARAMETERS</span></span>

### <span data-ttu-id="1e536-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="1e536-114">-AsJob</span></span>
<span data-ttu-id="1e536-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1e536-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e536-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e536-116">-DefaultProfile</span></span>
<span data-ttu-id="1e536-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e536-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e536-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e536-118">-InputObject</span></span>
<span data-ttu-id="1e536-119">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1e536-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="1e536-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e536-120">-Name</span></span>
<span data-ttu-id="1e536-121">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="1e536-121">SignalR service name.</span></span>

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

### <span data-ttu-id="1e536-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1e536-122">-PassThru</span></span>
<span data-ttu-id="1e536-123">Kaldırma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e536-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="1e536-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e536-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e536-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1e536-125">Resource group name.</span></span>

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

### <span data-ttu-id="1e536-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1e536-126">-ResourceId</span></span>
<span data-ttu-id="1e536-127">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1e536-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="1e536-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e536-128">-Confirm</span></span>
<span data-ttu-id="1e536-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e536-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e536-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e536-130">-WhatIf</span></span>
<span data-ttu-id="1e536-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e536-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e536-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e536-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e536-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e536-133">CommonParameters</span></span>
<span data-ttu-id="1e536-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e536-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e536-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e536-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e536-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e536-136">INPUTS</span></span>

### <span data-ttu-id="1e536-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1e536-137">System.String</span></span>
### <span data-ttu-id="1e536-138">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1e536-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="1e536-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e536-139">OUTPUTS</span></span>

### <span data-ttu-id="1e536-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e536-140">System.Boolean</span></span>
## <span data-ttu-id="1e536-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e536-141">NOTES</span></span>

## <span data-ttu-id="1e536-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e536-142">RELATED LINKS</span></span>
