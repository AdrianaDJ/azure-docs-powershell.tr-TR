---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 383ad627ff7a633d508daccde70e3de395e4ad57
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939094"
---
# <span data-ttu-id="85b8a-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="85b8a-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="85b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="85b8a-103">Bir Azure uygulaması ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85b8a-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85b8a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85b8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="85b8a-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet 'i bir Azure uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85b8a-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="85b8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="85b8a-108">Örnek 1: uygulama ağ geçidinden SSL ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="85b8a-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="85b8a-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="85b8a-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="85b8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="85b8a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85b8a-111">-ApplicationGateway</span></span>
<span data-ttu-id="85b8a-112">Bu cmdlet 'in SSL ilkesini kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85b8a-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="85b8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b8a-113">-DefaultProfile</span></span>
<span data-ttu-id="85b8a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85b8a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b8a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="85b8a-115">-Force</span></span>
<span data-ttu-id="85b8a-116">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="85b8a-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="85b8a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="85b8a-117">-Confirm</span></span>
<span data-ttu-id="85b8a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85b8a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85b8a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b8a-119">-WhatIf</span></span>
<span data-ttu-id="85b8a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85b8a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85b8a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85b8a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85b8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b8a-122">CommonParameters</span></span>
<span data-ttu-id="85b8a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85b8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b8a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b8a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85b8a-125">INPUTS</span></span>

### <span data-ttu-id="85b8a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="85b8a-126">System.String</span></span>

## <span data-ttu-id="85b8a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85b8a-127">OUTPUTS</span></span>

### <span data-ttu-id="85b8a-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85b8a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85b8a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85b8a-129">NOTES</span></span>
<span data-ttu-id="85b8a-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="85b8a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="85b8a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85b8a-131">RELATED LINKS</span></span>

[<span data-ttu-id="85b8a-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="85b8a-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="85b8a-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="85b8a-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="85b8a-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="85b8a-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

