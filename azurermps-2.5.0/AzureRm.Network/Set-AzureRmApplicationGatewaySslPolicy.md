---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 1e0d5de8013bbb6fd5104c3af5bdb555b0317e75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938773"
---
# <span data-ttu-id="070f4-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="070f4-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="070f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="070f4-102">SYNOPSIS</span></span>
<span data-ttu-id="070f4-103">Uygulama ağ geçidinin SSL ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="070f4-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="070f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="070f4-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="070f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="070f4-105">DESCRIPTION</span></span>
<span data-ttu-id="070f4-106">**Set-AzureRmApplicationGatewaySslPolicy** cmdlet 'i, bir uygulama ağ geçidinin SSL ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="070f4-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="070f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="070f4-107">EXAMPLES</span></span>

### <span data-ttu-id="070f4-108">2</span><span class="sxs-lookup"><span data-stu-id="070f4-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="070f4-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="070f4-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="070f4-110">Bu ikinci komut SSL ilkesini önceden tanımlanmış bir ilke türüne ve ilke adı AppGwSslPolicy20170401 değiştirir.</span><span class="sxs-lookup"><span data-stu-id="070f4-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="070f4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="070f4-111">PARAMETERS</span></span>

### <span data-ttu-id="070f4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="070f4-112">-ApplicationGateway</span></span>
<span data-ttu-id="070f4-113">Bu cmdlet 'in değiştirdiği SSL ilkesinin uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="070f4-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="070f4-114">-CipherSuite</span></span>
<span data-ttu-id="070f4-115">Uygulama ağ geçidine belirtilen sırada etkinleştirilecek SSL şifre paketleri</span><span class="sxs-lookup"><span data-stu-id="070f4-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070f4-116">-DefaultProfile</span></span>
<span data-ttu-id="070f4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="070f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="070f4-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="070f4-119">Hangi protokollerin devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="070f4-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="070f4-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="070f4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="070f4-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="070f4-121">TLSv1_0</span></span> 
- <span data-ttu-id="070f4-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="070f4-122">TLSv1_1</span></span> 
- <span data-ttu-id="070f4-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="070f4-123">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="070f4-124">-MinProtocolVersion</span></span>
<span data-ttu-id="070f4-125">Uygulama ağ geçidinde desteklenecek SSL protokolünün en az sürümü</span><span class="sxs-lookup"><span data-stu-id="070f4-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="070f4-126">-PolicyName</span></span>
<span data-ttu-id="070f4-127">Önceden tanımlanmış SSL ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="070f4-127">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="070f4-128">-PolicyType</span></span>
<span data-ttu-id="070f4-129">SSL Ilkesinin türü</span><span class="sxs-lookup"><span data-stu-id="070f4-129">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="070f4-130">-Confirm</span></span>
<span data-ttu-id="070f4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="070f4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="070f4-132">-WhatIf</span></span>
<span data-ttu-id="070f4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="070f4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="070f4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="070f4-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070f4-135">CommonParameters</span></span>
<span data-ttu-id="070f4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="070f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070f4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="070f4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070f4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="070f4-138">INPUTS</span></span>

### <span data-ttu-id="070f4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="070f4-139">System.String</span></span>

## <span data-ttu-id="070f4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="070f4-140">OUTPUTS</span></span>

### <span data-ttu-id="070f4-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="070f4-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="070f4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="070f4-142">NOTES</span></span>
* <span data-ttu-id="070f4-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="070f4-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="070f4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="070f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="070f4-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="070f4-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="070f4-146">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="070f4-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


