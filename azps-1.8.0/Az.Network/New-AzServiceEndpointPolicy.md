---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760277"
---
# <span data-ttu-id="8d8d1-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8d8d1-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="8d8d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8d1-103">Hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="8d8d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d8d1-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d8d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d8d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8d1-106">**Yeni-Azhizmetiendpointpolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="8d8d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d8d1-107">EXAMPLES</span></span>

### <span data-ttu-id="8d8d1-108">Örnek 1: hizmet bitiş noktası ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="8d8d1-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="8d8d1-109">Bu komut, Policy1 adında, nesne $serviceEndpointDefinition tanımlanan tanımlara sahip bir hizmet bitiş noktası ilkesi oluşturur ve $serviceEndpointPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="8d8d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d8d1-110">PARAMETERS</span></span>

### <span data-ttu-id="8d8d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8d1-111">-DefaultProfile</span></span>
<span data-ttu-id="8d8d1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d8d1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8d8d1-113">-Force</span></span>
<span data-ttu-id="8d8d1-114">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="8d8d1-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8d8d1-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="8d8d1-115">-Location</span></span>
<span data-ttu-id="8d8d1-116">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-116">location.</span></span>

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

### <span data-ttu-id="8d8d1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d8d1-117">-Name</span></span>
<span data-ttu-id="8d8d1-118">Alt ağın adı</span><span class="sxs-lookup"><span data-stu-id="8d8d1-118">The name of the subnet</span></span>

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

### <span data-ttu-id="8d8d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d8d1-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-120">The resource group name.</span></span>

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

### <span data-ttu-id="8d8d1-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d8d1-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="8d8d1-122">Hizmet uç noktası tanımlarının listesi</span><span class="sxs-lookup"><span data-stu-id="8d8d1-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="8d8d1-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8d8d1-123">-Confirm</span></span>
<span data-ttu-id="8d8d1-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d8d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d8d1-125">-WhatIf</span></span>
<span data-ttu-id="8d8d1-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d8d1-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d8d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8d1-128">CommonParameters</span></span>
<span data-ttu-id="8d8d1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d8d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8d1-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d8d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8d1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d8d1-131">INPUTS</span></span>

### <span data-ttu-id="8d8d1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8d1-132">System.String</span></span>

## <span data-ttu-id="8d8d1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d8d1-133">OUTPUTS</span></span>

### <span data-ttu-id="8d8d1-134">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8d8d1-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8d8d1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d8d1-135">NOTES</span></span>

## <span data-ttu-id="8d8d1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d8d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d8d1-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8d8d1-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8d8d1-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8d8d1-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8d8d1-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8d8d1-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
