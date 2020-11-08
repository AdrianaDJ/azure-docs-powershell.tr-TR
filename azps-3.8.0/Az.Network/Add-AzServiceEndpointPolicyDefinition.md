---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098018"
---
# <span data-ttu-id="0424b-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0424b-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="0424b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0424b-102">SYNOPSIS</span></span>
<span data-ttu-id="0424b-103">Belirtilen ilkeye hizmet uç noktası ilke tanımı ekler.</span><span class="sxs-lookup"><span data-stu-id="0424b-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="0424b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0424b-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0424b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0424b-105">DESCRIPTION</span></span>
<span data-ttu-id="0424b-106">**Add-AzServiceEndpointPolicyDefinition** cmdlet 'i ilkeye bir hizmet uç noktası ilke tanımı ekler.</span><span class="sxs-lookup"><span data-stu-id="0424b-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="0424b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0424b-107">EXAMPLES</span></span>

### <span data-ttu-id="0424b-108">Örnek 1: hizmet uç noktası ilkesinde hizmet uç noktası İlkesi tanımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0424b-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="0424b-109">Bu komut, ad ServiceEndpointPolicyDefinition1, hizmet Microsoft. Storage, hizmet kaynakları abonelikleri/sub1 ve açıklaması "yeni tanım" olan hizmet uç noktası İlkesi tanımını, ResourceGroup01 adlı kaynak grubuna ait ve $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0424b-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="0424b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0424b-110">PARAMETERS</span></span>

### <span data-ttu-id="0424b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0424b-111">-DefaultProfile</span></span>
<span data-ttu-id="0424b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0424b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0424b-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0424b-113">-Description</span></span>
<span data-ttu-id="0424b-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="0424b-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0424b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0424b-115">-Name</span></span>
<span data-ttu-id="0424b-116">Hizmet uç noktası ilke tanımının adı</span><span class="sxs-lookup"><span data-stu-id="0424b-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="0424b-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="0424b-117">-Service</span></span>
<span data-ttu-id="0424b-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="0424b-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0424b-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0424b-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="0424b-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0424b-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="0424b-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="0424b-121">-ServiceResource</span></span>
<span data-ttu-id="0424b-122">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="0424b-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0424b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0424b-123">-Confirm</span></span>
<span data-ttu-id="0424b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0424b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0424b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0424b-125">-WhatIf</span></span>
<span data-ttu-id="0424b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0424b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0424b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0424b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0424b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0424b-128">CommonParameters</span></span>
<span data-ttu-id="0424b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0424b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0424b-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0424b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0424b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0424b-131">INPUTS</span></span>

### <span data-ttu-id="0424b-132">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0424b-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0424b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0424b-133">OUTPUTS</span></span>

### <span data-ttu-id="0424b-134">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0424b-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0424b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0424b-135">NOTES</span></span>

## <span data-ttu-id="0424b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0424b-136">RELATED LINKS</span></span>

[<span data-ttu-id="0424b-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0424b-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="0424b-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0424b-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="0424b-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0424b-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="0424b-140">Set-Azhizmetiendpointpolicydefinition</span><span class="sxs-lookup"><span data-stu-id="0424b-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
