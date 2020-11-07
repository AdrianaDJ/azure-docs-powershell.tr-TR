---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932337"
---
# <span data-ttu-id="34a31-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="34a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a31-102">SYNOPSIS</span></span>
<span data-ttu-id="34a31-103">Hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34a31-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="34a31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34a31-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34a31-105">DESCRIPTION</span></span>
<span data-ttu-id="34a31-106">**New-AzServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34a31-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="34a31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34a31-107">EXAMPLES</span></span>

### <span data-ttu-id="34a31-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="34a31-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="34a31-109">Bu komut, ad ServiceEndpointPolicyDefinition1, hizmet Microsoft. Storage, hizmet kaynakları abonelikleri/sub1 ve açıklaması "yeni tanım" olan ve ResourceGroup01 adlı kaynak grubuna ait olan hizmet uç noktası İlkesi tanımını oluşturur ve $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="34a31-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="34a31-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34a31-110">PARAMETERS</span></span>

### <span data-ttu-id="34a31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a31-111">-DefaultProfile</span></span>
<span data-ttu-id="34a31-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34a31-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34a31-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="34a31-113">-Description</span></span>
<span data-ttu-id="34a31-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="34a31-114">The description of the definition</span></span>

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

### <span data-ttu-id="34a31-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="34a31-115">-Name</span></span>
<span data-ttu-id="34a31-116">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="34a31-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="34a31-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="34a31-117">-Service</span></span>
<span data-ttu-id="34a31-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="34a31-118">Name of the service</span></span>

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

### <span data-ttu-id="34a31-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="34a31-119">-ServiceResource</span></span>
<span data-ttu-id="34a31-120">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="34a31-120">List of service resources</span></span>

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

### <span data-ttu-id="34a31-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="34a31-121">-Confirm</span></span>
<span data-ttu-id="34a31-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34a31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a31-123">-WhatIf</span></span>
<span data-ttu-id="34a31-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34a31-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34a31-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34a31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a31-126">CommonParameters</span></span>
<span data-ttu-id="34a31-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34a31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a31-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a31-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a31-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34a31-129">INPUTS</span></span>

### <span data-ttu-id="34a31-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34a31-130">None</span></span>

## <span data-ttu-id="34a31-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34a31-131">OUTPUTS</span></span>

### <span data-ttu-id="34a31-132">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="34a31-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34a31-133">NOTES</span></span>

## <span data-ttu-id="34a31-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34a31-134">RELATED LINKS</span></span>

[<span data-ttu-id="34a31-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="34a31-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="34a31-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="34a31-138">Set-Azhizmetiendpointpolicydefinition</span><span class="sxs-lookup"><span data-stu-id="34a31-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
