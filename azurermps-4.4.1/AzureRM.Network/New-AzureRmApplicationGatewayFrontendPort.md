---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c12034d41eeecbba2146592247a034f99af94c89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764807"
---
# <span data-ttu-id="deeed-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="deeed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deeed-102">SYNOPSIS</span></span>
<span data-ttu-id="deeed-103">Uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="deeed-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deeed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deeed-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deeed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="deeed-105">DESCRIPTION</span></span>
<span data-ttu-id="deeed-106">**New-AzureRmApplicationGatewayFrontendPort** cmdlet 'ı bir Azure Application Gateway için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="deeed-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="deeed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deeed-107">EXAMPLES</span></span>

### <span data-ttu-id="deeed-108">Example1: ön uç bağlantı noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="deeed-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="deeed-109">Bu komut FrontEndPort01 adlı bir ön uç bağlantı noktası 80 bağlantı noktası oluşturur ve sonucu $FrontEndPort adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="deeed-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="deeed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deeed-110">PARAMETERS</span></span>

### <span data-ttu-id="deeed-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="deeed-111">-Name</span></span>
<span data-ttu-id="deeed-112">Bu cmdlet 'in oluşturduğu ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deeed-112">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="deeed-113">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="deeed-113">-Port</span></span>
<span data-ttu-id="deeed-114">Ön uç bağlantı noktasının bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deeed-114">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deeed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deeed-115">-DefaultProfile</span></span>
<span data-ttu-id="deeed-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="deeed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deeed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deeed-117">CommonParameters</span></span>
<span data-ttu-id="deeed-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deeed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deeed-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deeed-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deeed-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deeed-120">INPUTS</span></span>

### <span data-ttu-id="deeed-121">System. String</span><span class="sxs-lookup"><span data-stu-id="deeed-121">System.String</span></span>

## <span data-ttu-id="deeed-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deeed-122">OUTPUTS</span></span>

### <span data-ttu-id="deeed-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="deeed-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deeed-124">NOTES</span></span>

## <span data-ttu-id="deeed-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deeed-125">RELATED LINKS</span></span>

[<span data-ttu-id="deeed-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="deeed-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="deeed-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="deeed-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="deeed-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


