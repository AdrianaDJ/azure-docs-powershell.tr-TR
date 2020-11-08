---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097973"
---
# <span data-ttu-id="a0024-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a0024-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="a0024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0024-102">SYNOPSIS</span></span>
<span data-ttu-id="a0024-103">Genel IP adresi, genel IP öneki ve ıdzamanzamansayısı</span><span class="sxs-lookup"><span data-stu-id="a0024-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="a0024-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0024-104">SYNTAX</span></span>

### <span data-ttu-id="a0024-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0024-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0024-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a0024-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0024-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0024-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0024-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0024-108">DESCRIPTION</span></span>
<span data-ttu-id="a0024-109">Genel IP adresi, genel IP öneki ve ıdzamanzamansayısı</span><span class="sxs-lookup"><span data-stu-id="a0024-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="a0024-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0024-110">EXAMPLES</span></span>

### <span data-ttu-id="a0024-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0024-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="a0024-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0024-112">PARAMETERS</span></span>

### <span data-ttu-id="a0024-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a0024-113">-AsJob</span></span>
<span data-ttu-id="a0024-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a0024-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0024-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0024-115">-DefaultProfile</span></span>
<span data-ttu-id="a0024-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0024-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0024-117">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="a0024-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a0024-118">NAT ağ geçidinin Boşta durma süresi.</span><span class="sxs-lookup"><span data-stu-id="a0024-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="a0024-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0024-119">-InputObject</span></span>
<span data-ttu-id="a0024-120">NAT ağ geçidi kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0024-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="a0024-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0024-121">-Name</span></span>
<span data-ttu-id="a0024-122">NAT ağ geçidi kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="a0024-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="a0024-123">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="a0024-123">-PublicIpAddress</span></span>
<span data-ttu-id="a0024-124">NAT ağ geçidi kaynağıyla ilişkili ortak IP adresleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="a0024-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a0024-125">-Publicıpprefix</span><span class="sxs-lookup"><span data-stu-id="a0024-125">-PublicIpPrefix</span></span>
<span data-ttu-id="a0024-126">NAT ağ geçidi kaynağıyla ilişkili genel IP önekleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="a0024-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a0024-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0024-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0024-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0024-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a0024-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0024-129">-ResourceId</span></span>
<span data-ttu-id="a0024-130">NAT ağ geçidi kaynağının kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0024-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="a0024-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0024-131">-Confirm</span></span>
<span data-ttu-id="a0024-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0024-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0024-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0024-133">-WhatIf</span></span>
<span data-ttu-id="a0024-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0024-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0024-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0024-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0024-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0024-136">CommonParameters</span></span>
<span data-ttu-id="a0024-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0024-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0024-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0024-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0024-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0024-139">INPUTS</span></span>

### <span data-ttu-id="a0024-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a0024-140">System.String</span></span>

### <span data-ttu-id="a0024-141">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a0024-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a0024-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0024-142">OUTPUTS</span></span>

### <span data-ttu-id="a0024-143">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a0024-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a0024-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0024-144">NOTES</span></span>

## <span data-ttu-id="a0024-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0024-145">RELATED LINKS</span></span>
