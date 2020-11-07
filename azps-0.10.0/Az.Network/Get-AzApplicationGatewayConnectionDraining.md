---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 842ac402becd78decb00333c39a4a8247d543987
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935589"
---
# <span data-ttu-id="5672d-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5672d-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5672d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5672d-102">SYNOPSIS</span></span>
<span data-ttu-id="5672d-103">Arka uç HTTP ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5672d-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="5672d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5672d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5672d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5672d-105">DESCRIPTION</span></span>
<span data-ttu-id="5672d-106">**Get-Azapplicationgatewayconnectionboşaltma** cmdlet 'i, arka uç http ayarları nesnesinin bağlantı boşaltma yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5672d-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="5672d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5672d-107">EXAMPLES</span></span>

### <span data-ttu-id="5672d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5672d-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="5672d-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5672d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5672d-110">İkinci komut $AppGw için Settings01 adlı arka uç HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="5672d-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="5672d-111">Son komut arka uç HTTP ayarları $Settings bağlantı boşaltma yapılandırmasını alır ve $ConnectionDraining değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5672d-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="5672d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5672d-112">PARAMETERS</span></span>

### <span data-ttu-id="5672d-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5672d-113">-BackendHttpSettings</span></span>
<span data-ttu-id="5672d-114">Arka uç http ayarları</span><span class="sxs-lookup"><span data-stu-id="5672d-114">The backend http settings</span></span>

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

### <span data-ttu-id="5672d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5672d-115">-DefaultProfile</span></span>
<span data-ttu-id="5672d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5672d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5672d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5672d-117">CommonParameters</span></span>
<span data-ttu-id="5672d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5672d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5672d-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5672d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5672d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5672d-120">INPUTS</span></span>

### <span data-ttu-id="5672d-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5672d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="5672d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5672d-122">OUTPUTS</span></span>

### <span data-ttu-id="5672d-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5672d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5672d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5672d-124">NOTES</span></span>

## <span data-ttu-id="5672d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5672d-125">RELATED LINKS</span></span>

[<span data-ttu-id="5672d-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5672d-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="5672d-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5672d-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5672d-128">Yeni-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="5672d-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5672d-129">Remove-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="5672d-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5672d-130">Set-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="5672d-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
