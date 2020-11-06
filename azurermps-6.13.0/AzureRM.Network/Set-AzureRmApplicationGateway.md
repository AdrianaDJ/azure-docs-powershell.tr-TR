---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: d9eb7f4783f950ba001be5b173fca9614422ce9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593938"
---
# <span data-ttu-id="2c15c-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c15c-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2c15c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c15c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c15c-103">Uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c15c-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c15c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c15c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c15c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c15c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c15c-106">**Set-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c15c-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="2c15c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c15c-107">EXAMPLES</span></span>

### <span data-ttu-id="2c15c-108">Örnek 1: uygulama ağ geçidini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2c15c-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="2c15c-109">Bu komut, uygulama ağ geçidini $AppGw değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2c15c-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="2c15c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c15c-110">PARAMETERS</span></span>

### <span data-ttu-id="2c15c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c15c-111">-ApplicationGateway</span></span>
<span data-ttu-id="2c15c-112">Uygulama ağ geçidinin ayarlanması gereken durumu temsil eden bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c15c-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="2c15c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2c15c-113">-AsJob</span></span>
<span data-ttu-id="2c15c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2c15c-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c15c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c15c-115">-DefaultProfile</span></span>
<span data-ttu-id="2c15c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c15c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c15c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c15c-117">CommonParameters</span></span>
<span data-ttu-id="2c15c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c15c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c15c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c15c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c15c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c15c-120">INPUTS</span></span>

### <span data-ttu-id="2c15c-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c15c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="2c15c-122">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c15c-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="2c15c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c15c-123">OUTPUTS</span></span>

### <span data-ttu-id="2c15c-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c15c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c15c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c15c-125">NOTES</span></span>

## <span data-ttu-id="2c15c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c15c-126">RELATED LINKS</span></span>

[<span data-ttu-id="2c15c-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c15c-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


