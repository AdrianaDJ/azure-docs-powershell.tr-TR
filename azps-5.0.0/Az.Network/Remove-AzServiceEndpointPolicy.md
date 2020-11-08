---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278304"
---
# <span data-ttu-id="e869a-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e869a-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="e869a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e869a-102">SYNOPSIS</span></span>
<span data-ttu-id="e869a-103">Hizmet uç noktası ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e869a-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="e869a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e869a-104">SYNTAX</span></span>

### <span data-ttu-id="e869a-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e869a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e869a-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e869a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e869a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e869a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e869a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e869a-108">DESCRIPTION</span></span>
<span data-ttu-id="e869a-109">**Remove-AzServiceEndpointPolicy** cmdlet 'i, hizmet uç nokta ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e869a-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="e869a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e869a-110">EXAMPLES</span></span>

### <span data-ttu-id="e869a-111">Örnek 1: ad kullanan bir hizmet uç nokta ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="e869a-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="e869a-112">Bu komut, "resourcegroup1" adıyla resourcegroup 'a ait olan Policy1 ad uç noktası ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="e869a-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="e869a-113">Örnek 2: giriş nesnesini kullanarak hizmet uç nokta ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="e869a-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="e869a-114">Bu komut, "resourcegroup1" adıyla bir Policy1</span><span class="sxs-lookup"><span data-stu-id="e869a-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="e869a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e869a-115">PARAMETERS</span></span>

### <span data-ttu-id="e869a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e869a-116">-DefaultProfile</span></span>
<span data-ttu-id="e869a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e869a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e869a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e869a-118">-Force</span></span>
<span data-ttu-id="e869a-119">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="e869a-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e869a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e869a-120">-InputObject</span></span>
<span data-ttu-id="e869a-121">Hizmet bitiş noktası ilke nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e869a-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e869a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e869a-122">-Name</span></span>
<span data-ttu-id="e869a-123">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="e869a-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e869a-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e869a-124">-PassThru</span></span>
<span data-ttu-id="e869a-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e869a-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e869a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e869a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e869a-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e869a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e869a-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e869a-128">-ResourceId</span></span>
<span data-ttu-id="e869a-129">Hizmet bitiş noktası ilkesinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e869a-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="e869a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e869a-130">-Confirm</span></span>
<span data-ttu-id="e869a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e869a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e869a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e869a-132">-WhatIf</span></span>
<span data-ttu-id="e869a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e869a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e869a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e869a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e869a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e869a-135">CommonParameters</span></span>
<span data-ttu-id="e869a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e869a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e869a-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e869a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e869a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e869a-138">INPUTS</span></span>

### <span data-ttu-id="e869a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e869a-139">System.String</span></span>

### <span data-ttu-id="e869a-140">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e869a-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e869a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e869a-141">OUTPUTS</span></span>

### <span data-ttu-id="e869a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e869a-142">System.Boolean</span></span>

## <span data-ttu-id="e869a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e869a-143">NOTES</span></span>

## <span data-ttu-id="e869a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e869a-144">RELATED LINKS</span></span>

[<span data-ttu-id="e869a-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e869a-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e869a-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e869a-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="e869a-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e869a-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
