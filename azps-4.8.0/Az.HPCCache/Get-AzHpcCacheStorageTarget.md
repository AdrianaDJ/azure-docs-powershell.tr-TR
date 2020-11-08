---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109623"
---
# <span data-ttu-id="59eb3-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="59eb3-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="59eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="59eb3-103">HPC önbellek depolama hedefini edinin.</span><span class="sxs-lookup"><span data-stu-id="59eb3-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="59eb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59eb3-104">SYNTAX</span></span>

### <span data-ttu-id="59eb3-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59eb3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59eb3-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="59eb3-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59eb3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59eb3-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59eb3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59eb3-108">DESCRIPTION</span></span>
<span data-ttu-id="59eb3-109">**Get-AzHpcCacheStorageTarget** cmdlet 'i önbellekte bulunan depolama hedefini alır.</span><span class="sxs-lookup"><span data-stu-id="59eb3-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="59eb3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59eb3-110">EXAMPLES</span></span>

### <span data-ttu-id="59eb3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59eb3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="59eb3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="59eb3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="59eb3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59eb3-113">PARAMETERS</span></span>

### <span data-ttu-id="59eb3-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="59eb3-114">-CacheId</span></span>
<span data-ttu-id="59eb3-115">Önbelleğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="59eb3-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59eb3-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="59eb3-116">-CacheName</span></span>
<span data-ttu-id="59eb3-117">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="59eb3-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59eb3-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="59eb3-118">-CacheObject</span></span>
<span data-ttu-id="59eb3-119">Başlayacak önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="59eb3-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59eb3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59eb3-120">-DefaultProfile</span></span>
<span data-ttu-id="59eb3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59eb3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59eb3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="59eb3-122">-Name</span></span>
<span data-ttu-id="59eb3-123">Depolama hedefinin adı.</span><span class="sxs-lookup"><span data-stu-id="59eb3-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59eb3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59eb3-124">-ResourceGroupName</span></span>
<span data-ttu-id="59eb3-125">Kaynak grubu önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="59eb3-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59eb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eb3-126">CommonParameters</span></span>
<span data-ttu-id="59eb3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59eb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eb3-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59eb3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eb3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59eb3-129">INPUTS</span></span>

### <span data-ttu-id="59eb3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="59eb3-130">System.String</span></span>

## <span data-ttu-id="59eb3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59eb3-131">OUTPUTS</span></span>

### <span data-ttu-id="59eb3-132">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="59eb3-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="59eb3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59eb3-133">NOTES</span></span>

## <span data-ttu-id="59eb3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59eb3-134">RELATED LINKS</span></span>
