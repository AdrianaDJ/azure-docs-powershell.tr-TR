---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: 6c0fb28010aff759c406ddd04db281dc05ce1f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937545"
---
# <span data-ttu-id="0b612-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b612-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="0b612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b612-102">SYNOPSIS</span></span>
<span data-ttu-id="0b612-103">Verilen CosmosDB hesabı için {"ConnectionKeys", "PrimaryReadOnly" veya "Keys"} tuşlarını alın.</span><span class="sxs-lookup"><span data-stu-id="0b612-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="0b612-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b612-104">SYNTAX</span></span>

### <span data-ttu-id="0b612-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b612-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b612-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0b612-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b612-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b612-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b612-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b612-108">DESCRIPTION</span></span>
<span data-ttu-id="0b612-109">Bağlantı anahtarları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="0b612-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="0b612-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b612-110">EXAMPLES</span></span>

### <span data-ttu-id="0b612-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b612-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="0b612-112">CosmosDB hesabı anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0b612-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="0b612-113">Anahtar türü: ConnectionString, anahtarlar ve ReadOnlyKeys değerleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="0b612-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="0b612-114">Anahtarlar varsayılan.</span><span class="sxs-lookup"><span data-stu-id="0b612-114">Default is Keys.</span></span>

## <span data-ttu-id="0b612-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b612-115">PARAMETERS</span></span>

### <span data-ttu-id="0b612-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b612-116">-DefaultProfile</span></span>
<span data-ttu-id="0b612-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b612-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b612-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b612-118">-InputObject</span></span>
<span data-ttu-id="0b612-119">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="0b612-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b612-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b612-120">-Name</span></span>
<span data-ttu-id="0b612-121">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="0b612-121">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b612-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b612-122">-ResourceGroupName</span></span>
<span data-ttu-id="0b612-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b612-123">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b612-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b612-124">-ResourceId</span></span>
<span data-ttu-id="0b612-125">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0b612-125">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b612-126">-Tür</span><span class="sxs-lookup"><span data-stu-id="0b612-126">-Type</span></span>
<span data-ttu-id="0b612-127">Değer: {ConnectionStrings, anahtarlar, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="0b612-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="0b612-128">Anahtarlar varsayılan.</span><span class="sxs-lookup"><span data-stu-id="0b612-128">Default is Keys.</span></span>

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

### <span data-ttu-id="0b612-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b612-129">CommonParameters</span></span>
<span data-ttu-id="0b612-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b612-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b612-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b612-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b612-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b612-132">INPUTS</span></span>

### <span data-ttu-id="0b612-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b612-133">None</span></span>

## <span data-ttu-id="0b612-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b612-134">OUTPUTS</span></span>

### <span data-ttu-id="0b612-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDAtabaseaccountlistconnectionstring</span><span class="sxs-lookup"><span data-stu-id="0b612-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="0b612-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="0b612-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="0b612-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="0b612-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="0b612-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b612-138">NOTES</span></span>

## <span data-ttu-id="0b612-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b612-139">RELATED LINKS</span></span>
