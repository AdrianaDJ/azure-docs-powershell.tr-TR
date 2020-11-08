---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277818"
---
# <span data-ttu-id="e4756-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e4756-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="e4756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4756-102">SYNOPSIS</span></span>
<span data-ttu-id="e4756-103">Önbelleği alır.</span><span class="sxs-lookup"><span data-stu-id="e4756-103">Gets a cache(s).</span></span>

## <span data-ttu-id="e4756-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4756-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4756-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4756-105">DESCRIPTION</span></span>
<span data-ttu-id="e4756-106">**Get-AzHpcCache** cmdlet 'i, belirli bir kaynak grubundaki veya abonelik kapsamlı önbelleklerin tek bir önbelleğini, önbelleklerini veya aboneliğini alır.</span><span class="sxs-lookup"><span data-stu-id="e4756-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="e4756-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4756-107">EXAMPLES</span></span>

### <span data-ttu-id="e4756-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4756-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="e4756-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e4756-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="e4756-110">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e4756-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="e4756-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4756-111">PARAMETERS</span></span>

### <span data-ttu-id="e4756-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4756-112">-DefaultProfile</span></span>
<span data-ttu-id="e4756-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4756-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4756-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4756-114">-Name</span></span>
<span data-ttu-id="e4756-115">Belirli bir önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="e4756-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4756-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4756-116">-ResourceGroupName</span></span>
<span data-ttu-id="e4756-117">Önbelleğini listelemek istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e4756-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4756-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4756-118">CommonParameters</span></span>
<span data-ttu-id="e4756-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4756-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4756-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e4756-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4756-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4756-121">INPUTS</span></span>

### <span data-ttu-id="e4756-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e4756-122">System.String</span></span>

## <span data-ttu-id="e4756-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4756-123">OUTPUTS</span></span>

### <span data-ttu-id="e4756-124">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="e4756-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="e4756-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4756-125">NOTES</span></span>

## <span data-ttu-id="e4756-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4756-126">RELATED LINKS</span></span>
