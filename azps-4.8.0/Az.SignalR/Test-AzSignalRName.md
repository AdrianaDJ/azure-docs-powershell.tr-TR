---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266327"
---
# <span data-ttu-id="9378b-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="9378b-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="9378b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9378b-102">SYNOPSIS</span></span>
<span data-ttu-id="9378b-103">Bir adın kullanılabilirliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9378b-103">Check the availability of a name.</span></span> <span data-ttu-id="9378b-104">Diğer ad: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="9378b-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="9378b-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9378b-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9378b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9378b-106">DESCRIPTION</span></span>
<span data-ttu-id="9378b-107">Bir adın kullanılabilirliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9378b-107">Check the availability of a name.</span></span> <span data-ttu-id="9378b-108">Diğer ad: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="9378b-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="9378b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9378b-109">EXAMPLES</span></span>

### <span data-ttu-id="9378b-110">Var olan bir adı denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9378b-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="9378b-111">Yok adını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9378b-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="9378b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9378b-112">PARAMETERS</span></span>

### <span data-ttu-id="9378b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9378b-113">-DefaultProfile</span></span>
<span data-ttu-id="9378b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9378b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9378b-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="9378b-115">-Location</span></span>
<span data-ttu-id="9378b-116">SignalR hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="9378b-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9378b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9378b-117">-Name</span></span>
<span data-ttu-id="9378b-118">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="9378b-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9378b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9378b-119">CommonParameters</span></span>
<span data-ttu-id="9378b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9378b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9378b-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9378b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9378b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9378b-122">INPUTS</span></span>

### <span data-ttu-id="9378b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9378b-123">System.String</span></span>

## <span data-ttu-id="9378b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9378b-124">OUTPUTS</span></span>

### <span data-ttu-id="9378b-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9378b-125">System.Boolean</span></span>

## <span data-ttu-id="9378b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9378b-126">NOTES</span></span>

## <span data-ttu-id="9378b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9378b-127">RELATED LINKS</span></span>
