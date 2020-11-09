---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323221"
---
# <span data-ttu-id="edfdd-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfdd-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="edfdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="edfdd-103">Hizmet uç noktası İlkesi tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="edfdd-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="edfdd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edfdd-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfdd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edfdd-105">DESCRIPTION</span></span>
<span data-ttu-id="edfdd-106">**Set-Azhizmetiendpointpolicydefinition** cmdlet 'i bir hizmet uç noktası ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="edfdd-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="edfdd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edfdd-107">EXAMPLES</span></span>

### <span data-ttu-id="edfdd-108">Örnek 1: hizmet uç noktası ilkesinde hizmet uç noktası İlkesi tanımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="edfdd-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="edfdd-109">Bu komut, nesne $ServiceEndpointPolicy tarafından tanımlanan hizmet uç noktası ilkesinde Policydef1 adlı bir hizmet uç noktası İlkesi tanımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="edfdd-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="edfdd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edfdd-110">PARAMETERS</span></span>

### <span data-ttu-id="edfdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfdd-111">-DefaultProfile</span></span>
<span data-ttu-id="edfdd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edfdd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edfdd-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="edfdd-113">-Description</span></span>
<span data-ttu-id="edfdd-114">Tanımın açıklaması</span><span class="sxs-lookup"><span data-stu-id="edfdd-114">The description of the definition</span></span>

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

### <span data-ttu-id="edfdd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="edfdd-115">-Name</span></span>
<span data-ttu-id="edfdd-116">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="edfdd-116">The name of the rule</span></span>

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

### <span data-ttu-id="edfdd-117">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="edfdd-117">-Service</span></span>
<span data-ttu-id="edfdd-118">Hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="edfdd-118">Name of the service</span></span>

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

### <span data-ttu-id="edfdd-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="edfdd-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="edfdd-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="edfdd-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="edfdd-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="edfdd-121">-ServiceResource</span></span>
<span data-ttu-id="edfdd-122">Hizmet kaynakları listesi</span><span class="sxs-lookup"><span data-stu-id="edfdd-122">List of service resources</span></span>

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

### <span data-ttu-id="edfdd-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="edfdd-123">-Confirm</span></span>
<span data-ttu-id="edfdd-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edfdd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfdd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfdd-125">-WhatIf</span></span>
<span data-ttu-id="edfdd-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edfdd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edfdd-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edfdd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfdd-128">CommonParameters</span></span>
<span data-ttu-id="edfdd-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edfdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfdd-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfdd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfdd-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edfdd-131">INPUTS</span></span>

### <span data-ttu-id="edfdd-132">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="edfdd-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="edfdd-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edfdd-133">OUTPUTS</span></span>

### <span data-ttu-id="edfdd-134">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="edfdd-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="edfdd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edfdd-135">NOTES</span></span>

## <span data-ttu-id="edfdd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edfdd-136">RELATED LINKS</span></span>

[<span data-ttu-id="edfdd-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfdd-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="edfdd-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfdd-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="edfdd-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfdd-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="edfdd-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="edfdd-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
