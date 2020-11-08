---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938166"
---
# <span data-ttu-id="16d18-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="16d18-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="16d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d18-102">SYNOPSIS</span></span>
<span data-ttu-id="16d18-103">Belirtilen WcfRelay için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="16d18-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="16d18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16d18-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16d18-105">DESCRIPTION</span></span>
<span data-ttu-id="16d18-106">**Get-AzWcfRelay** cmdlet 'ı belirtilen wcfrelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="16d18-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="16d18-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16d18-107">EXAMPLES</span></span>

### <span data-ttu-id="16d18-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16d18-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="16d18-109">WcfRelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="16d18-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="16d18-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16d18-110">PARAMETERS</span></span>

### <span data-ttu-id="16d18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d18-111">-DefaultProfile</span></span>
<span data-ttu-id="16d18-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16d18-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d18-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="16d18-113">-Name</span></span>
<span data-ttu-id="16d18-114">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="16d18-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d18-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16d18-115">-Namespace</span></span>
<span data-ttu-id="16d18-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="16d18-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d18-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d18-117">-ResourceGroupName</span></span>
<span data-ttu-id="16d18-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16d18-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d18-119">CommonParameters</span></span>
<span data-ttu-id="16d18-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16d18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d18-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d18-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d18-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16d18-122">INPUTS</span></span>

### <span data-ttu-id="16d18-123">System. String</span><span class="sxs-lookup"><span data-stu-id="16d18-123">System.String</span></span>

## <span data-ttu-id="16d18-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16d18-124">OUTPUTS</span></span>

### <span data-ttu-id="16d18-125">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="16d18-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="16d18-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16d18-126">NOTES</span></span>

## <span data-ttu-id="16d18-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16d18-127">RELATED LINKS</span></span>