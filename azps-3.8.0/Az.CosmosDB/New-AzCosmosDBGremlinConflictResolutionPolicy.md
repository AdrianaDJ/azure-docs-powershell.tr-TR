---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097564"
---
# <span data-ttu-id="e4bac-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4bac-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="e4bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bac-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bac-103">PSConflictResolutionPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e4bac-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="e4bac-104">Set-AzCosmosDBGremlinGraph için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="e4bac-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="e4bac-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4bac-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4bac-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4bac-106">DESCRIPTION</span></span>
<span data-ttu-id="e4bac-107">Gremlın API 'sinin ConflictResolutionPolicy öğesine karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="e4bac-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="e4bac-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4bac-108">EXAMPLES</span></span>

### <span data-ttu-id="e4bac-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4bac-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="e4bac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4bac-110">PARAMETERS</span></span>

### <span data-ttu-id="e4bac-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="e4bac-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="e4bac-112">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="e4bac-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bac-113">-DefaultProfile</span></span>
<span data-ttu-id="e4bac-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4bac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bac-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="e4bac-115">-Path</span></span>
<span data-ttu-id="e4bac-116">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="e4bac-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bac-117">-Tür</span><span class="sxs-lookup"><span data-stu-id="e4bac-117">-Type</span></span>
<span data-ttu-id="e4bac-118">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="e4bac-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4bac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bac-119">CommonParameters</span></span>
<span data-ttu-id="e4bac-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4bac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bac-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e4bac-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bac-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4bac-122">INPUTS</span></span>

### <span data-ttu-id="e4bac-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e4bac-123">None</span></span>

## <span data-ttu-id="e4bac-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4bac-124">OUTPUTS</span></span>

### <span data-ttu-id="e4bac-125">Microsoft. Azure. Commands. CosmosDB. modeller. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4bac-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="e4bac-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4bac-126">NOTES</span></span>

## <span data-ttu-id="e4bac-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4bac-127">RELATED LINKS</span></span>
