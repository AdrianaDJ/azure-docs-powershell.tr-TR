---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 342c18add7438c75babd1225722c3830c4c5c696
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587190"
---
# <span data-ttu-id="8aa96-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="8aa96-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="8aa96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa96-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa96-103">Belirtilen WcfRelay için bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="8aa96-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aa96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8aa96-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8aa96-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa96-106">**Get-AzureRmWcfRelay** cmdlet 'ı belirtilen wcfrelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8aa96-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="8aa96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8aa96-107">EXAMPLES</span></span>

### <span data-ttu-id="8aa96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8aa96-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

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

<span data-ttu-id="8aa96-109">WcfRelay 'in açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8aa96-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="8aa96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8aa96-110">PARAMETERS</span></span>

### <span data-ttu-id="8aa96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa96-111">-DefaultProfile</span></span>
<span data-ttu-id="8aa96-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8aa96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa96-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8aa96-113">-Name</span></span>
<span data-ttu-id="8aa96-114">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="8aa96-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8aa96-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8aa96-115">-Namespace</span></span>
<span data-ttu-id="8aa96-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="8aa96-116">Namespace Name.</span></span>

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

### <span data-ttu-id="8aa96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa96-117">-ResourceGroupName</span></span>
<span data-ttu-id="8aa96-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8aa96-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="8aa96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa96-119">CommonParameters</span></span>
<span data-ttu-id="8aa96-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8aa96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8aa96-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aa96-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa96-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8aa96-122">INPUTS</span></span>

### <span data-ttu-id="8aa96-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8aa96-123">System.String</span></span>


## <span data-ttu-id="8aa96-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8aa96-124">OUTPUTS</span></span>

### <span data-ttu-id="8aa96-125">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8aa96-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="8aa96-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8aa96-126">NOTES</span></span>

## <span data-ttu-id="8aa96-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8aa96-127">RELATED LINKS</span></span>
