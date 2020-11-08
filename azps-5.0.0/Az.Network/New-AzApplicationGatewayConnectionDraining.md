---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279685"
---
# <span data-ttu-id="1c924-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1c924-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="1c924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c924-102">SYNOPSIS</span></span>
<span data-ttu-id="1c924-103">Arka uç HTTP ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c924-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="1c924-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c924-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c924-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c924-105">DESCRIPTION</span></span>
<span data-ttu-id="1c924-106">**Yeni-Azapplicationgatewayconnectionboşaltma** cmdlet 'i arka uç http ayarları için yeni bir bağlantı boşaltma yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c924-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="1c924-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c924-107">EXAMPLES</span></span>

### <span data-ttu-id="1c924-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1c924-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="1c924-109">Bu komut, Enabled değeri true olarak ayarlanmış yeni bir bağlantı boşaltma yapılandırması oluşturur ve DrainTimeoutInSec olarak 42 ayarlanır ve $connectionDraining içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="1c924-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="1c924-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c924-110">PARAMETERS</span></span>

### <span data-ttu-id="1c924-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c924-111">-DefaultProfile</span></span>
<span data-ttu-id="1c924-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c924-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c924-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="1c924-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="1c924-114">Saniye bağlantısı boşaltma etkin.</span><span class="sxs-lookup"><span data-stu-id="1c924-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="1c924-115">Kabul edilebilir değerler 1 saniye ile 3600 saniye arasında değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="1c924-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="1c924-116">Özellikli</span><span class="sxs-lookup"><span data-stu-id="1c924-116">-Enabled</span></span>
<span data-ttu-id="1c924-117">Bağlantı boşaltma 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="1c924-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="1c924-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c924-118">CommonParameters</span></span>
<span data-ttu-id="1c924-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c924-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c924-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c924-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c924-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c924-121">INPUTS</span></span>

### <span data-ttu-id="1c924-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1c924-122">None</span></span>

## <span data-ttu-id="1c924-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c924-123">OUTPUTS</span></span>

### <span data-ttu-id="1c924-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1c924-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="1c924-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c924-125">NOTES</span></span>

## <span data-ttu-id="1c924-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c924-126">RELATED LINKS</span></span>

[<span data-ttu-id="1c924-127">Get-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="1c924-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="1c924-128">Remove-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="1c924-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="1c924-129">Set-Azapplicationgatewayconnectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="1c924-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

