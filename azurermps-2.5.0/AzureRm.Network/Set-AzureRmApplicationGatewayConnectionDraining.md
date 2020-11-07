---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: ab876b5bc0ea63a2299ec17168b56125c9dbcdba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939270"
---
# <span data-ttu-id="13c59-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="13c59-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="13c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13c59-102">SYNOPSIS</span></span>
<span data-ttu-id="13c59-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="13c59-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13c59-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13c59-105">DESCRIPTION</span></span>
<span data-ttu-id="13c59-106">**Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="13c59-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="13c59-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13c59-107">EXAMPLES</span></span>

### <span data-ttu-id="13c59-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13c59-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="13c59-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="13c59-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="13c59-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="13c59-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="13c59-111">Son komut $Settings depolanan arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını, false değerine ve DrainTimeoutInSec 'e 3600 'e ayarlayarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="13c59-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="13c59-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13c59-112">PARAMETERS</span></span>

### <span data-ttu-id="13c59-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13c59-113">-BackendHttpSettings</span></span>
<span data-ttu-id="13c59-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="13c59-114">The backend http settings</span></span>

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

### <span data-ttu-id="13c59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c59-115">-DefaultProfile</span></span>
<span data-ttu-id="13c59-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13c59-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13c59-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="13c59-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="13c59-118">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="13c59-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="13c59-119">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="13c59-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c59-120">Özellikli</span><span class="sxs-lookup"><span data-stu-id="13c59-120">-Enabled</span></span>
<span data-ttu-id="13c59-121">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="13c59-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c59-122">CommonParameters</span></span>
<span data-ttu-id="13c59-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13c59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c59-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c59-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c59-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13c59-125">INPUTS</span></span>

### <span data-ttu-id="13c59-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13c59-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="13c59-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13c59-127">OUTPUTS</span></span>

### <span data-ttu-id="13c59-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13c59-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="13c59-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13c59-129">NOTES</span></span>

## <span data-ttu-id="13c59-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13c59-130">RELATED LINKS</span></span>

[<span data-ttu-id="13c59-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13c59-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="13c59-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13c59-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="13c59-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="13c59-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="13c59-134">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="13c59-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="13c59-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="13c59-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

