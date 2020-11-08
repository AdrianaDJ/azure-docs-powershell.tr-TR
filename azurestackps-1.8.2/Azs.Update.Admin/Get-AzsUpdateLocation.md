---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106935"
---
# <span data-ttu-id="4685b-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="4685b-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="4685b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4685b-102">SYNOPSIS</span></span>
<span data-ttu-id="4685b-103">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="4685b-103">Get the list of update locations.</span></span>

## <span data-ttu-id="4685b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4685b-104">SYNTAX</span></span>

### <span data-ttu-id="4685b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4685b-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4685b-106">Al</span><span class="sxs-lookup"><span data-stu-id="4685b-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4685b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4685b-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4685b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4685b-108">DESCRIPTION</span></span>
<span data-ttu-id="4685b-109">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="4685b-109">Get the list of update locations.</span></span> <span data-ttu-id="4685b-110">Verilen konumlar, Get-AzsUpdate kullanarak belirli bir konumda kullanılabilir güncelleştirmeleri almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4685b-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="4685b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4685b-111">EXAMPLES</span></span>

### <span data-ttu-id="4685b-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="4685b-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="4685b-113">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="4685b-113">Get the list of update locations.</span></span>

## <span data-ttu-id="4685b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4685b-114">PARAMETERS</span></span>

### <span data-ttu-id="4685b-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="4685b-115">-Location</span></span>
<span data-ttu-id="4685b-116">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="4685b-116">Name of the Location.</span></span>

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

### <span data-ttu-id="4685b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4685b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4685b-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4685b-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4685b-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4685b-119">-ResourceId</span></span>
<span data-ttu-id="4685b-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4685b-120">The resource id.</span></span>

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

### <span data-ttu-id="4685b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4685b-121">CommonParameters</span></span>
<span data-ttu-id="4685b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4685b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4685b-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4685b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4685b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4685b-124">INPUTS</span></span>

## <span data-ttu-id="4685b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4685b-125">OUTPUTS</span></span>

### <span data-ttu-id="4685b-126">Microsoft. AzureStack. Management. Update. admin. modeller. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="4685b-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="4685b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4685b-127">NOTES</span></span>

## <span data-ttu-id="4685b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4685b-128">RELATED LINKS</span></span>
