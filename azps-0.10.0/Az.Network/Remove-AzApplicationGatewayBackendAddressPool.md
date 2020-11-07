---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a9346f3ff990007ed1033032d111e5851a2ac534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935337"
---
# <span data-ttu-id="b962f-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b962f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b962f-102">SYNOPSIS</span></span>
<span data-ttu-id="b962f-103">Bir arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b962f-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="b962f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b962f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b962f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b962f-105">DESCRIPTION</span></span>
<span data-ttu-id="b962f-106">**Remove-AzApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidinden arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b962f-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="b962f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b962f-107">EXAMPLES</span></span>

### <span data-ttu-id="b962f-108">Örnek 1: uygulama ağ geçidinden arka uç adres havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="b962f-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="b962f-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b962f-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="b962f-110">İkinci komut BackEndPool02 adındaki arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b962f-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="b962f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b962f-111">PARAMETERS</span></span>

### <span data-ttu-id="b962f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b962f-112">-ApplicationGateway</span></span>
<span data-ttu-id="b962f-113">Bu cmdlet 'in arka uç adres havuzunu kaldıran uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b962f-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="b962f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b962f-114">-DefaultProfile</span></span>
<span data-ttu-id="b962f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b962f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b962f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b962f-116">-Name</span></span>
<span data-ttu-id="b962f-117">Bu cmdlet 'in kaldırdığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b962f-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b962f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b962f-118">-Confirm</span></span>
<span data-ttu-id="b962f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b962f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b962f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b962f-120">-WhatIf</span></span>
<span data-ttu-id="b962f-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b962f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b962f-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b962f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b962f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b962f-123">CommonParameters</span></span>
<span data-ttu-id="b962f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b962f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b962f-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b962f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b962f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b962f-126">INPUTS</span></span>

### <span data-ttu-id="b962f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b962f-127">System.String</span></span>

## <span data-ttu-id="b962f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b962f-128">OUTPUTS</span></span>

### <span data-ttu-id="b962f-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b962f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b962f-130">NOTES</span></span>

## <span data-ttu-id="b962f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b962f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b962f-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b962f-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b962f-134">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b962f-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b962f-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


