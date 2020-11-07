---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 455ee170ffba9f601cd8e3034e0c774966f92eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935316"
---
# <span data-ttu-id="4e6b1-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4e6b1-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4e6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b1-103">Bir Azure uygulaması ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="4e6b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e6b1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e6b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6b1-106">Remove-AzApplicationGatewaySslPolicy cmdlet 'i bir Azure uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="4e6b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6b1-108">Örnek 1: uygulama ağ geçidinden SSL ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4e6b1-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="4e6b1-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="4e6b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6b1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e6b1-111">-ApplicationGateway</span></span>
<span data-ttu-id="4e6b1-112">Bu cmdlet 'in SSL ilkesini kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="4e6b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b1-113">-DefaultProfile</span></span>
<span data-ttu-id="4e6b1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e6b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4e6b1-115">-Force</span></span>
<span data-ttu-id="4e6b1-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e6b1-117">-Confirm</span></span>
<span data-ttu-id="4e6b1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6b1-119">-WhatIf</span></span>
<span data-ttu-id="4e6b1-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6b1-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b1-122">CommonParameters</span></span>
<span data-ttu-id="4e6b1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e6b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b1-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6b1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e6b1-125">INPUTS</span></span>

### <span data-ttu-id="4e6b1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4e6b1-126">System.String</span></span>

## <span data-ttu-id="4e6b1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e6b1-127">OUTPUTS</span></span>

### <span data-ttu-id="4e6b1-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e6b1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e6b1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e6b1-129">NOTES</span></span>
<span data-ttu-id="4e6b1-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4e6b1-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4e6b1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e6b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e6b1-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4e6b1-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4e6b1-133">Yeni-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4e6b1-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4e6b1-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4e6b1-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

