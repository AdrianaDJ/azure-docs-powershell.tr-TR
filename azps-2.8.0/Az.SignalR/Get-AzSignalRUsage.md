---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 99cf5e96e859932863236eacc1ad83a0b73ceecf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933174"
---
# <span data-ttu-id="62a03-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="62a03-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="62a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a03-102">SYNOPSIS</span></span>
<span data-ttu-id="62a03-103">Aboneliğin kullanım kotasını alma.</span><span class="sxs-lookup"><span data-stu-id="62a03-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="62a03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62a03-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62a03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62a03-105">DESCRIPTION</span></span>
<span data-ttu-id="62a03-106">Aboneliğin kullanım kotasını alma.</span><span class="sxs-lookup"><span data-stu-id="62a03-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="62a03-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62a03-107">EXAMPLES</span></span>

### <span data-ttu-id="62a03-108">Konumu alarak kullanım kotasını alma</span><span class="sxs-lookup"><span data-stu-id="62a03-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="62a03-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62a03-109">PARAMETERS</span></span>

### <span data-ttu-id="62a03-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a03-110">-DefaultProfile</span></span>
<span data-ttu-id="62a03-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62a03-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a03-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="62a03-112">-Location</span></span>
<span data-ttu-id="62a03-113">SignalR hizmet konumu.</span><span class="sxs-lookup"><span data-stu-id="62a03-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="62a03-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a03-114">CommonParameters</span></span>
<span data-ttu-id="62a03-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62a03-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a03-116">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62a03-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a03-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62a03-117">INPUTS</span></span>

### <span data-ttu-id="62a03-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62a03-118">None</span></span>

## <span data-ttu-id="62a03-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62a03-119">OUTPUTS</span></span>

### <span data-ttu-id="62a03-120">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="62a03-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="62a03-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62a03-121">NOTES</span></span>

## <span data-ttu-id="62a03-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62a03-122">RELATED LINKS</span></span>
