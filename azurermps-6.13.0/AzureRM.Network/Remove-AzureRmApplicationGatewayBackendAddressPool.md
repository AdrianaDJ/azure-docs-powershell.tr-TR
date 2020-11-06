---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 996a2c17b6283e967eaca8462f4d703aed60d19c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589458"
---
# <span data-ttu-id="d8148-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d8148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8148-102">SYNOPSIS</span></span>
<span data-ttu-id="d8148-103">Bir arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d8148-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8148-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8148-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8148-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8148-105">DESCRIPTION</span></span>
<span data-ttu-id="d8148-106">**Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidinden arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d8148-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="d8148-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8148-107">EXAMPLES</span></span>

### <span data-ttu-id="d8148-108">Örnek 1: uygulama ağ geçidinden arka uç adres havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="d8148-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="d8148-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d8148-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="d8148-110">İkinci komut BackEndPool02 adındaki arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d8148-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="d8148-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8148-111">PARAMETERS</span></span>

### <span data-ttu-id="d8148-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8148-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8148-113">Bu cmdlet 'in arka uç adres havuzunu kaldıran uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8148-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="d8148-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8148-114">-DefaultProfile</span></span>
<span data-ttu-id="d8148-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8148-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8148-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8148-116">-Name</span></span>
<span data-ttu-id="d8148-117">Bu cmdlet 'in kaldırdığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8148-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8148-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8148-118">-Confirm</span></span>
<span data-ttu-id="d8148-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8148-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8148-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8148-120">-WhatIf</span></span>
<span data-ttu-id="d8148-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8148-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8148-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8148-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8148-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8148-123">CommonParameters</span></span>
<span data-ttu-id="d8148-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8148-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8148-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8148-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8148-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8148-126">INPUTS</span></span>

### <span data-ttu-id="d8148-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8148-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d8148-128">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8148-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d8148-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8148-129">OUTPUTS</span></span>

### <span data-ttu-id="d8148-130">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d8148-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8148-131">NOTES</span></span>

## <span data-ttu-id="d8148-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8148-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8148-133">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-133">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d8148-134">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-134">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d8148-135">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-135">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d8148-136">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d8148-136">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


