---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: acc0157cf24a4eb3c1611dd25fc5939a704463db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763022"
---
# <span data-ttu-id="12f08-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="12f08-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="12f08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f08-102">SYNOPSIS</span></span>
<span data-ttu-id="12f08-103">Uygulama ağ geçidinin ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="12f08-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12f08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12f08-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12f08-105">DESCRIPTION</span></span>
<span data-ttu-id="12f08-106">**Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet 'i, uygulama ağ geçidinin ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="12f08-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="12f08-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12f08-107">EXAMPLES</span></span>

### <span data-ttu-id="12f08-108">Örnek 1: belirtilen ön uç IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="12f08-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="12f08-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FrontEndIP01 adlı ön uç IP yapılandırmasını $AppGw ve $FrontEndIP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12f08-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="12f08-110">Örnek 2: ön uç IP yapılandırmalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="12f08-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="12f08-111">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw 'dan ön uç IP yapılandırmalarının bir listesini alır ve $FrontEndIPs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12f08-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="12f08-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12f08-112">PARAMETERS</span></span>

### <span data-ttu-id="12f08-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12f08-113">-ApplicationGateway</span></span>
<span data-ttu-id="12f08-114">Ön uç IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f08-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="12f08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f08-115">-DefaultProfile</span></span>
<span data-ttu-id="12f08-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12f08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12f08-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="12f08-117">-Name</span></span>
<span data-ttu-id="12f08-118">Bu cmdlet 'in aldığı ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f08-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12f08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f08-119">CommonParameters</span></span>
<span data-ttu-id="12f08-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12f08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f08-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f08-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f08-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12f08-122">INPUTS</span></span>

### <span data-ttu-id="12f08-123">System. String</span><span class="sxs-lookup"><span data-stu-id="12f08-123">System.String</span></span>

## <span data-ttu-id="12f08-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12f08-124">OUTPUTS</span></span>

### <span data-ttu-id="12f08-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12f08-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="12f08-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12f08-126">NOTES</span></span>

## <span data-ttu-id="12f08-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12f08-127">RELATED LINKS</span></span>

[<span data-ttu-id="12f08-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="12f08-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="12f08-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="12f08-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="12f08-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="12f08-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="12f08-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="12f08-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


