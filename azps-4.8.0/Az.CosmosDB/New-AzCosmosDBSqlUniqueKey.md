---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274617"
---
# <span data-ttu-id="4e7ba-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="4e7ba-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="4e7ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7ba-103">Yeni bir CosmosDB SQL UniqueKey nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="4e7ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e7ba-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e7ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="4e7ba-106">**New-AzCosmosDBSqlUniqueKey** cmdlet 'i PSUniqueKey türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="4e7ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="4e7ba-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e7ba-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="4e7ba-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e7ba-109">PARAMETERS</span></span>

### <span data-ttu-id="4e7ba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7ba-110">-DefaultProfile</span></span>
<span data-ttu-id="4e7ba-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e7ba-112">-Yol</span><span class="sxs-lookup"><span data-stu-id="4e7ba-112">-Path</span></span>
<span data-ttu-id="4e7ba-113">Yol değerleri dizesi dizisi</span><span class="sxs-lookup"><span data-stu-id="4e7ba-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e7ba-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7ba-114">CommonParameters</span></span>
<span data-ttu-id="4e7ba-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7ba-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7ba-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e7ba-117">INPUTS</span></span>

### <span data-ttu-id="4e7ba-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e7ba-118">None</span></span>

## <span data-ttu-id="4e7ba-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e7ba-119">OUTPUTS</span></span>

### <span data-ttu-id="4e7ba-120">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="4e7ba-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="4e7ba-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e7ba-121">NOTES</span></span>

## <span data-ttu-id="4e7ba-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e7ba-122">RELATED LINKS</span></span>
