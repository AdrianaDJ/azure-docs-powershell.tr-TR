---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931932"
---
# <span data-ttu-id="5a4e7-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a4e7-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5a4e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4e7-103">Uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="5a4e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a4e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a4e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="5a4e7-106">**Yeni-Azapplicationgatewayfrontenvseçport** cmdlet 'ı bir Azure uygulama ağ geçidi için ön uç bağlantı noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="5a4e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a4e7-107">EXAMPLES</span></span>

### <span data-ttu-id="5a4e7-108">Example1: ön uç bağlantı noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a4e7-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5a4e7-109">Bu komut FrontEndPort01 adlı bir ön uç bağlantı noktası 80 bağlantı noktası oluşturur ve sonucu $FrontEndPort adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="5a4e7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a4e7-110">PARAMETERS</span></span>

### <span data-ttu-id="5a4e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4e7-111">-DefaultProfile</span></span>
<span data-ttu-id="5a4e7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a4e7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a4e7-113">-Name</span></span>
<span data-ttu-id="5a4e7-114">Bu cmdlet 'in oluşturduğu ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5a4e7-115">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="5a4e7-115">-Port</span></span>
<span data-ttu-id="5a4e7-116">Ön uç bağlantı noktasının bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="5a4e7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4e7-117">CommonParameters</span></span>
<span data-ttu-id="5a4e7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4e7-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4e7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4e7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a4e7-120">INPUTS</span></span>

### <span data-ttu-id="5a4e7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5a4e7-121">None</span></span>

## <span data-ttu-id="5a4e7-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a4e7-122">OUTPUTS</span></span>

### <span data-ttu-id="5a4e7-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a4e7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5a4e7-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a4e7-124">NOTES</span></span>

## <span data-ttu-id="5a4e7-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a4e7-125">RELATED LINKS</span></span>

[<span data-ttu-id="5a4e7-126">Add-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5a4e7-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a4e7-127">Get-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5a4e7-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a4e7-128">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5a4e7-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a4e7-129">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5a4e7-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


