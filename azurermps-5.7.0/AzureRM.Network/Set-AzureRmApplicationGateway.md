---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: ff836268c92b575db05e05b1843c57af2bc6dca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594056"
---
# <span data-ttu-id="090c4-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="090c4-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="090c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="090c4-102">SYNOPSIS</span></span>
<span data-ttu-id="090c4-103">Uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="090c4-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="090c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="090c4-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="090c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="090c4-105">DESCRIPTION</span></span>
<span data-ttu-id="090c4-106">**Set-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="090c4-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="090c4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="090c4-107">EXAMPLES</span></span>

### <span data-ttu-id="090c4-108">Örnek 1: uygulama ağ geçidini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="090c4-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="090c4-109">Bu komut, uygulama ağ geçidini $AppGw değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="090c4-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="090c4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="090c4-110">PARAMETERS</span></span>

### <span data-ttu-id="090c4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="090c4-111">-ApplicationGateway</span></span>
<span data-ttu-id="090c4-112">Uygulama ağ geçidinin ayarlanması gereken durumu temsil eden bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="090c4-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="090c4-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="090c4-113">-AsJob</span></span>
<span data-ttu-id="090c4-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="090c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="090c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="090c4-115">-DefaultProfile</span></span>
<span data-ttu-id="090c4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="090c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="090c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090c4-117">CommonParameters</span></span>
<span data-ttu-id="090c4-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="090c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090c4-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090c4-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="090c4-120">INPUTS</span></span>

### <span data-ttu-id="090c4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="090c4-121">PSApplicationGateway</span></span>
<span data-ttu-id="090c4-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="090c4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="090c4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="090c4-123">OUTPUTS</span></span>

### <span data-ttu-id="090c4-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="090c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="090c4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="090c4-125">NOTES</span></span>

## <span data-ttu-id="090c4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="090c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="090c4-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="090c4-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


