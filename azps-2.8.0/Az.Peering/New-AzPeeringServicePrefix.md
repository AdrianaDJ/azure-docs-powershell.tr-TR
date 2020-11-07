---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 2e85cc87f0f0b1fb0451e3697f6ffef3b317124b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932843"
---
# <span data-ttu-id="812ee-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="812ee-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="812ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812ee-102">SYNOPSIS</span></span>
<span data-ttu-id="812ee-103">Yeni bir eşleme hizmeti öneki oluşturur</span><span class="sxs-lookup"><span data-stu-id="812ee-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="812ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="812ee-104">SYNTAX</span></span>

### <span data-ttu-id="812ee-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="812ee-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812ee-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812ee-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812ee-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="812ee-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="812ee-108">DESCRIPTION</span></span>
<span data-ttu-id="812ee-109">Eşleme hizmeti nesnesiyle ilişkilendirilmiş eşleme hizmeti önekini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="812ee-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="812ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="812ee-110">EXAMPLES</span></span>

### <span data-ttu-id="812ee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="812ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="812ee-112">Eşleme hizmeti nesnesinden önek oluşturur</span><span class="sxs-lookup"><span data-stu-id="812ee-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="812ee-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="812ee-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="812ee-114">Eşleme hizmeti kaynak kimliğinden bir önek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="812ee-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="812ee-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="812ee-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="812ee-116">Eşleme hizmeti kaynak grubu adı ve adından önek oluşturur</span><span class="sxs-lookup"><span data-stu-id="812ee-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="812ee-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="812ee-117">PARAMETERS</span></span>

### <span data-ttu-id="812ee-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="812ee-118">-AsJob</span></span>
<span data-ttu-id="812ee-119">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="812ee-119">Run in the background.</span></span>

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

### <span data-ttu-id="812ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812ee-120">-DefaultProfile</span></span>
<span data-ttu-id="812ee-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="812ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="812ee-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="812ee-122">-Name</span></span>
<span data-ttu-id="812ee-123">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="812ee-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-124">-Peeringserviceıd</span><span class="sxs-lookup"><span data-stu-id="812ee-124">-PeeringServiceId</span></span>
<span data-ttu-id="812ee-125">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="812ee-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-126">-Peeringhizmetadı</span><span class="sxs-lookup"><span data-stu-id="812ee-126">-PeeringServiceName</span></span>
<span data-ttu-id="812ee-127">Eşleme hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="812ee-127">The peering service name.</span></span>
<span data-ttu-id="812ee-128">Yeni bir eşleme hizmeti Get-AzPeeringService veya liste için New-AzPeeringService cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="812ee-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="812ee-129">-PeeringServiceObject</span></span>
<span data-ttu-id="812ee-130">Get-AzPeeringService kullanma</span><span class="sxs-lookup"><span data-stu-id="812ee-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-131">-Önek</span><span class="sxs-lookup"><span data-stu-id="812ee-131">-Prefix</span></span>
<span data-ttu-id="812ee-132">Oturum IPv4 öneki</span><span class="sxs-lookup"><span data-stu-id="812ee-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812ee-133">-ResourceGroupName</span></span>
<span data-ttu-id="812ee-134">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="812ee-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812ee-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="812ee-135">-Confirm</span></span>
<span data-ttu-id="812ee-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="812ee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812ee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812ee-137">-WhatIf</span></span>
<span data-ttu-id="812ee-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="812ee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812ee-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="812ee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812ee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812ee-140">CommonParameters</span></span>
<span data-ttu-id="812ee-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="812ee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812ee-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="812ee-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812ee-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="812ee-143">INPUTS</span></span>

### <span data-ttu-id="812ee-144">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="812ee-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="812ee-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="812ee-145">OUTPUTS</span></span>

### <span data-ttu-id="812ee-146">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="812ee-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="812ee-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="812ee-147">NOTES</span></span>

## <span data-ttu-id="812ee-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="812ee-148">RELATED LINKS</span></span>
