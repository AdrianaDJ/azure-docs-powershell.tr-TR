---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 7dab3fd72dcd7ac097dbf5a1d5da342c39d3c504
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933401"
---
# <span data-ttu-id="e6cb9-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="e6cb9-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="e6cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cb9-103">Geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="e6cb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6cb9-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6cb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cb9-106">**Get-AzRelayHybridConnection** cmdlet 'ı, geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="e6cb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cb9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6cb9-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="e6cb9-109">HybridConnection 'un açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="e6cb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6cb9-110">PARAMETERS</span></span>

### <span data-ttu-id="e6cb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cb9-111">-DefaultProfile</span></span>
<span data-ttu-id="e6cb9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cb9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6cb9-113">-Name</span></span>
<span data-ttu-id="e6cb9-114">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cb9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e6cb9-115">-Namespace</span></span>
<span data-ttu-id="e6cb9-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-116">Namespace Name.</span></span>

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

### <span data-ttu-id="e6cb9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cb9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6cb9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e6cb9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cb9-119">CommonParameters</span></span>
<span data-ttu-id="e6cb9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6cb9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cb9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cb9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cb9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6cb9-122">INPUTS</span></span>

### <span data-ttu-id="e6cb9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e6cb9-123">System.String</span></span>

## <span data-ttu-id="e6cb9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6cb9-124">OUTPUTS</span></span>

### <span data-ttu-id="e6cb9-125">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="e6cb9-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="e6cb9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6cb9-126">NOTES</span></span>

## <span data-ttu-id="e6cb9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6cb9-127">RELATED LINKS</span></span>