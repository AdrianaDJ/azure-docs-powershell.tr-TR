---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760427"
---
# <span data-ttu-id="8a48f-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8a48f-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="8a48f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a48f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a48f-103">Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a48f-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="8a48f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a48f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a48f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a48f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a48f-106">**Yeni-Azapplicationgatewayconnectionboşaltma** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a48f-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="8a48f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a48f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a48f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a48f-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="8a48f-109">Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="8a48f-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="8a48f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a48f-110">PARAMETERS</span></span>

### <span data-ttu-id="8a48f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a48f-111">-DefaultProfile</span></span>
<span data-ttu-id="8a48f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a48f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a48f-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="8a48f-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="8a48f-114">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="8a48f-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="8a48f-115">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="8a48f-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="8a48f-116">Özellikli</span><span class="sxs-lookup"><span data-stu-id="8a48f-116">-Enabled</span></span>
<span data-ttu-id="8a48f-117">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="8a48f-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="8a48f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a48f-118">CommonParameters</span></span>
<span data-ttu-id="8a48f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a48f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a48f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a48f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a48f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a48f-121">INPUTS</span></span>

### <span data-ttu-id="8a48f-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a48f-122">None</span></span>

## <span data-ttu-id="8a48f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a48f-123">OUTPUTS</span></span>

### <span data-ttu-id="8a48f-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8a48f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="8a48f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a48f-125">NOTES</span></span>

## <span data-ttu-id="8a48f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a48f-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a48f-127">Get-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="8a48f-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8a48f-128">Remove-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="8a48f-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8a48f-129">Set-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="8a48f-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

