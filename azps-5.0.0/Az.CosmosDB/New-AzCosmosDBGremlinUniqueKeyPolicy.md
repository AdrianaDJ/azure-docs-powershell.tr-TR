---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321541"
---
# <span data-ttu-id="588b3-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="588b3-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="588b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="588b3-102">SYNOPSIS</span></span>
<span data-ttu-id="588b3-103">Yeni bir CosmosDB UniqueKeyPolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="588b3-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="588b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="588b3-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="588b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="588b3-105">DESCRIPTION</span></span>
<span data-ttu-id="588b3-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet 'i PSUniqueKeyPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="588b3-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="588b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="588b3-107">EXAMPLES</span></span>

### <span data-ttu-id="588b3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="588b3-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="588b3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="588b3-109">PARAMETERS</span></span>

### <span data-ttu-id="588b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588b3-110">-DefaultProfile</span></span>
<span data-ttu-id="588b3-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="588b3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588b3-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="588b3-112">-UniqueKey</span></span>
<span data-ttu-id="588b3-113">PSUniqueKey türünde nesneler dizisi.</span><span class="sxs-lookup"><span data-stu-id="588b3-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588b3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588b3-114">CommonParameters</span></span>
<span data-ttu-id="588b3-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="588b3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588b3-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="588b3-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588b3-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="588b3-117">INPUTS</span></span>

### <span data-ttu-id="588b3-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="588b3-118">None</span></span>

## <span data-ttu-id="588b3-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="588b3-119">OUTPUTS</span></span>

### <span data-ttu-id="588b3-120">Microsoft. Azure. Commands. CosmosDB. modeller. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="588b3-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="588b3-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="588b3-121">NOTES</span></span>

## <span data-ttu-id="588b3-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="588b3-122">RELATED LINKS</span></span>
