---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931974"
---
# <span data-ttu-id="3692a-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3692a-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="3692a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3692a-102">SYNOPSIS</span></span>
<span data-ttu-id="3692a-103">Hizmet uç noktası ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3692a-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="3692a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3692a-104">SYNTAX</span></span>

### <span data-ttu-id="3692a-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3692a-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3692a-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3692a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3692a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3692a-107">DESCRIPTION</span></span>
<span data-ttu-id="3692a-108">**Get-AzServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3692a-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="3692a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3692a-109">EXAMPLES</span></span>

### <span data-ttu-id="3692a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3692a-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3692a-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait olan ServiceEndpointPolicy1 adlı hizmet uç noktası ilkesini alır ve $policy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3692a-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="3692a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3692a-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3692a-113">Bu komut, ResourceGroup01 adındaki kaynak grubundaki tüm hizmet uç noktası ilkelerinin listesini alır ve $policyList değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3692a-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="3692a-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3692a-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="3692a-115">Bu komut, "ServiceEndpointPolicy" ile başlayan tüm hizmet uç noktası ilkelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3692a-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="3692a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3692a-116">PARAMETERS</span></span>

### <span data-ttu-id="3692a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3692a-117">-DefaultProfile</span></span>
<span data-ttu-id="3692a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3692a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3692a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3692a-119">-Name</span></span>
<span data-ttu-id="3692a-120">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="3692a-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3692a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3692a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3692a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3692a-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3692a-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3692a-123">-ResourceId</span></span>
<span data-ttu-id="3692a-124">Hizmet uç noktası ilkesinin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3692a-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3692a-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="3692a-125">-Confirm</span></span>
<span data-ttu-id="3692a-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3692a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3692a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3692a-127">-WhatIf</span></span>
<span data-ttu-id="3692a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3692a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3692a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3692a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3692a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3692a-130">CommonParameters</span></span>
<span data-ttu-id="3692a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3692a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3692a-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3692a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3692a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3692a-133">INPUTS</span></span>

### <span data-ttu-id="3692a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3692a-134">System.String</span></span>

## <span data-ttu-id="3692a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3692a-135">OUTPUTS</span></span>

### <span data-ttu-id="3692a-136">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3692a-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3692a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3692a-137">NOTES</span></span>

## <span data-ttu-id="3692a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3692a-138">RELATED LINKS</span></span>

[<span data-ttu-id="3692a-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3692a-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3692a-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3692a-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3692a-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3692a-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)