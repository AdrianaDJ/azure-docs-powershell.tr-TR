---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594230"
---
# <span data-ttu-id="092fb-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="092fb-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="092fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="092fb-102">SYNOPSIS</span></span>
<span data-ttu-id="092fb-103">Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="092fb-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="092fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="092fb-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="092fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="092fb-105">DESCRIPTION</span></span>
<span data-ttu-id="092fb-106">**New-AzureRmApplicationGatewayConnectionDraining** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="092fb-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="092fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="092fb-107">EXAMPLES</span></span>

### <span data-ttu-id="092fb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="092fb-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="092fb-109">Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="092fb-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="092fb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="092fb-110">PARAMETERS</span></span>

### <span data-ttu-id="092fb-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="092fb-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="092fb-112">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="092fb-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="092fb-113">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="092fb-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="092fb-114">Özellikli</span><span class="sxs-lookup"><span data-stu-id="092fb-114">-Enabled</span></span>
<span data-ttu-id="092fb-115">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="092fb-115">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092fb-116">-DefaultProfile</span></span>
<span data-ttu-id="092fb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="092fb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="092fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092fb-118">CommonParameters</span></span>
<span data-ttu-id="092fb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="092fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092fb-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="092fb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092fb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="092fb-121">INPUTS</span></span>

### <span data-ttu-id="092fb-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="092fb-122">None</span></span>

## <span data-ttu-id="092fb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="092fb-123">OUTPUTS</span></span>

### <span data-ttu-id="092fb-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="092fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="092fb-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="092fb-125">NOTES</span></span>

## <span data-ttu-id="092fb-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="092fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="092fb-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="092fb-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="092fb-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="092fb-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="092fb-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="092fb-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

