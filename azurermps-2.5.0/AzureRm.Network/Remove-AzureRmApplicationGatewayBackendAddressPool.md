---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939506"
---
# <span data-ttu-id="0f7b5-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0f7b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7b5-103">Bir arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f7b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f7b5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f7b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="0f7b5-106">**Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidinden arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="0f7b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f7b5-107">EXAMPLES</span></span>

### <span data-ttu-id="0f7b5-108">Örnek 1: uygulama ağ geçidinden arka uç adres havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="0f7b5-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="0f7b5-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="0f7b5-110">İkinci komut BackEndPool02 adındaki arka uç adres havuzunu uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="0f7b5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f7b5-111">PARAMETERS</span></span>

### <span data-ttu-id="0f7b5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f7b5-112">-ApplicationGateway</span></span>
<span data-ttu-id="0f7b5-113">Bu cmdlet 'in arka uç adres havuzunu kaldıran uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="0f7b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7b5-114">-DefaultProfile</span></span>
<span data-ttu-id="0f7b5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f7b5-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f7b5-116">-Name</span></span>
<span data-ttu-id="0f7b5-117">Bu cmdlet 'in kaldırdığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f7b5-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f7b5-118">-Confirm</span></span>
<span data-ttu-id="0f7b5-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f7b5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7b5-120">-WhatIf</span></span>
<span data-ttu-id="0f7b5-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f7b5-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f7b5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7b5-123">CommonParameters</span></span>
<span data-ttu-id="0f7b5-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f7b5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7b5-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f7b5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7b5-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f7b5-126">INPUTS</span></span>

### <span data-ttu-id="0f7b5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0f7b5-127">System.String</span></span>

## <span data-ttu-id="0f7b5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f7b5-128">OUTPUTS</span></span>

### <span data-ttu-id="0f7b5-129">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="0f7b5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f7b5-130">NOTES</span></span>

## <span data-ttu-id="0f7b5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f7b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="0f7b5-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0f7b5-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0f7b5-134">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0f7b5-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f7b5-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


