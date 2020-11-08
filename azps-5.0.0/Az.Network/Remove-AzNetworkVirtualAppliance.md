---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276884"
---
# <span data-ttu-id="6c845-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6c845-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6c845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c845-102">SYNOPSIS</span></span>
<span data-ttu-id="6c845-103">Ağ sanal bir gereç kaynağını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6c845-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6c845-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c845-104">SYNTAX</span></span>

### <span data-ttu-id="6c845-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c845-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c845-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6c845-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c845-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c845-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c845-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c845-108">DESCRIPTION</span></span>
<span data-ttu-id="6c845-109">Remove-AzNetworkVirtualAppliance komutu bir ağ sanal gereç kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6c845-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6c845-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c845-110">EXAMPLES</span></span>

### <span data-ttu-id="6c845-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6c845-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="6c845-112">Ağ sanal bir gereç kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="6c845-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6c845-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c845-113">PARAMETERS</span></span>

### <span data-ttu-id="6c845-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6c845-114">-AsJob</span></span>
<span data-ttu-id="6c845-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6c845-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c845-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c845-116">-DefaultProfile</span></span>
<span data-ttu-id="6c845-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c845-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c845-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6c845-118">-Force</span></span>
<span data-ttu-id="6c845-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="6c845-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6c845-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c845-120">-Name</span></span>
<span data-ttu-id="6c845-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6c845-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c845-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6c845-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="6c845-123">Kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6c845-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c845-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6c845-124">-PassThru</span></span>
<span data-ttu-id="6c845-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6c845-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6c845-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6c845-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c845-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c845-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c845-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6c845-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c845-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6c845-129">-ResourceId</span></span>
<span data-ttu-id="6c845-130">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6c845-130">The Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c845-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c845-131">-Confirm</span></span>
<span data-ttu-id="6c845-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c845-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c845-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c845-133">-WhatIf</span></span>
<span data-ttu-id="6c845-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c845-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c845-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c845-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c845-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c845-136">CommonParameters</span></span>
<span data-ttu-id="6c845-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c845-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c845-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6c845-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c845-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c845-139">INPUTS</span></span>

### <span data-ttu-id="6c845-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6c845-140">System.String</span></span>

### <span data-ttu-id="6c845-141">Microsoft. Azure. Commands. Network. model. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6c845-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6c845-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c845-142">OUTPUTS</span></span>

### <span data-ttu-id="6c845-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c845-143">System.Boolean</span></span>

## <span data-ttu-id="6c845-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c845-144">NOTES</span></span>

## <span data-ttu-id="6c845-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c845-145">RELATED LINKS</span></span>
