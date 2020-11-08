---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277815"
---
# <span data-ttu-id="c4716-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="c4716-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="c4716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4716-102">SYNOPSIS</span></span>
<span data-ttu-id="c4716-103">HPC önbellek depolama hedefini edinin.</span><span class="sxs-lookup"><span data-stu-id="c4716-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="c4716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4716-104">SYNTAX</span></span>

### <span data-ttu-id="c4716-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4716-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4716-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c4716-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4716-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4716-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4716-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4716-108">DESCRIPTION</span></span>
<span data-ttu-id="c4716-109">**Get-AzHpcCacheStorageTarget** cmdlet 'i önbellekte bulunan depolama hedefini alır.</span><span class="sxs-lookup"><span data-stu-id="c4716-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="c4716-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4716-110">EXAMPLES</span></span>

### <span data-ttu-id="c4716-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4716-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="c4716-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4716-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="c4716-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4716-113">PARAMETERS</span></span>

### <span data-ttu-id="c4716-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c4716-114">-CacheId</span></span>
<span data-ttu-id="c4716-115">Önbelleğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c4716-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="c4716-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="c4716-116">-CacheName</span></span>
<span data-ttu-id="c4716-117">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="c4716-117">Name of cache.</span></span>

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

### <span data-ttu-id="c4716-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="c4716-118">-CacheObject</span></span>
<span data-ttu-id="c4716-119">Başlayacak önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c4716-119">The cache object to start.</span></span>

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

### <span data-ttu-id="c4716-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4716-120">-DefaultProfile</span></span>
<span data-ttu-id="c4716-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4716-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4716-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4716-122">-Name</span></span>
<span data-ttu-id="c4716-123">Depolama hedefinin adı.</span><span class="sxs-lookup"><span data-stu-id="c4716-123">Name of storage target.</span></span>

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

### <span data-ttu-id="c4716-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4716-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4716-125">Kaynak grubu önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="c4716-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="c4716-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4716-126">CommonParameters</span></span>
<span data-ttu-id="c4716-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4716-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4716-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c4716-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4716-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4716-129">INPUTS</span></span>

### <span data-ttu-id="c4716-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c4716-130">System.String</span></span>

## <span data-ttu-id="c4716-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4716-131">OUTPUTS</span></span>

### <span data-ttu-id="c4716-132">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="c4716-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="c4716-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4716-133">NOTES</span></span>

## <span data-ttu-id="c4716-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4716-134">RELATED LINKS</span></span>
