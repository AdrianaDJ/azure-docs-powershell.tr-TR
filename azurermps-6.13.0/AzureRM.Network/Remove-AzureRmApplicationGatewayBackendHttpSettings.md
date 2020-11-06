---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 036fef4e43d8d754bd0798e72159cba367a3e2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588459"
---
# <span data-ttu-id="1def6-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1def6-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1def6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1def6-102">SYNOPSIS</span></span>
<span data-ttu-id="1def6-103">Uygulama ağ geçidinden arka uç HTTP ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1def6-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1def6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1def6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1def6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1def6-105">DESCRIPTION</span></span>
<span data-ttu-id="1def6-106">Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i bir Azure uygulama ağ geçidinden arka uç köprü metni Aktarma Protokolü (HTTP) ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1def6-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="1def6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1def6-107">EXAMPLES</span></span>

### <span data-ttu-id="1def6-108">Örnek 1: uygulama ağ geçidinden geri açılan HTTP ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1def6-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="1def6-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1def6-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1def6-110">İkinci komut, BackEndSetting02 adlı geri dönüş HTTP ayarını $AppGw depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1def6-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1def6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1def6-111">PARAMETERS</span></span>

### <span data-ttu-id="1def6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1def6-112">-ApplicationGateway</span></span>
<span data-ttu-id="1def6-113">Bu cmdlet 'in arka uç HTTP ayarlarını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1def6-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1def6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1def6-114">-DefaultProfile</span></span>
<span data-ttu-id="1def6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1def6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1def6-116">-Name</span></span>
<span data-ttu-id="1def6-117">Bu cmdlet 'in kaldırdığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1def6-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1def6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1def6-118">CommonParameters</span></span>
<span data-ttu-id="1def6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1def6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1def6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1def6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1def6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1def6-121">INPUTS</span></span>

### <span data-ttu-id="1def6-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1def6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1def6-123">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1def6-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1def6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1def6-124">OUTPUTS</span></span>

### <span data-ttu-id="1def6-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1def6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1def6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1def6-126">NOTES</span></span>

## <span data-ttu-id="1def6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1def6-127">RELATED LINKS</span></span>

[<span data-ttu-id="1def6-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1def6-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1def6-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1def6-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1def6-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1def6-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1def6-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1def6-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

