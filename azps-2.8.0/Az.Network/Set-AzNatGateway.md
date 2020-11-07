---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: 40a1d9c77d870971f8aa432735f556e89ad55e0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932197"
---
# <span data-ttu-id="5c1f2-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c1f2-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="5c1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1f2-103">Genel IP adresi, genel IP öneki ve ıdzamanzamansayısı</span><span class="sxs-lookup"><span data-stu-id="5c1f2-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="5c1f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c1f2-104">SYNTAX</span></span>

### <span data-ttu-id="5c1f2-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c1f2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1f2-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5c1f2-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c1f2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1f2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1f2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c1f2-108">DESCRIPTION</span></span>
<span data-ttu-id="5c1f2-109">Genel IP adresi, genel IP öneki ve ıdzamanzamansayısı</span><span class="sxs-lookup"><span data-stu-id="5c1f2-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="5c1f2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c1f2-110">EXAMPLES</span></span>

### <span data-ttu-id="5c1f2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c1f2-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="5c1f2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c1f2-112">PARAMETERS</span></span>

### <span data-ttu-id="5c1f2-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5c1f2-113">-AsJob</span></span>
<span data-ttu-id="5c1f2-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5c1f2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c1f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1f2-115">-DefaultProfile</span></span>
<span data-ttu-id="5c1f2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1f2-117">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="5c1f2-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5c1f2-118">NAT ağ geçidinin Boşta durma süresi.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c1f2-119">-InputObject</span></span>
<span data-ttu-id="5c1f2-120">NAT ağ geçidi kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c1f2-121">-Name</span></span>
<span data-ttu-id="5c1f2-122">NAT ağ geçidi kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="5c1f2-123">-PublicIpAddress</span></span>
<span data-ttu-id="5c1f2-124">NAT ağ geçidi kaynağıyla ilişkili ortak IP adresleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-125">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="5c1f2-125">-PublicIpPrefix</span></span>
<span data-ttu-id="5c1f2-126">NAT ağ geçidi kaynağıyla ilişkili genel IP önekleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c1f2-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5c1f2-129">-ResourceId</span></span>
<span data-ttu-id="5c1f2-130">NAT ağ geçidi kaynağının kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1f2-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c1f2-131">-Confirm</span></span>
<span data-ttu-id="5c1f2-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1f2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1f2-133">-WhatIf</span></span>
<span data-ttu-id="5c1f2-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1f2-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1f2-136">CommonParameters</span></span>
<span data-ttu-id="5c1f2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1f2-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c1f2-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1f2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c1f2-139">INPUTS</span></span>

### <span data-ttu-id="5c1f2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1f2-140">System.String</span></span>

### <span data-ttu-id="5c1f2-141">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c1f2-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="5c1f2-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c1f2-142">OUTPUTS</span></span>

### <span data-ttu-id="5c1f2-143">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c1f2-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="5c1f2-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c1f2-144">NOTES</span></span>

## <span data-ttu-id="5c1f2-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c1f2-145">RELATED LINKS</span></span>