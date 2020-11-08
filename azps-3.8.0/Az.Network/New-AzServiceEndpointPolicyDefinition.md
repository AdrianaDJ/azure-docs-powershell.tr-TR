---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098725"
---
# <span data-ttu-id="89cd5-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="89cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="89cd5-103">Hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89cd5-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="89cd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89cd5-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89cd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="89cd5-106">**New-AzServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="89cd5-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="89cd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="89cd5-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="89cd5-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="89cd5-109">Bu komut, ad ServiceEndpointPolicyDefinition1, hizmet Microsoft. Storage, hizmet kaynakları abonelikleri/sub1 ve açıklaması "yeni tanım" olan ve ResourceGroup01 adlı kaynak grubuna ait olan hizmet uç noktası İlkesi tanımını oluşturur ve $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89cd5-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="89cd5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89cd5-110">PARAMETERS</span></span>

### <span data-ttu-id="89cd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cd5-111">-DefaultProfile</span></span>
<span data-ttu-id="89cd5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89cd5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89cd5-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="89cd5-113">-Description</span></span>
<span data-ttu-id="89cd5-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="89cd5-114">The description of the definition</span></span>

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

### <span data-ttu-id="89cd5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="89cd5-115">-Name</span></span>
<span data-ttu-id="89cd5-116">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="89cd5-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="89cd5-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="89cd5-117">-Service</span></span>
<span data-ttu-id="89cd5-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="89cd5-118">Name of the service</span></span>

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

### <span data-ttu-id="89cd5-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="89cd5-119">-ServiceResource</span></span>
<span data-ttu-id="89cd5-120">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="89cd5-120">List of service resources</span></span>

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

### <span data-ttu-id="89cd5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="89cd5-121">-Confirm</span></span>
<span data-ttu-id="89cd5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89cd5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cd5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cd5-123">-WhatIf</span></span>
<span data-ttu-id="89cd5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89cd5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89cd5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89cd5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89cd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cd5-126">CommonParameters</span></span>
<span data-ttu-id="89cd5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89cd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cd5-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89cd5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cd5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89cd5-129">INPUTS</span></span>

### <span data-ttu-id="89cd5-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89cd5-130">None</span></span>

## <span data-ttu-id="89cd5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89cd5-131">OUTPUTS</span></span>

### <span data-ttu-id="89cd5-132">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="89cd5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89cd5-133">NOTES</span></span>

## <span data-ttu-id="89cd5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89cd5-134">RELATED LINKS</span></span>

[<span data-ttu-id="89cd5-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="89cd5-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="89cd5-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="89cd5-138">Set-Azhizmetiendpointpolicydefinition</span><span class="sxs-lookup"><span data-stu-id="89cd5-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
