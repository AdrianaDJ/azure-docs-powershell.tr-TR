---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 97dc4b46f4a9156bc43e7902d50414a586d0f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936488"
---
# <span data-ttu-id="e8d73-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="e8d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d73-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d73-103">Uygulama ağ geçidini durdurur</span><span class="sxs-lookup"><span data-stu-id="e8d73-103">Stops an application gateway</span></span>

## <span data-ttu-id="e8d73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8d73-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8d73-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d73-106">**Stop-AzApplicationGateway** cmdlet 'i bir uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e8d73-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="e8d73-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8d73-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d73-108">Örnek 1: uygulama ağ geçidini durdurma</span><span class="sxs-lookup"><span data-stu-id="e8d73-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e8d73-109">Bu komut $AppGw değişkeninde depolanan uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e8d73-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="e8d73-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8d73-110">PARAMETERS</span></span>

### <span data-ttu-id="e8d73-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-111">-ApplicationGateway</span></span>
<span data-ttu-id="e8d73-112">Bu cmdlet 'in durdurduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8d73-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e8d73-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="e8d73-113">-AsJob</span></span>
<span data-ttu-id="e8d73-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e8d73-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d73-115">-DefaultProfile</span></span>
<span data-ttu-id="e8d73-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8d73-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8d73-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d73-117">CommonParameters</span></span>
<span data-ttu-id="e8d73-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8d73-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d73-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d73-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d73-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8d73-120">INPUTS</span></span>

### <span data-ttu-id="e8d73-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d73-121">System.String</span></span>

## <span data-ttu-id="e8d73-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8d73-122">OUTPUTS</span></span>

### <span data-ttu-id="e8d73-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8d73-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8d73-124">NOTES</span></span>

## <span data-ttu-id="e8d73-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8d73-125">RELATED LINKS</span></span>

[<span data-ttu-id="e8d73-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="e8d73-127">Yeni-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="e8d73-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="e8d73-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="e8d73-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8d73-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


