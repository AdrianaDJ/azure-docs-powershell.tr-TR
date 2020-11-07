---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934006"
---
# <span data-ttu-id="98f7f-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="98f7f-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="98f7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="98f7f-103">Depolama paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="98f7f-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="98f7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98f7f-104">SYNTAX</span></span>

### <span data-ttu-id="98f7f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98f7f-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="98f7f-106">Al</span><span class="sxs-lookup"><span data-stu-id="98f7f-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="98f7f-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="98f7f-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="98f7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="98f7f-108">DESCRIPTION</span></span>
<span data-ttu-id="98f7f-109">Depolama paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="98f7f-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="98f7f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98f7f-110">EXAMPLES</span></span>

### <span data-ttu-id="98f7f-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98f7f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="98f7f-112">Depolama paylaşımlarının listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="98f7f-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="98f7f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98f7f-113">PARAMETERS</span></span>

### <span data-ttu-id="98f7f-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="98f7f-114">-FarmName</span></span>
<span data-ttu-id="98f7f-115">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="98f7f-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f7f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="98f7f-116">-Name</span></span>
<span data-ttu-id="98f7f-117">Paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="98f7f-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f7f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f7f-118">-ResourceGroupName</span></span>
<span data-ttu-id="98f7f-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="98f7f-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f7f-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="98f7f-120">-ResourceId</span></span>
<span data-ttu-id="98f7f-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="98f7f-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f7f-122">CommonParameters</span></span>
<span data-ttu-id="98f7f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98f7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f7f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f7f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f7f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98f7f-125">INPUTS</span></span>

## <span data-ttu-id="98f7f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98f7f-126">OUTPUTS</span></span>

### <span data-ttu-id="98f7f-127">Microsoft. AzureStack. Management. Storage. admin. modeller. Share</span><span class="sxs-lookup"><span data-stu-id="98f7f-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="98f7f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98f7f-128">NOTES</span></span>

## <span data-ttu-id="98f7f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98f7f-129">RELATED LINKS</span></span>

