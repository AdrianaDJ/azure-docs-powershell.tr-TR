---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 5357b8a0a59fade3e9ff7439da9ac1eeb63f6035
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932314"
---
# <span data-ttu-id="d0cfc-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d0cfc-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d0cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cfc-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d0cfc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0cfc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0cfc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="d0cfc-106">**Remove-Azapplicationgatewayconnectionboşaltma** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d0cfc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0cfc-107">EXAMPLES</span></span>

### <span data-ttu-id="d0cfc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d0cfc-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="d0cfc-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0cfc-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="d0cfc-111">Son komut $Settings depolanan arka uç HTTP ayarlarının bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="d0cfc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0cfc-112">PARAMETERS</span></span>

### <span data-ttu-id="d0cfc-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0cfc-113">-BackendHttpSettings</span></span>
<span data-ttu-id="d0cfc-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="d0cfc-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0cfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cfc-115">-DefaultProfile</span></span>
<span data-ttu-id="d0cfc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0cfc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cfc-117">CommonParameters</span></span>
<span data-ttu-id="d0cfc-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0cfc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cfc-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0cfc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cfc-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0cfc-120">INPUTS</span></span>

### <span data-ttu-id="d0cfc-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0cfc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d0cfc-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0cfc-122">OUTPUTS</span></span>

### <span data-ttu-id="d0cfc-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0cfc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d0cfc-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0cfc-124">NOTES</span></span>

## <span data-ttu-id="d0cfc-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0cfc-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0cfc-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0cfc-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d0cfc-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0cfc-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="d0cfc-128">Get-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="d0cfc-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d0cfc-129">Yeni-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="d0cfc-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d0cfc-130">Set-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="d0cfc-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

