---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104023"
---
# <span data-ttu-id="a307c-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a307c-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="a307c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a307c-102">SYNOPSIS</span></span>
<span data-ttu-id="a307c-103">NAT ağ geçidi kaynağını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a307c-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="a307c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a307c-104">SYNTAX</span></span>

### <span data-ttu-id="a307c-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a307c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a307c-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a307c-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a307c-107">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a307c-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a307c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a307c-108">DESCRIPTION</span></span>
<span data-ttu-id="a307c-109">NAT ağ geçidi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a307c-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="a307c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a307c-110">EXAMPLES</span></span>

### <span data-ttu-id="a307c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a307c-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="a307c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a307c-112">PARAMETERS</span></span>

### <span data-ttu-id="a307c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a307c-113">-AsJob</span></span>
<span data-ttu-id="a307c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a307c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a307c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a307c-115">-DefaultProfile</span></span>
<span data-ttu-id="a307c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a307c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a307c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a307c-117">-Force</span></span>
<span data-ttu-id="a307c-118">Kaynağı silmek istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="a307c-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="a307c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a307c-119">-InputObject</span></span>
<span data-ttu-id="a307c-120">NAT ağ geçidi kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a307c-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a307c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a307c-121">-Name</span></span>
<span data-ttu-id="a307c-122">NAT ağ geçidi kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="a307c-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a307c-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a307c-123">-PassThru</span></span>
<span data-ttu-id="a307c-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a307c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a307c-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a307c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a307c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a307c-126">-ResourceGroupName</span></span>
<span data-ttu-id="a307c-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a307c-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a307c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a307c-128">-ResourceId</span></span>
<span data-ttu-id="a307c-129">NAT ağ geçidiyle ilişkili kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a307c-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a307c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="a307c-130">-Confirm</span></span>
<span data-ttu-id="a307c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a307c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a307c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a307c-132">-WhatIf</span></span>
<span data-ttu-id="a307c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a307c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a307c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a307c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a307c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a307c-135">CommonParameters</span></span>
<span data-ttu-id="a307c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a307c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a307c-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a307c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a307c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a307c-138">INPUTS</span></span>

### <span data-ttu-id="a307c-139">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a307c-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="a307c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a307c-140">System.String</span></span>

## <span data-ttu-id="a307c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a307c-141">OUTPUTS</span></span>

### <span data-ttu-id="a307c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a307c-142">System.Boolean</span></span>

## <span data-ttu-id="a307c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a307c-143">NOTES</span></span>

## <span data-ttu-id="a307c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a307c-144">RELATED LINKS</span></span>
