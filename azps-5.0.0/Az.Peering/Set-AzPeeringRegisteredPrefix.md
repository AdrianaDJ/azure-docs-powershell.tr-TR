---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278074"
---
# <span data-ttu-id="22145-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="22145-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="22145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22145-102">SYNOPSIS</span></span>
<span data-ttu-id="22145-103">Üst eşleme kaynağından kaydedilen bir öneki ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22145-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="22145-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22145-104">SYNTAX</span></span>

### <span data-ttu-id="22145-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22145-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22145-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="22145-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22145-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="22145-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22145-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="22145-108">DESCRIPTION</span></span>
<span data-ttu-id="22145-109">Üst eşleme kaynağından kaydedilen bir önekin güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="22145-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="22145-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22145-110">EXAMPLES</span></span>

### <span data-ttu-id="22145-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22145-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="22145-112">Öneki kaynak kimliğiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="22145-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="22145-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22145-113">PARAMETERS</span></span>

### <span data-ttu-id="22145-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="22145-114">-AsJob</span></span>
<span data-ttu-id="22145-115">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="22145-115">Run in the background.</span></span>

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

### <span data-ttu-id="22145-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22145-116">-DefaultProfile</span></span>
<span data-ttu-id="22145-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22145-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22145-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22145-118">-InputObject</span></span>
<span data-ttu-id="22145-119">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="22145-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22145-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="22145-120">-Name</span></span>
<span data-ttu-id="22145-121">Önek adı.</span><span class="sxs-lookup"><span data-stu-id="22145-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22145-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="22145-122">-PeeringName</span></span>
<span data-ttu-id="22145-123">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="22145-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22145-124">-Önek</span><span class="sxs-lookup"><span data-stu-id="22145-124">-Prefix</span></span>
<span data-ttu-id="22145-125">Oturum IPv4 öneki</span><span class="sxs-lookup"><span data-stu-id="22145-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="22145-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22145-126">-ResourceGroupName</span></span>
<span data-ttu-id="22145-127">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="22145-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22145-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="22145-128">-ResourceId</span></span>
<span data-ttu-id="22145-129">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="22145-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22145-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="22145-130">-Confirm</span></span>
<span data-ttu-id="22145-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22145-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22145-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22145-132">-WhatIf</span></span>
<span data-ttu-id="22145-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22145-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22145-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22145-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22145-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22145-135">CommonParameters</span></span>
<span data-ttu-id="22145-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22145-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22145-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22145-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22145-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22145-138">INPUTS</span></span>

### <span data-ttu-id="22145-139">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22145-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="22145-140">System. String</span><span class="sxs-lookup"><span data-stu-id="22145-140">System.String</span></span>

## <span data-ttu-id="22145-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22145-141">OUTPUTS</span></span>

### <span data-ttu-id="22145-142">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22145-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="22145-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22145-143">NOTES</span></span>

## <span data-ttu-id="22145-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22145-144">RELATED LINKS</span></span>
