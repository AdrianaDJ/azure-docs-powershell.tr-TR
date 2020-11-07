---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 9b03a33ebea52e57950e46c894e95ffefe520b4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918199"
---
# <span data-ttu-id="a049d-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a049d-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="a049d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a049d-102">SYNOPSIS</span></span>
<span data-ttu-id="a049d-103">Hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a049d-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="a049d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a049d-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a049d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a049d-105">DESCRIPTION</span></span>
<span data-ttu-id="a049d-106">**Yeni-Azhizmetiendpointpolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a049d-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="a049d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a049d-107">EXAMPLES</span></span>

### <span data-ttu-id="a049d-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="a049d-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="a049d-109">Bu komut, Policy1 adında, nesne $serviceEndpointDefinition tanımlanan tanımlara sahip bir hizmet bitiş noktası ilkesi oluşturur ve $serviceEndpointPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a049d-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="a049d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a049d-110">PARAMETERS</span></span>

### <span data-ttu-id="a049d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a049d-111">-DefaultProfile</span></span>
<span data-ttu-id="a049d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a049d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a049d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a049d-113">-Force</span></span>
<span data-ttu-id="a049d-114">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="a049d-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a049d-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="a049d-115">-Location</span></span>
<span data-ttu-id="a049d-116">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="a049d-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a049d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a049d-117">-Name</span></span>
<span data-ttu-id="a049d-118">Alt ağın adı</span><span class="sxs-lookup"><span data-stu-id="a049d-118">The name of the subnet</span></span>

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

### <span data-ttu-id="a049d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a049d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a049d-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a049d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a049d-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a049d-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="a049d-122">Hizmet uç noktası tanımlarının listesi</span><span class="sxs-lookup"><span data-stu-id="a049d-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a049d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a049d-123">-Confirm</span></span>
<span data-ttu-id="a049d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a049d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a049d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a049d-125">-WhatIf</span></span>
<span data-ttu-id="a049d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a049d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a049d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a049d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a049d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a049d-128">CommonParameters</span></span>
<span data-ttu-id="a049d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a049d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a049d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a049d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a049d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a049d-131">INPUTS</span></span>

### <span data-ttu-id="a049d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a049d-132">System.String</span></span>

## <span data-ttu-id="a049d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a049d-133">OUTPUTS</span></span>

### <span data-ttu-id="a049d-134">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a049d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a049d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a049d-135">NOTES</span></span>

## <span data-ttu-id="a049d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a049d-136">RELATED LINKS</span></span>

[<span data-ttu-id="a049d-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a049d-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a049d-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a049d-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a049d-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a049d-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)