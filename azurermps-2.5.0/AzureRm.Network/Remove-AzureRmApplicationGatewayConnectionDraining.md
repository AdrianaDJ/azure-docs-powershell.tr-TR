---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 751e27600d81a24005ea0a9200d3efa1d1647597
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940048"
---
# <span data-ttu-id="ae538-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ae538-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ae538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae538-102">SYNOPSIS</span></span>
<span data-ttu-id="ae538-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae538-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae538-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae538-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae538-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae538-105">DESCRIPTION</span></span>
<span data-ttu-id="ae538-106">**Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae538-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ae538-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae538-107">EXAMPLES</span></span>

### <span data-ttu-id="ae538-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae538-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ae538-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ae538-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ae538-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="ae538-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ae538-111">Son komut $Settings depolanan arka uç HTTP ayarlarının bağlantı boşaltma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae538-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="ae538-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae538-112">PARAMETERS</span></span>

### <span data-ttu-id="ae538-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ae538-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ae538-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="ae538-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae538-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae538-115">-DefaultProfile</span></span>
<span data-ttu-id="ae538-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae538-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae538-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae538-117">CommonParameters</span></span>
<span data-ttu-id="ae538-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae538-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae538-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae538-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae538-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae538-120">INPUTS</span></span>

### <span data-ttu-id="ae538-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ae538-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ae538-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae538-122">OUTPUTS</span></span>

### <span data-ttu-id="ae538-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ae538-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ae538-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae538-124">NOTES</span></span>

## <span data-ttu-id="ae538-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae538-125">RELATED LINKS</span></span>

[<span data-ttu-id="ae538-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae538-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="ae538-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ae538-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="ae538-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ae538-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ae538-129">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ae538-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ae538-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ae538-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

