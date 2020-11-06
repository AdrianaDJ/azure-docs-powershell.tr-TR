---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 81928913565c6e95f3768ccd5c05e8baa2c14b74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595003"
---
# <span data-ttu-id="4a02d-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a02d-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="4a02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a02d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a02d-103">Bir Azure uygulaması ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a02d-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a02d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a02d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a02d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a02d-105">DESCRIPTION</span></span>
<span data-ttu-id="4a02d-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet 'i bir Azure uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a02d-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="4a02d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a02d-107">EXAMPLES</span></span>

### <span data-ttu-id="4a02d-108">Örnek 1: uygulama ağ geçidinden SSL ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4a02d-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="4a02d-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a02d-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="4a02d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a02d-110">PARAMETERS</span></span>

### <span data-ttu-id="4a02d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a02d-111">-ApplicationGateway</span></span>
<span data-ttu-id="4a02d-112">Bu cmdlet 'in SSL ilkesini kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a02d-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="4a02d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4a02d-113">-Force</span></span>
<span data-ttu-id="4a02d-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4a02d-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a02d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a02d-115">-Confirm</span></span>
<span data-ttu-id="4a02d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a02d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a02d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a02d-117">-WhatIf</span></span>
<span data-ttu-id="4a02d-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a02d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a02d-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a02d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a02d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a02d-120">-DefaultProfile</span></span>
<span data-ttu-id="4a02d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a02d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a02d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a02d-122">CommonParameters</span></span>
<span data-ttu-id="4a02d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a02d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a02d-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a02d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a02d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a02d-125">INPUTS</span></span>

### <span data-ttu-id="4a02d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4a02d-126">System.String</span></span>

## <span data-ttu-id="4a02d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a02d-127">OUTPUTS</span></span>

### <span data-ttu-id="4a02d-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a02d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a02d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a02d-129">NOTES</span></span>
<span data-ttu-id="4a02d-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4a02d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4a02d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a02d-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a02d-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a02d-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4a02d-133">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a02d-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="4a02d-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="4a02d-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

