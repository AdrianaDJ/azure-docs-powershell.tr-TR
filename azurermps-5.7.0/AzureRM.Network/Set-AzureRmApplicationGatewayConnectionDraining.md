---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3fe3d07a40f81c22fba39aee0db2eb0a2da6e788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594055"
---
# <span data-ttu-id="67796-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="67796-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="67796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67796-102">SYNOPSIS</span></span>
<span data-ttu-id="67796-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="67796-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67796-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67796-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67796-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67796-105">DESCRIPTION</span></span>
<span data-ttu-id="67796-106">**Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="67796-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="67796-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67796-107">EXAMPLES</span></span>

### <span data-ttu-id="67796-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67796-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="67796-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="67796-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="67796-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="67796-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="67796-111">Son komut $Settings depolanan arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını, false değerine ve DrainTimeoutInSec 'e 3600 'e ayarlayarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="67796-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="67796-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67796-112">PARAMETERS</span></span>

### <span data-ttu-id="67796-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67796-113">-BackendHttpSettings</span></span>
<span data-ttu-id="67796-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="67796-114">The backend http settings</span></span>

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

### <span data-ttu-id="67796-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67796-115">-DefaultProfile</span></span>
<span data-ttu-id="67796-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67796-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67796-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="67796-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="67796-118">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="67796-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="67796-119">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="67796-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="67796-120">Özellikli</span><span class="sxs-lookup"><span data-stu-id="67796-120">-Enabled</span></span>
<span data-ttu-id="67796-121">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="67796-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="67796-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67796-122">CommonParameters</span></span>
<span data-ttu-id="67796-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67796-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67796-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67796-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67796-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67796-125">INPUTS</span></span>

### <span data-ttu-id="67796-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67796-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="67796-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67796-127">OUTPUTS</span></span>

### <span data-ttu-id="67796-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67796-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="67796-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67796-129">NOTES</span></span>

## <span data-ttu-id="67796-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67796-130">RELATED LINKS</span></span>

[<span data-ttu-id="67796-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67796-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="67796-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67796-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="67796-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="67796-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="67796-134">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="67796-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="67796-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="67796-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

