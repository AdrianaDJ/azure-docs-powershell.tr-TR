---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265943"
---
# <span data-ttu-id="6a89a-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a89a-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="6a89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a89a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a89a-103">NAT ağ geçidi kaynağını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6a89a-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="6a89a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a89a-104">SYNTAX</span></span>

### <span data-ttu-id="6a89a-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a89a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a89a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a89a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a89a-107">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6a89a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a89a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a89a-108">DESCRIPTION</span></span>
<span data-ttu-id="6a89a-109">NAT ağ geçidi kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6a89a-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="6a89a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a89a-110">EXAMPLES</span></span>

### <span data-ttu-id="6a89a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a89a-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="6a89a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a89a-112">PARAMETERS</span></span>

### <span data-ttu-id="6a89a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6a89a-113">-AsJob</span></span>
<span data-ttu-id="6a89a-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6a89a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a89a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a89a-115">-DefaultProfile</span></span>
<span data-ttu-id="6a89a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a89a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a89a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6a89a-117">-Force</span></span>
<span data-ttu-id="6a89a-118">Kaynağı silmek istiyorsanız onay isteyin.</span><span class="sxs-lookup"><span data-stu-id="6a89a-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="6a89a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a89a-119">-InputObject</span></span>
<span data-ttu-id="6a89a-120">NAT ağ geçidi kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a89a-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="6a89a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a89a-121">-Name</span></span>
<span data-ttu-id="6a89a-122">NAT ağ geçidi kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="6a89a-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="6a89a-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6a89a-123">-PassThru</span></span>
<span data-ttu-id="6a89a-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a89a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a89a-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6a89a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a89a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a89a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a89a-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a89a-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6a89a-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6a89a-128">-ResourceId</span></span>
<span data-ttu-id="6a89a-129">NAT ağ geçidiyle ilişkili kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6a89a-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="6a89a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a89a-130">-Confirm</span></span>
<span data-ttu-id="6a89a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a89a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a89a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a89a-132">-WhatIf</span></span>
<span data-ttu-id="6a89a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a89a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a89a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a89a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a89a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a89a-135">CommonParameters</span></span>
<span data-ttu-id="6a89a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a89a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a89a-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a89a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a89a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a89a-138">INPUTS</span></span>

### <span data-ttu-id="6a89a-139">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a89a-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="6a89a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6a89a-140">System.String</span></span>

## <span data-ttu-id="6a89a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a89a-141">OUTPUTS</span></span>

### <span data-ttu-id="6a89a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a89a-142">System.Boolean</span></span>

## <span data-ttu-id="6a89a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a89a-143">NOTES</span></span>

## <span data-ttu-id="6a89a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a89a-144">RELATED LINKS</span></span>
