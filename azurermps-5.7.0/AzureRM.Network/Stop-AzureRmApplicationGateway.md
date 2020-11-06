---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: cf8a639b6ebbe2b5ea7c0e07f212de3c742e7556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590391"
---
# <span data-ttu-id="97fba-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="97fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97fba-102">SYNOPSIS</span></span>
<span data-ttu-id="97fba-103">Uygulama ağ geçidini durdurur</span><span class="sxs-lookup"><span data-stu-id="97fba-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97fba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97fba-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97fba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97fba-105">DESCRIPTION</span></span>
<span data-ttu-id="97fba-106">**Stop-AzureRmApplicationGateway** cmdlet 'i bir uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="97fba-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="97fba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97fba-107">EXAMPLES</span></span>

### <span data-ttu-id="97fba-108">Örnek 1: uygulama ağ geçidini durdurma</span><span class="sxs-lookup"><span data-stu-id="97fba-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="97fba-109">Bu komut $AppGw değişkeninde depolanan uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="97fba-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="97fba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97fba-110">PARAMETERS</span></span>

### <span data-ttu-id="97fba-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-111">-ApplicationGateway</span></span>
<span data-ttu-id="97fba-112">Bu cmdlet 'in durdurduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97fba-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="97fba-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="97fba-113">-AsJob</span></span>
<span data-ttu-id="97fba-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="97fba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97fba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fba-115">-DefaultProfile</span></span>
<span data-ttu-id="97fba-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97fba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97fba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fba-117">CommonParameters</span></span>
<span data-ttu-id="97fba-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97fba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fba-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fba-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fba-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97fba-120">INPUTS</span></span>

### <span data-ttu-id="97fba-121">System. String</span><span class="sxs-lookup"><span data-stu-id="97fba-121">System.String</span></span>

## <span data-ttu-id="97fba-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97fba-122">OUTPUTS</span></span>

### <span data-ttu-id="97fba-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97fba-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97fba-124">NOTES</span></span>

## <span data-ttu-id="97fba-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97fba-125">RELATED LINKS</span></span>

[<span data-ttu-id="97fba-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="97fba-127">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="97fba-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="97fba-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="97fba-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97fba-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


