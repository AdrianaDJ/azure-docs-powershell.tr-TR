---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097537"
---
# <span data-ttu-id="47e8d-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47e8d-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="47e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="47e8d-103">Otomatik ölçeklendirme yapılandırmasını uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47e8d-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="47e8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47e8d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e8d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47e8d-105">DESCRIPTION</span></span>
<span data-ttu-id="47e8d-106">**Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet 'i var olan uygulama ağ geçidinden otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47e8d-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="47e8d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47e8d-107">EXAMPLES</span></span>

### <span data-ttu-id="47e8d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47e8d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="47e8d-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="47e8d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="47e8d-110">İkinci komut, uygulama ağ geçidinden otomatik ölçeklendirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47e8d-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="47e8d-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="47e8d-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="47e8d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47e8d-112">PARAMETERS</span></span>

### <span data-ttu-id="47e8d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e8d-113">-ApplicationGateway</span></span>
<span data-ttu-id="47e8d-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e8d-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e8d-115">-DefaultProfile</span></span>
<span data-ttu-id="47e8d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47e8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e8d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="47e8d-117">-Force</span></span>
<span data-ttu-id="47e8d-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="47e8d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47e8d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="47e8d-119">-Confirm</span></span>
<span data-ttu-id="47e8d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47e8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e8d-121">-WhatIf</span></span>
<span data-ttu-id="47e8d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47e8d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e8d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47e8d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e8d-124">CommonParameters</span></span>
<span data-ttu-id="47e8d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47e8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e8d-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e8d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e8d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47e8d-127">INPUTS</span></span>

### <span data-ttu-id="47e8d-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e8d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47e8d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47e8d-129">OUTPUTS</span></span>

### <span data-ttu-id="47e8d-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e8d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47e8d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47e8d-131">NOTES</span></span>

## <span data-ttu-id="47e8d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47e8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="47e8d-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47e8d-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="47e8d-134">Yeni-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47e8d-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="47e8d-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47e8d-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
