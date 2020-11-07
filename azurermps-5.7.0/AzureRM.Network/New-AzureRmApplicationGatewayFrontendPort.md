---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: bccdcb5f94cc90dca04229ca643fd23f29a276e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762630"
---
# <span data-ttu-id="dba00-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="dba00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba00-102">SYNOPSIS</span></span>
<span data-ttu-id="dba00-103">Uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dba00-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dba00-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dba00-105">DESCRIPTION</span></span>
<span data-ttu-id="dba00-106">**New-AzureRmApplicationGatewayFrontendPort** cmdlet 'ı bir Azure Application Gateway için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dba00-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="dba00-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dba00-107">EXAMPLES</span></span>

### <span data-ttu-id="dba00-108">Example1: ön uç bağlantı noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="dba00-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="dba00-109">Bu komut FrontEndPort01 adlı bir ön uç bağlantı noktası 80 bağlantı noktası oluşturur ve sonucu $FrontEndPort adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="dba00-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="dba00-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dba00-110">PARAMETERS</span></span>

### <span data-ttu-id="dba00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba00-111">-DefaultProfile</span></span>
<span data-ttu-id="dba00-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dba00-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba00-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dba00-113">-Name</span></span>
<span data-ttu-id="dba00-114">Bu cmdlet 'in oluşturduğu ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dba00-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba00-115">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="dba00-115">-Port</span></span>
<span data-ttu-id="dba00-116">Ön uç bağlantı noktasının bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dba00-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="dba00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba00-117">CommonParameters</span></span>
<span data-ttu-id="dba00-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dba00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba00-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba00-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dba00-120">INPUTS</span></span>

### <span data-ttu-id="dba00-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dba00-121">System.String</span></span>

## <span data-ttu-id="dba00-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dba00-122">OUTPUTS</span></span>

### <span data-ttu-id="dba00-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="dba00-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dba00-124">NOTES</span></span>

## <span data-ttu-id="dba00-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dba00-125">RELATED LINKS</span></span>

[<span data-ttu-id="dba00-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dba00-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dba00-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="dba00-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="dba00-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

