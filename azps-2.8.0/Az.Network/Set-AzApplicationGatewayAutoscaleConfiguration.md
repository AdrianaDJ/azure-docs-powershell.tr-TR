---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: ad8795016fc10212a885267d23a61ddc7224c906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932231"
---
# <span data-ttu-id="01823-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="01823-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="01823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01823-102">SYNOPSIS</span></span>
<span data-ttu-id="01823-103">Uygulama ağ geçidinin otomatik ölçeklendirme yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01823-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="01823-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01823-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01823-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01823-105">DESCRIPTION</span></span>
<span data-ttu-id="01823-106">**Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet 'ı, uygulama ağ geçidinin varolan otomatik ölçeklendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="01823-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="01823-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01823-107">EXAMPLES</span></span>

### <span data-ttu-id="01823-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01823-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="01823-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="01823-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="01823-110">İkinci komut, uygulama ağ geçidinden otomatik ölçeklendirme yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01823-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="01823-111">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="01823-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="01823-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01823-112">PARAMETERS</span></span>

### <span data-ttu-id="01823-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01823-113">-ApplicationGateway</span></span>
<span data-ttu-id="01823-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01823-114">The applicationGateway</span></span>

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

### <span data-ttu-id="01823-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01823-115">-DefaultProfile</span></span>
<span data-ttu-id="01823-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01823-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01823-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="01823-117">-MaxCapacity</span></span>
<span data-ttu-id="01823-118">Uygulama ağ geçidi için maksimum kapasite.</span><span class="sxs-lookup"><span data-stu-id="01823-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01823-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="01823-119">-MinCapacity</span></span>
<span data-ttu-id="01823-120">Uygulama ağ geçidi için minimum kapasite.</span><span class="sxs-lookup"><span data-stu-id="01823-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01823-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="01823-121">-Confirm</span></span>
<span data-ttu-id="01823-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01823-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01823-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01823-123">-WhatIf</span></span>
<span data-ttu-id="01823-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01823-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01823-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01823-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01823-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01823-126">CommonParameters</span></span>
<span data-ttu-id="01823-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01823-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01823-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01823-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01823-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01823-129">INPUTS</span></span>

### <span data-ttu-id="01823-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01823-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01823-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01823-131">OUTPUTS</span></span>

### <span data-ttu-id="01823-132">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01823-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01823-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01823-133">NOTES</span></span>

## <span data-ttu-id="01823-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01823-134">RELATED LINKS</span></span>

[<span data-ttu-id="01823-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="01823-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="01823-136">Yeni-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="01823-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="01823-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="01823-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
