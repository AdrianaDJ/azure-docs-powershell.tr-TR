---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: aedcfa4134212ef1583a91a8b902ca8395dbbfe5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760035"
---
# <span data-ttu-id="a840b-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a840b-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="a840b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a840b-102">SYNOPSIS</span></span>
<span data-ttu-id="a840b-103">Uygulama ağ geçidinin SSL ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a840b-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="a840b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a840b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a840b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a840b-105">DESCRIPTION</span></span>
<span data-ttu-id="a840b-106">**Set-AzApplicationGatewaySslPolicy** cmdlet 'i, bir uygulama ağ geçidinin SSL ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a840b-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="a840b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a840b-107">EXAMPLES</span></span>

### <span data-ttu-id="a840b-108">2</span><span class="sxs-lookup"><span data-stu-id="a840b-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="a840b-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a840b-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a840b-110">Bu ikinci komut SSL ilkesini önceden tanımlanmış bir ilke türüne ve ilke adı AppGwSslPolicy20170401 değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a840b-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="a840b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a840b-111">PARAMETERS</span></span>

### <span data-ttu-id="a840b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a840b-112">-ApplicationGateway</span></span>
<span data-ttu-id="a840b-113">Bu cmdlet 'in değiştirdiği SSL ilkesinin uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a840b-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a840b-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="a840b-114">-CipherSuite</span></span>
<span data-ttu-id="a840b-115">Uygulama ağ geçidine belirtilen sırada etkinleştirilecek SSL şifre paketleri</span><span class="sxs-lookup"><span data-stu-id="a840b-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="a840b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a840b-116">-DefaultProfile</span></span>
<span data-ttu-id="a840b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a840b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a840b-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="a840b-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="a840b-119">Hangi protokollerin devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a840b-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="a840b-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a840b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a840b-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="a840b-121">TLSv1_0</span></span> 
- <span data-ttu-id="a840b-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="a840b-122">TLSv1_1</span></span> 
- <span data-ttu-id="a840b-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="a840b-123">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840b-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="a840b-124">-MinProtocolVersion</span></span>
<span data-ttu-id="a840b-125">Uygulama ağ geçidinde desteklenecek SSL protokolünün en az sürümü</span><span class="sxs-lookup"><span data-stu-id="a840b-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840b-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="a840b-126">-PolicyName</span></span>
<span data-ttu-id="a840b-127">Önceden tanımlanmış SSL ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="a840b-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="a840b-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="a840b-128">-PolicyType</span></span>
<span data-ttu-id="a840b-129">SSL Ilkesinin türü</span><span class="sxs-lookup"><span data-stu-id="a840b-129">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="a840b-130">-Confirm</span></span>
<span data-ttu-id="a840b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a840b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a840b-132">-WhatIf</span></span>
<span data-ttu-id="a840b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a840b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a840b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a840b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a840b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a840b-135">CommonParameters</span></span>
<span data-ttu-id="a840b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a840b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a840b-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a840b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a840b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a840b-138">INPUTS</span></span>

### <span data-ttu-id="a840b-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a840b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a840b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a840b-140">OUTPUTS</span></span>

### <span data-ttu-id="a840b-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a840b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a840b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a840b-142">NOTES</span></span>
* <span data-ttu-id="a840b-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="a840b-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a840b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a840b-144">RELATED LINKS</span></span>

[<span data-ttu-id="a840b-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a840b-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="a840b-146">Yeni-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a840b-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

