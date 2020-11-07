---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 517327ab3af1665d70f3d2f8eff4594d708a2f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918107"
---
# <span data-ttu-id="158f7-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="158f7-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="158f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158f7-102">SYNOPSIS</span></span>
<span data-ttu-id="158f7-103">Bir Azure uygulaması ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="158f7-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="158f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="158f7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="158f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="158f7-105">DESCRIPTION</span></span>
<span data-ttu-id="158f7-106">Remove-AzApplicationGatewaySslPolicy cmdlet 'i bir Azure uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="158f7-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="158f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="158f7-107">EXAMPLES</span></span>

### <span data-ttu-id="158f7-108">Örnek 1: uygulama ağ geçidinden SSL ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="158f7-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="158f7-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="158f7-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="158f7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="158f7-110">PARAMETERS</span></span>

### <span data-ttu-id="158f7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158f7-111">-ApplicationGateway</span></span>
<span data-ttu-id="158f7-112">Bu cmdlet 'in SSL ilkesini kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="158f7-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="158f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158f7-113">-DefaultProfile</span></span>
<span data-ttu-id="158f7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="158f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158f7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="158f7-115">-Force</span></span>
<span data-ttu-id="158f7-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="158f7-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="158f7-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="158f7-117">-Confirm</span></span>
<span data-ttu-id="158f7-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="158f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158f7-119">-WhatIf</span></span>
<span data-ttu-id="158f7-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="158f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="158f7-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="158f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158f7-122">CommonParameters</span></span>
<span data-ttu-id="158f7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="158f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158f7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158f7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="158f7-125">INPUTS</span></span>

### <span data-ttu-id="158f7-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158f7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="158f7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="158f7-127">OUTPUTS</span></span>

### <span data-ttu-id="158f7-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="158f7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="158f7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="158f7-129">NOTES</span></span>
<span data-ttu-id="158f7-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="158f7-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="158f7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="158f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="158f7-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="158f7-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="158f7-133">Yeni-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="158f7-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="158f7-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="158f7-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

