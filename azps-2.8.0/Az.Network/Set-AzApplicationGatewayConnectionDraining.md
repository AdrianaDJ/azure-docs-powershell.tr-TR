---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: d04dc0c3d9d446941870f30578f50d5ecd795009
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917963"
---
# <span data-ttu-id="76ba6-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="76ba6-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="76ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="76ba6-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="76ba6-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76ba6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76ba6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ba6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76ba6-105">DESCRIPTION</span></span>
<span data-ttu-id="76ba6-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="76ba6-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="76ba6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76ba6-107">EXAMPLES</span></span>

### <span data-ttu-id="76ba6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76ba6-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="76ba6-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="76ba6-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="76ba6-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="76ba6-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="76ba6-111">Son komut $Settings depolanan arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını, false değerine ve DrainTimeoutInSec 'e 3600 'e ayarlayarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="76ba6-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="76ba6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76ba6-112">PARAMETERS</span></span>

### <span data-ttu-id="76ba6-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76ba6-113">-BackendHttpSettings</span></span>
<span data-ttu-id="76ba6-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="76ba6-114">The backend http settings</span></span>

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

### <span data-ttu-id="76ba6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ba6-115">-DefaultProfile</span></span>
<span data-ttu-id="76ba6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76ba6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ba6-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="76ba6-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="76ba6-118">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="76ba6-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="76ba6-119">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="76ba6-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ba6-120">Özellikli</span><span class="sxs-lookup"><span data-stu-id="76ba6-120">-Enabled</span></span>
<span data-ttu-id="76ba6-121">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="76ba6-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ba6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ba6-122">CommonParameters</span></span>
<span data-ttu-id="76ba6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76ba6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ba6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ba6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ba6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76ba6-125">INPUTS</span></span>

### <span data-ttu-id="76ba6-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76ba6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76ba6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76ba6-127">OUTPUTS</span></span>

### <span data-ttu-id="76ba6-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76ba6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="76ba6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76ba6-129">NOTES</span></span>

## <span data-ttu-id="76ba6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76ba6-130">RELATED LINKS</span></span>

[<span data-ttu-id="76ba6-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76ba6-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="76ba6-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="76ba6-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="76ba6-133">Get-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="76ba6-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76ba6-134">Yeni-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="76ba6-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="76ba6-135">Remove-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="76ba6-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

