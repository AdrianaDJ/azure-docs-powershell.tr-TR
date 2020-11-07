---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 0c50f8b7fdd4a2093a734f3759bf6a893e56a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763024"
---
# <span data-ttu-id="b8277-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8277-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b8277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8277-102">SYNOPSIS</span></span>
<span data-ttu-id="b8277-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b8277-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8277-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8277-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8277-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8277-105">DESCRIPTION</span></span>
<span data-ttu-id="b8277-106">**Get-AzureRmApplicationGatewayConnectionDraining** cmdlet 'i arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="b8277-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b8277-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8277-107">EXAMPLES</span></span>

### <span data-ttu-id="b8277-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8277-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="b8277-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b8277-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8277-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="b8277-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b8277-111">Son komut arka uç HTTP ayarları $Settings bağlantı boşaltma yapılandırmasını alır ve $ConnectionDraining değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b8277-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="b8277-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8277-112">PARAMETERS</span></span>

### <span data-ttu-id="b8277-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8277-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b8277-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="b8277-114">The backend http settings</span></span>

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

### <span data-ttu-id="b8277-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8277-115">-DefaultProfile</span></span>
<span data-ttu-id="b8277-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8277-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8277-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8277-117">CommonParameters</span></span>
<span data-ttu-id="b8277-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8277-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8277-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8277-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8277-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8277-120">INPUTS</span></span>

### <span data-ttu-id="b8277-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8277-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b8277-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8277-122">OUTPUTS</span></span>

### <span data-ttu-id="b8277-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8277-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b8277-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8277-124">NOTES</span></span>

## <span data-ttu-id="b8277-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8277-125">RELATED LINKS</span></span>

[<span data-ttu-id="b8277-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8277-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="b8277-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8277-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="b8277-128">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8277-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8277-129">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8277-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8277-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8277-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
