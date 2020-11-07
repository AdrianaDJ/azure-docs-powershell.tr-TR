---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939066"
---
# <span data-ttu-id="d7fe9-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="d7fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fe9-103">Uygulama ağ geçidini durdurur</span><span class="sxs-lookup"><span data-stu-id="d7fe9-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7fe9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7fe9-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7fe9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fe9-106">**Stop-AzureRmApplicationGateway** cmdlet 'i bir uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="d7fe9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7fe9-107">EXAMPLES</span></span>

### <span data-ttu-id="d7fe9-108">Örnek 1: uygulama ağ geçidini durdurma</span><span class="sxs-lookup"><span data-stu-id="d7fe9-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d7fe9-109">Bu komut $AppGw değişkeninde depolanan uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d7fe9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7fe9-110">PARAMETERS</span></span>

### <span data-ttu-id="d7fe9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-111">-ApplicationGateway</span></span>
<span data-ttu-id="d7fe9-112">Bu cmdlet 'in durdurduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d7fe9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d7fe9-113">-AsJob</span></span>
<span data-ttu-id="d7fe9-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d7fe9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7fe9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fe9-115">-DefaultProfile</span></span>
<span data-ttu-id="d7fe9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7fe9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fe9-117">CommonParameters</span></span>
<span data-ttu-id="d7fe9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7fe9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fe9-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fe9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fe9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7fe9-120">INPUTS</span></span>

### <span data-ttu-id="d7fe9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d7fe9-121">System.String</span></span>

## <span data-ttu-id="d7fe9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7fe9-122">OUTPUTS</span></span>

### <span data-ttu-id="d7fe9-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7fe9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7fe9-124">NOTES</span></span>

## <span data-ttu-id="d7fe9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7fe9-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7fe9-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="d7fe9-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="d7fe9-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="d7fe9-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="d7fe9-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7fe9-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


