---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935025"
---
# <span data-ttu-id="21e33-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="21e33-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="21e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21e33-102">SYNOPSIS</span></span>
<span data-ttu-id="21e33-103">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="21e33-103">Get the list of update locations.</span></span>

## <span data-ttu-id="21e33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21e33-104">SYNTAX</span></span>

### <span data-ttu-id="21e33-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21e33-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="21e33-106">Al</span><span class="sxs-lookup"><span data-stu-id="21e33-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="21e33-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="21e33-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="21e33-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="21e33-108">DESCRIPTION</span></span>
<span data-ttu-id="21e33-109">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="21e33-109">Get the list of update locations.</span></span> <span data-ttu-id="21e33-110">Verilen konumlar, Get-AzsUpdate kullanarak belirli bir konumda kullanılabilir güncelleştirmeleri almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="21e33-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="21e33-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21e33-111">EXAMPLES</span></span>

### <span data-ttu-id="21e33-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="21e33-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="21e33-113">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="21e33-113">Get the list of update locations.</span></span>

## <span data-ttu-id="21e33-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21e33-114">PARAMETERS</span></span>

### <span data-ttu-id="21e33-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="21e33-115">-Location</span></span>
<span data-ttu-id="21e33-116">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="21e33-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e33-117">-ResourceGroupName</span></span>
<span data-ttu-id="21e33-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="21e33-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="21e33-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="21e33-119">-ResourceId</span></span>
<span data-ttu-id="21e33-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="21e33-120">The resource id.</span></span>

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

### <span data-ttu-id="21e33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e33-121">CommonParameters</span></span>
<span data-ttu-id="21e33-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21e33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e33-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e33-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e33-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21e33-124">INPUTS</span></span>

## <span data-ttu-id="21e33-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21e33-125">OUTPUTS</span></span>

### <span data-ttu-id="21e33-126">Microsoft. AzureStack. Management. Update. admin. modeller. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="21e33-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="21e33-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21e33-127">NOTES</span></span>

## <span data-ttu-id="21e33-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21e33-128">RELATED LINKS</span></span>