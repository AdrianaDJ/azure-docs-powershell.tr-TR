---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321533"
---
# <span data-ttu-id="ca5a7-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="ca5a7-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="ca5a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5a7-103">Yeni bir CosmosDB konum nesnesi (PSLocation) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="ca5a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca5a7-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca5a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5a7-106">Yeni bir CosmosDB konum nesnesi (PSLocation) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="ca5a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ca5a7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca5a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="ca5a7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca5a7-109">PARAMETERS</span></span>

### <span data-ttu-id="ca5a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5a7-110">-DefaultProfile</span></span>
<span data-ttu-id="ca5a7-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5a7-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="ca5a7-112">-FailoverPriority</span></span>
<span data-ttu-id="ca5a7-113">Konumun yük devretme önceliği.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="ca5a7-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ca5a7-114">-IsZoneRedundant</span></span>
<span data-ttu-id="ca5a7-115">Bu bölgenin, kullanılabilirlik bölgesi olup olmadığını belirtecek şekilde Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="ca5a7-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="ca5a7-116">-LocationName</span></span>
<span data-ttu-id="ca5a7-117">Dizede konumun adı.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="ca5a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5a7-118">CommonParameters</span></span>
<span data-ttu-id="ca5a7-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5a7-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca5a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5a7-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca5a7-121">INPUTS</span></span>

### <span data-ttu-id="ca5a7-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ca5a7-122">None</span></span>

## <span data-ttu-id="ca5a7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca5a7-123">OUTPUTS</span></span>

### <span data-ttu-id="ca5a7-124">Microsoft. Azure. Commands. CosmosDB. modeller. PSLocation</span><span class="sxs-lookup"><span data-stu-id="ca5a7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="ca5a7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca5a7-125">NOTES</span></span>

## <span data-ttu-id="ca5a7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca5a7-126">RELATED LINKS</span></span>
