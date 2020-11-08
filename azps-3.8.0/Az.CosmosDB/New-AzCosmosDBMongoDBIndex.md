---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103647"
---
# <span data-ttu-id="cb9dc-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="cb9dc-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="cb9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9dc-103">Yeni bir CosmosDB MongoDB dizini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="cb9dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb9dc-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9dc-106">**New-AzCosmosDBMongoDBIndex** , yeni bir Cosmosdb MongoDB dizini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="cb9dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9dc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb9dc-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="cb9dc-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb9dc-109">PARAMETERS</span></span>

### <span data-ttu-id="cb9dc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9dc-110">-DefaultProfile</span></span>
<span data-ttu-id="cb9dc-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9dc-112">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="cb9dc-112">-Key</span></span>
<span data-ttu-id="cb9dc-113">Anahtar değerler dizeler olarak dizi.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9dc-114">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="cb9dc-114">-TtlInSeconds</span></span>
<span data-ttu-id="cb9dc-115">Dizinin süre sonundan sonraki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9dc-116">-Benzersiz</span><span class="sxs-lookup"><span data-stu-id="cb9dc-116">-Unique</span></span>
<span data-ttu-id="cb9dc-117">Bool, dizinin benzersiz olup olmadığını belirtecek şekilde Boole.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9dc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9dc-118">CommonParameters</span></span>
<span data-ttu-id="cb9dc-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9dc-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb9dc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9dc-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb9dc-121">INPUTS</span></span>

### <span data-ttu-id="cb9dc-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb9dc-122">None</span></span>

## <span data-ttu-id="cb9dc-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb9dc-123">OUTPUTS</span></span>

### <span data-ttu-id="cb9dc-124">Microsoft. Azure. Commands. CosmosDB. modeller. Psmte Goındex</span><span class="sxs-lookup"><span data-stu-id="cb9dc-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="cb9dc-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb9dc-125">NOTES</span></span>

## <span data-ttu-id="cb9dc-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb9dc-126">RELATED LINKS</span></span>
