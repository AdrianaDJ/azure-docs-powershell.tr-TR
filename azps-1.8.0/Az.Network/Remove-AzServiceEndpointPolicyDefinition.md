---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: c907c60619f5a0a2fc5f0620f086ba0b99ca62ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760114"
---
# <span data-ttu-id="e4867-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e4867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4867-102">SYNOPSIS</span></span>
<span data-ttu-id="e4867-103">Hizmet uç noktası ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4867-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="e4867-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4867-104">SYNTAX</span></span>

### <span data-ttu-id="e4867-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4867-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4867-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e4867-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4867-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4867-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4867-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4867-108">DESCRIPTION</span></span>
<span data-ttu-id="e4867-109">**Remove-AzServiceEndpointPolicy** cmdlet 'i, hizmet uç nokta ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4867-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="e4867-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4867-110">EXAMPLES</span></span>

### <span data-ttu-id="e4867-111">Örnek 1: ad kullanan bir hizmet uç nokta ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="e4867-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="e4867-112">Bu komut, ad</span><span class="sxs-lookup"><span data-stu-id="e4867-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="e4867-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4867-113">PARAMETERS</span></span>

### <span data-ttu-id="e4867-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4867-114">-DefaultProfile</span></span>
<span data-ttu-id="e4867-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4867-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4867-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4867-116">-InputObject</span></span>
<span data-ttu-id="e4867-117">Hizmet bitiş noktası İlkesi tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e4867-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4867-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4867-118">-Name</span></span>
<span data-ttu-id="e4867-119">Hizmet uç noktası tanımının adı</span><span class="sxs-lookup"><span data-stu-id="e4867-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4867-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4867-120">-ResourceId</span></span>
<span data-ttu-id="e4867-121">Hizmet uç noktası tanımının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e4867-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4867-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e4867-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e4867-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e4867-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4867-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4867-124">-Confirm</span></span>
<span data-ttu-id="e4867-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4867-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4867-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4867-126">-WhatIf</span></span>
<span data-ttu-id="e4867-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4867-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4867-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4867-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4867-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4867-129">CommonParameters</span></span>
<span data-ttu-id="e4867-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4867-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4867-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4867-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4867-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4867-132">INPUTS</span></span>

### <span data-ttu-id="e4867-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e4867-133">System.String</span></span>

### <span data-ttu-id="e4867-134">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="e4867-135">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e4867-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e4867-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4867-136">OUTPUTS</span></span>

### <span data-ttu-id="e4867-137">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e4867-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e4867-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4867-138">NOTES</span></span>

## <span data-ttu-id="e4867-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4867-139">RELATED LINKS</span></span>

[<span data-ttu-id="e4867-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e4867-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e4867-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e4867-143">Set-Azhizmetiendpointpolicydefinition</span><span class="sxs-lookup"><span data-stu-id="e4867-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)