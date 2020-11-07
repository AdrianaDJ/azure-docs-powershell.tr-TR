---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: b7d49645426425f914714f65c244974277e975e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918348"
---
# <span data-ttu-id="fb33f-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="fb33f-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="fb33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb33f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb33f-103">Güvenlik duvarı durumu için eşleştirme değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb33f-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="fb33f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb33f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb33f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb33f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb33f-106">**Yeni-AzApplicationGatewayFirewallMatchVariable** , güvenlik duvarı koşulu için eşleştirme değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb33f-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="fb33f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb33f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb33f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb33f-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="fb33f-109">Komut, istek üst bilgilerinin ve seçicinin adıyla yeni bir eşleşme değişkeni oluşturur;</span><span class="sxs-lookup"><span data-stu-id="fb33f-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="fb33f-110">Yeni eşleşme değişkeni $variable kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="fb33f-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="fb33f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb33f-111">PARAMETERS</span></span>

### <span data-ttu-id="fb33f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb33f-112">-DefaultProfile</span></span>
<span data-ttu-id="fb33f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb33f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb33f-114">-Seçici</span><span class="sxs-lookup"><span data-stu-id="fb33f-114">-Selector</span></span>
<span data-ttu-id="fb33f-115">MatchVariable koleksiyonunun bir alanını açıklar.</span><span class="sxs-lookup"><span data-stu-id="fb33f-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb33f-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="fb33f-116">-VariableName</span></span>
<span data-ttu-id="fb33f-117">Değişkeni eşle.</span><span class="sxs-lookup"><span data-stu-id="fb33f-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb33f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb33f-118">CommonParameters</span></span>
<span data-ttu-id="fb33f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb33f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb33f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb33f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb33f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb33f-121">INPUTS</span></span>

### <span data-ttu-id="fb33f-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fb33f-122">None</span></span>

## <span data-ttu-id="fb33f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb33f-123">OUTPUTS</span></span>

### <span data-ttu-id="fb33f-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="fb33f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="fb33f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb33f-125">NOTES</span></span>

## <span data-ttu-id="fb33f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb33f-126">RELATED LINKS</span></span>