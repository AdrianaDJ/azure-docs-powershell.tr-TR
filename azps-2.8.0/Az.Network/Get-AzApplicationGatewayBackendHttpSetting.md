---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 0261eb6ed3a88ca33edce134911c405f530a2a5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932065"
---
# <span data-ttu-id="871ae-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="871ae-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="871ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="871ae-102">SYNOPSIS</span></span>
<span data-ttu-id="871ae-103">Uygulama ağ geçidinin geri dönüş HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="871ae-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="871ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="871ae-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="871ae-105">DESCRIPTION</span></span>
<span data-ttu-id="871ae-106">Get-AzApplicationGatewayBackendHttpSetting cmdlet 'i, uygulama ağ geçidinin arka uç HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="871ae-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="871ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="871ae-107">EXAMPLES</span></span>

### <span data-ttu-id="871ae-108">Örnek 1: geri dönüş HTTP ayarlarını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="871ae-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="871ae-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için Settings01 adındaki HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="871ae-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="871ae-110">Örnek 2: arka plan HTTP ayarları koleksiyonu alma</span><span class="sxs-lookup"><span data-stu-id="871ae-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="871ae-111">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için HTTP ayarları koleksiyonunu alır ve $SettingsList değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="871ae-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="871ae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="871ae-112">PARAMETERS</span></span>

### <span data-ttu-id="871ae-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="871ae-113">-ApplicationGateway</span></span>
<span data-ttu-id="871ae-114">Geri dönüş HTTP ayarlarını içeren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="871ae-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="871ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871ae-115">-DefaultProfile</span></span>
<span data-ttu-id="871ae-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="871ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="871ae-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="871ae-117">-Name</span></span>
<span data-ttu-id="871ae-118">Bu cmdlet 'in aldığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="871ae-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871ae-119">CommonParameters</span></span>
<span data-ttu-id="871ae-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="871ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871ae-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="871ae-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871ae-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="871ae-122">INPUTS</span></span>

### <span data-ttu-id="871ae-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="871ae-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="871ae-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="871ae-124">OUTPUTS</span></span>

### <span data-ttu-id="871ae-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="871ae-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="871ae-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="871ae-126">NOTES</span></span>

## <span data-ttu-id="871ae-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="871ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="871ae-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="871ae-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="871ae-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="871ae-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="871ae-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="871ae-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="871ae-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="871ae-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)
