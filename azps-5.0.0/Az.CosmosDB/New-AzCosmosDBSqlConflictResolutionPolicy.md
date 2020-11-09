---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321517"
---
# <span data-ttu-id="1fb3e-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb3e-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="1fb3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb3e-103">PSSqlConflictResolutionPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="1fb3e-104">Set-AzCosmosDBSqlContainer için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="1fb3e-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fb3e-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb3e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fb3e-106">DESCRIPTION</span></span>
<span data-ttu-id="1fb3e-107">SQL API 'ın ConflictResolutionPolicy öğesine karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="1fb3e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fb3e-108">EXAMPLES</span></span>

### <span data-ttu-id="1fb3e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1fb3e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="1fb3e-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="1fb3e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="1fb3e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fb3e-111">PARAMETERS</span></span>

### <span data-ttu-id="1fb3e-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="1fb3e-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="1fb3e-113">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1fb3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb3e-114">-DefaultProfile</span></span>
<span data-ttu-id="1fb3e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb3e-116">-Yol</span><span class="sxs-lookup"><span data-stu-id="1fb3e-116">-Path</span></span>
<span data-ttu-id="1fb3e-117">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1fb3e-118">-Tür</span><span class="sxs-lookup"><span data-stu-id="1fb3e-118">-Type</span></span>
<span data-ttu-id="1fb3e-119">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1fb3e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb3e-120">CommonParameters</span></span>
<span data-ttu-id="1fb3e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb3e-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb3e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fb3e-123">INPUTS</span></span>

### <span data-ttu-id="1fb3e-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1fb3e-124">None</span></span>

## <span data-ttu-id="1fb3e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fb3e-125">OUTPUTS</span></span>

### <span data-ttu-id="1fb3e-126">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb3e-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="1fb3e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fb3e-127">NOTES</span></span>

## <span data-ttu-id="1fb3e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fb3e-128">RELATED LINKS</span></span>
