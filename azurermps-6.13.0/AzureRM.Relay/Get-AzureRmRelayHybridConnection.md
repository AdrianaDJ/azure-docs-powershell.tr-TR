---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 468128f16c3a5ef7ef4b400694dbcc1c570f5488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594842"
---
# <span data-ttu-id="af296-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="af296-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="af296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af296-102">SYNOPSIS</span></span>
<span data-ttu-id="af296-103">Geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="af296-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af296-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af296-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af296-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af296-105">DESCRIPTION</span></span>
<span data-ttu-id="af296-106">**Get-AzureRmRelayHybridConnection** cmdlet 'ı, geçiş ad alanında belirtilen HybridConnection için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="af296-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="af296-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af296-107">EXAMPLES</span></span>

### <span data-ttu-id="af296-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af296-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

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

<span data-ttu-id="af296-109">HybridConnection 'un açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="af296-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="af296-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af296-110">PARAMETERS</span></span>

### <span data-ttu-id="af296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af296-111">-DefaultProfile</span></span>
<span data-ttu-id="af296-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af296-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af296-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="af296-113">-Name</span></span>
<span data-ttu-id="af296-114">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="af296-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="af296-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="af296-115">-Namespace</span></span>
<span data-ttu-id="af296-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="af296-116">Namespace Name.</span></span>

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

### <span data-ttu-id="af296-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af296-117">-ResourceGroupName</span></span>
<span data-ttu-id="af296-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="af296-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="af296-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af296-119">CommonParameters</span></span>
<span data-ttu-id="af296-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af296-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="af296-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af296-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af296-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af296-122">INPUTS</span></span>

### <span data-ttu-id="af296-123">System. String</span><span class="sxs-lookup"><span data-stu-id="af296-123">System.String</span></span>


## <span data-ttu-id="af296-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af296-124">OUTPUTS</span></span>

### <span data-ttu-id="af296-125">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="af296-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="af296-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af296-126">NOTES</span></span>

## <span data-ttu-id="af296-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af296-127">RELATED LINKS</span></span>
