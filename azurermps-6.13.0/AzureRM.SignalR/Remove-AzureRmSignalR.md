---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590838"
---
# <span data-ttu-id="656d2-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="656d2-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="656d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="656d2-102">SYNOPSIS</span></span>
<span data-ttu-id="656d2-103">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="656d2-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="656d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="656d2-104">SYNTAX</span></span>

### <span data-ttu-id="656d2-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="656d2-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="656d2-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="656d2-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="656d2-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="656d2-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="656d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="656d2-108">DESCRIPTION</span></span>
<span data-ttu-id="656d2-109">Bir SignalR hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="656d2-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="656d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="656d2-110">EXAMPLES</span></span>

### <span data-ttu-id="656d2-111">SignalR hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="656d2-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="656d2-112">Kanaldan tüm SignalR hizmetini kaldır</span><span class="sxs-lookup"><span data-stu-id="656d2-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="656d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="656d2-113">PARAMETERS</span></span>

### <span data-ttu-id="656d2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="656d2-114">-AsJob</span></span>
<span data-ttu-id="656d2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="656d2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="656d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="656d2-116">-DefaultProfile</span></span>
<span data-ttu-id="656d2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="656d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656d2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="656d2-118">-InputObject</span></span>
<span data-ttu-id="656d2-119">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="656d2-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="656d2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="656d2-120">-Name</span></span>
<span data-ttu-id="656d2-121">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="656d2-121">SignalR service name.</span></span>

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

### <span data-ttu-id="656d2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="656d2-122">-PassThru</span></span>
<span data-ttu-id="656d2-123">Kaldırma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="656d2-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="656d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="656d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="656d2-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="656d2-125">Resource group name.</span></span>

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

### <span data-ttu-id="656d2-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="656d2-126">-ResourceId</span></span>
<span data-ttu-id="656d2-127">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="656d2-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="656d2-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="656d2-128">-Confirm</span></span>
<span data-ttu-id="656d2-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="656d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="656d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="656d2-130">-WhatIf</span></span>
<span data-ttu-id="656d2-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="656d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="656d2-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="656d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="656d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656d2-133">CommonParameters</span></span>
<span data-ttu-id="656d2-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="656d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656d2-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656d2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656d2-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="656d2-136">INPUTS</span></span>

### <span data-ttu-id="656d2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="656d2-137">System.String</span></span>
<span data-ttu-id="656d2-138">Parametreler: RESOURCEID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="656d2-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="656d2-139">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="656d2-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="656d2-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="656d2-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="656d2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="656d2-141">OUTPUTS</span></span>

### <span data-ttu-id="656d2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="656d2-142">System.Boolean</span></span>

## <span data-ttu-id="656d2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="656d2-143">NOTES</span></span>

## <span data-ttu-id="656d2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="656d2-144">RELATED LINKS</span></span>
