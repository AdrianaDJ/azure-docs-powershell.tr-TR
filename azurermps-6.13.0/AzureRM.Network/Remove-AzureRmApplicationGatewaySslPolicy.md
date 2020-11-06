---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3504e4fbdb74fffc41e3f6424540dec71bb209e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589450"
---
# <span data-ttu-id="65194-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="65194-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="65194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65194-102">SYNOPSIS</span></span>
<span data-ttu-id="65194-103">Bir Azure uygulaması ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65194-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65194-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65194-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65194-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65194-105">DESCRIPTION</span></span>
<span data-ttu-id="65194-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet 'i bir Azure uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65194-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="65194-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65194-107">EXAMPLES</span></span>

### <span data-ttu-id="65194-108">Örnek 1: uygulama ağ geçidinden SSL ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="65194-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="65194-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65194-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="65194-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65194-110">PARAMETERS</span></span>

### <span data-ttu-id="65194-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65194-111">-ApplicationGateway</span></span>
<span data-ttu-id="65194-112">Bu cmdlet 'in SSL ilkesini kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65194-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="65194-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65194-113">-DefaultProfile</span></span>
<span data-ttu-id="65194-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65194-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65194-115">-Force</span><span class="sxs-lookup"><span data-stu-id="65194-115">-Force</span></span>
<span data-ttu-id="65194-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="65194-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65194-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="65194-117">-Confirm</span></span>
<span data-ttu-id="65194-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65194-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65194-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65194-119">-WhatIf</span></span>
<span data-ttu-id="65194-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65194-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65194-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65194-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65194-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65194-122">CommonParameters</span></span>
<span data-ttu-id="65194-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65194-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65194-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65194-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65194-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65194-125">INPUTS</span></span>

### <span data-ttu-id="65194-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65194-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="65194-127">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65194-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="65194-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65194-128">OUTPUTS</span></span>

### <span data-ttu-id="65194-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65194-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65194-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65194-130">NOTES</span></span>
<span data-ttu-id="65194-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="65194-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="65194-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65194-132">RELATED LINKS</span></span>

[<span data-ttu-id="65194-133">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="65194-133">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="65194-134">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="65194-134">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="65194-135">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="65194-135">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

