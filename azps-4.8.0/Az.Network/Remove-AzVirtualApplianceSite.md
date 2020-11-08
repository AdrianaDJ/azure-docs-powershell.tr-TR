---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108877"
---
# <span data-ttu-id="5e601-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5e601-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="5e601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e601-102">SYNOPSIS</span></span>
<span data-ttu-id="5e601-103">Sanal bir gereç sitesini ağ sanal bir gereç kaynağından kaldırma.</span><span class="sxs-lookup"><span data-stu-id="5e601-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5e601-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e601-104">SYNTAX</span></span>

### <span data-ttu-id="5e601-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e601-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e601-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5e601-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e601-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e601-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e601-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e601-108">DESCRIPTION</span></span>
<span data-ttu-id="5e601-109">Remove-AzVirtualApplianceSite komutu sanal bir gereç sitesini ağ sanal bir gereç kaynağından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e601-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5e601-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e601-110">EXAMPLES</span></span>

### <span data-ttu-id="5e601-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e601-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="5e601-112">Sanal bir gereç sitesi kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="5e601-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="5e601-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e601-113">PARAMETERS</span></span>

### <span data-ttu-id="5e601-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="5e601-114">-AsJob</span></span>
<span data-ttu-id="5e601-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5e601-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e601-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e601-116">-DefaultProfile</span></span>
<span data-ttu-id="5e601-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e601-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e601-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5e601-118">-Force</span></span>
<span data-ttu-id="5e601-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5e601-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5e601-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e601-120">-Name</span></span>
<span data-ttu-id="5e601-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5e601-121">The resource name.</span></span>

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

### <span data-ttu-id="5e601-122">-Networkvirtualapplianceıd</span><span class="sxs-lookup"><span data-stu-id="5e601-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="5e601-123">Bu siteyle ilişkilendirilmiş ağ sanal aygıtının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e601-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="5e601-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5e601-124">-PassThru</span></span>
<span data-ttu-id="5e601-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e601-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5e601-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5e601-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e601-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e601-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e601-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5e601-128">The resource group name.</span></span>

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

### <span data-ttu-id="5e601-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5e601-129">-ResourceId</span></span>
<span data-ttu-id="5e601-130">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5e601-130">The resource id.</span></span>

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

### <span data-ttu-id="5e601-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5e601-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="5e601-132">Sanal Gereç sitesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5e601-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e601-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e601-133">-Confirm</span></span>
<span data-ttu-id="5e601-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e601-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e601-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e601-135">-WhatIf</span></span>
<span data-ttu-id="5e601-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e601-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e601-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e601-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e601-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e601-138">CommonParameters</span></span>
<span data-ttu-id="5e601-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e601-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e601-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e601-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e601-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e601-141">INPUTS</span></span>

### <span data-ttu-id="5e601-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5e601-142">System.String</span></span>

### <span data-ttu-id="5e601-143">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5e601-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="5e601-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e601-144">OUTPUTS</span></span>

### <span data-ttu-id="5e601-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e601-145">System.Boolean</span></span>

## <span data-ttu-id="5e601-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e601-146">NOTES</span></span>

## <span data-ttu-id="5e601-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e601-147">RELATED LINKS</span></span>
