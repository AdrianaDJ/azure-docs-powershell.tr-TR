---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 6c5729ec4d450ad122e359b9bd009000212e3b0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918136"
---
# <span data-ttu-id="1a03a-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1a03a-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="1a03a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a03a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a03a-103">Uygulama ağ geçidinden arka uç HTTP ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a03a-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="1a03a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a03a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a03a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a03a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a03a-106">Remove-AzApplicationGatewayBackendHttpSetting cmdlet 'i bir Azure uygulama ağ geçidinden arka uç köprü metni Aktarma Protokolü (HTTP) ayarlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a03a-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="1a03a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a03a-107">EXAMPLES</span></span>

### <span data-ttu-id="1a03a-108">Örnek 1: uygulama ağ geçidinden geri açılan HTTP ayarlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1a03a-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="1a03a-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1a03a-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1a03a-110">İkinci komut, BackEndSetting02 adlı geri dönüş HTTP ayarını $AppGw depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a03a-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1a03a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a03a-111">PARAMETERS</span></span>

### <span data-ttu-id="1a03a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a03a-112">-ApplicationGateway</span></span>
<span data-ttu-id="1a03a-113">Bu cmdlet 'in arka uç HTTP ayarlarını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a03a-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="1a03a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a03a-114">-DefaultProfile</span></span>
<span data-ttu-id="1a03a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a03a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a03a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a03a-116">-Name</span></span>
<span data-ttu-id="1a03a-117">Bu cmdlet 'in kaldırdığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a03a-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1a03a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a03a-118">CommonParameters</span></span>
<span data-ttu-id="1a03a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a03a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a03a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a03a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a03a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a03a-121">INPUTS</span></span>

### <span data-ttu-id="1a03a-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a03a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a03a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a03a-123">OUTPUTS</span></span>

### <span data-ttu-id="1a03a-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a03a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a03a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a03a-125">NOTES</span></span>

## <span data-ttu-id="1a03a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a03a-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a03a-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1a03a-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1a03a-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1a03a-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1a03a-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1a03a-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1a03a-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1a03a-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

