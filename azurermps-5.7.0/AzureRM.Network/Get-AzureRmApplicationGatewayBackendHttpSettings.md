---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590986"
---
# <span data-ttu-id="16540-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="16540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16540-102">SYNOPSIS</span></span>
<span data-ttu-id="16540-103">Uygulama ağ geçidinin geri dönüş HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16540-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16540-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16540-105">DESCRIPTION</span></span>
<span data-ttu-id="16540-106">Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i, uygulama ağ geçidinin arka uç HTTP ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="16540-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16540-107">EXAMPLES</span></span>

### <span data-ttu-id="16540-108">Örnek 1: geri dönüş HTTP ayarlarını ada göre alma</span><span class="sxs-lookup"><span data-stu-id="16540-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="16540-109">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için Settings01 adındaki HTTP ayarlarını alır ve $Settings değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="16540-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="16540-110">Örnek 2: arka plan HTTP ayarları koleksiyonu alma</span><span class="sxs-lookup"><span data-stu-id="16540-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="16540-111">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw için HTTP ayarları koleksiyonunu alır ve $SettingsList değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="16540-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="16540-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16540-112">PARAMETERS</span></span>

### <span data-ttu-id="16540-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16540-113">-ApplicationGateway</span></span>
<span data-ttu-id="16540-114">Geri dönüş HTTP ayarlarını içeren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16540-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16540-115">-DefaultProfile</span></span>
<span data-ttu-id="16540-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16540-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16540-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="16540-117">-Name</span></span>
<span data-ttu-id="16540-118">Bu cmdlet 'in aldığı arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16540-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16540-119">CommonParameters</span></span>
<span data-ttu-id="16540-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16540-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16540-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16540-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16540-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16540-122">INPUTS</span></span>

### <span data-ttu-id="16540-123">System. String</span><span class="sxs-lookup"><span data-stu-id="16540-123">System.String</span></span>

## <span data-ttu-id="16540-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16540-124">OUTPUTS</span></span>

### <span data-ttu-id="16540-125">Microsoft. Azure. Commands. Network. modeller. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="16540-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16540-126">NOTES</span></span>

## <span data-ttu-id="16540-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16540-127">RELATED LINKS</span></span>

[<span data-ttu-id="16540-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="16540-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="16540-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="16540-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="16540-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

