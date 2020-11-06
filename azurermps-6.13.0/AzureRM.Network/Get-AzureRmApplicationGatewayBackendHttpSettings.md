---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: d7dc38e25ffda43eae3c29bc0e3db83f1a27c9f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589510"
---
# <span data-ttu-id="24330-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="24330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24330-102">SYNOPSIS</span></span>
<span data-ttu-id="24330-103">Uygulama ağ geçidinin geri dönüş HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="24330-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24330-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24330-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24330-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24330-105">DESCRIPTION</span></span>
<span data-ttu-id="24330-106">Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i, uygulama ağ geçidinin arka uç HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="24330-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="24330-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24330-107">EXAMPLES</span></span>

### <span data-ttu-id="24330-108">Örnek 1: geri dönüş HTTP ayarlarını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="24330-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="24330-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için Settings01 adındaki HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="24330-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="24330-110">Örnek 2: arka plan HTTP ayarları koleksiyonu alma</span><span class="sxs-lookup"><span data-stu-id="24330-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="24330-111">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için HTTP ayarları koleksiyonunu alır ve $SettingsList değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="24330-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="24330-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24330-112">PARAMETERS</span></span>

### <span data-ttu-id="24330-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24330-113">-ApplicationGateway</span></span>
<span data-ttu-id="24330-114">Geri dönüş HTTP ayarlarını içeren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="24330-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="24330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24330-115">-DefaultProfile</span></span>
<span data-ttu-id="24330-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24330-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24330-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="24330-117">-Name</span></span>
<span data-ttu-id="24330-118">Bu cmdlet 'in aldığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24330-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24330-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24330-119">CommonParameters</span></span>
<span data-ttu-id="24330-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24330-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24330-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24330-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24330-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24330-122">INPUTS</span></span>

### <span data-ttu-id="24330-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24330-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="24330-124">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24330-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="24330-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24330-125">OUTPUTS</span></span>

### <span data-ttu-id="24330-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="24330-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24330-127">NOTES</span></span>

## <span data-ttu-id="24330-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24330-128">RELATED LINKS</span></span>

[<span data-ttu-id="24330-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-129">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24330-130">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-130">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24330-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-131">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="24330-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24330-132">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

