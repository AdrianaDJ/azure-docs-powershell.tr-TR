---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278353"
---
# <span data-ttu-id="52d21-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52d21-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="52d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d21-102">SYNOPSIS</span></span>
<span data-ttu-id="52d21-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="52d21-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="52d21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d21-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d21-105">DESCRIPTION</span></span>
<span data-ttu-id="52d21-106">**Get-Azapplicationgatewayconnectionboşaltma** cmdlet 'i, arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="52d21-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="52d21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d21-107">EXAMPLES</span></span>

### <span data-ttu-id="52d21-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52d21-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="52d21-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="52d21-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="52d21-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="52d21-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="52d21-111">Son komut arka uç HTTP ayarları $Settings bağlantı boşaltma yapılandırmasını alır ve $ConnectionDraining değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="52d21-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="52d21-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d21-112">PARAMETERS</span></span>

### <span data-ttu-id="52d21-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52d21-113">-BackendHttpSettings</span></span>
<span data-ttu-id="52d21-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="52d21-114">The backend http settings</span></span>

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

### <span data-ttu-id="52d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d21-115">-DefaultProfile</span></span>
<span data-ttu-id="52d21-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52d21-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d21-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d21-117">CommonParameters</span></span>
<span data-ttu-id="52d21-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d21-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d21-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="52d21-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d21-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d21-120">INPUTS</span></span>

### <span data-ttu-id="52d21-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52d21-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="52d21-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d21-122">OUTPUTS</span></span>

### <span data-ttu-id="52d21-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="52d21-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="52d21-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d21-124">NOTES</span></span>

## <span data-ttu-id="52d21-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d21-125">RELATED LINKS</span></span>

[<span data-ttu-id="52d21-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52d21-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="52d21-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="52d21-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="52d21-128">Yeni-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="52d21-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="52d21-129">Remove-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="52d21-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="52d21-130">Set-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="52d21-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
