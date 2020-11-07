---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 6e17db790cd776e8662c4c445e53604dcb8929de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939303"
---
# <span data-ttu-id="99f71-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="99f71-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="99f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f71-102">SYNOPSIS</span></span>
<span data-ttu-id="99f71-103">Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99f71-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99f71-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99f71-105">DESCRIPTION</span></span>
<span data-ttu-id="99f71-106">**New-AzureRmApplicationGatewayConnectionDraining** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99f71-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="99f71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99f71-107">EXAMPLES</span></span>

### <span data-ttu-id="99f71-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99f71-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="99f71-109">Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="99f71-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="99f71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99f71-110">PARAMETERS</span></span>

### <span data-ttu-id="99f71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f71-111">-DefaultProfile</span></span>
<span data-ttu-id="99f71-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99f71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99f71-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="99f71-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="99f71-114">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="99f71-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="99f71-115">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="99f71-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="99f71-116">Özellikli</span><span class="sxs-lookup"><span data-stu-id="99f71-116">-Enabled</span></span>
<span data-ttu-id="99f71-117">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="99f71-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f71-118">CommonParameters</span></span>
<span data-ttu-id="99f71-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99f71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f71-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f71-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99f71-121">INPUTS</span></span>

### <span data-ttu-id="99f71-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99f71-122">None</span></span>

## <span data-ttu-id="99f71-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99f71-123">OUTPUTS</span></span>

### <span data-ttu-id="99f71-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="99f71-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="99f71-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99f71-125">NOTES</span></span>

## <span data-ttu-id="99f71-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99f71-126">RELATED LINKS</span></span>

[<span data-ttu-id="99f71-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="99f71-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="99f71-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="99f71-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="99f71-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="99f71-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

