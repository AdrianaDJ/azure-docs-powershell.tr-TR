---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934561"
---
# <span data-ttu-id="03a9b-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="03a9b-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="03a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="03a9b-103">Güncelleştirme çalıştırmaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="03a9b-103">Get the list of update runs.</span></span>

## <span data-ttu-id="03a9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03a9b-104">SYNTAX</span></span>

### <span data-ttu-id="03a9b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03a9b-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="03a9b-106">Al</span><span class="sxs-lookup"><span data-stu-id="03a9b-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="03a9b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="03a9b-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="03a9b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03a9b-108">DESCRIPTION</span></span>
<span data-ttu-id="03a9b-109">Güncelleştirme çalıştırmaları listesini alın.</span><span class="sxs-lookup"><span data-stu-id="03a9b-109">Get the list of update runs.</span></span> <span data-ttu-id="03a9b-110">Geri döndürülen Updaterobjects örneklerinin örnekleri, uygun olduğunda yeniden başlatma-AzsUpdateRun ile kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="03a9b-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="03a9b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03a9b-111">EXAMPLES</span></span>

### <span data-ttu-id="03a9b-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="03a9b-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="03a9b-113">Belirli bir güncelleştirmeyi uygulamaya yönelik tüm girişimlerin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="03a9b-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="03a9b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03a9b-114">PARAMETERS</span></span>

### <span data-ttu-id="03a9b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="03a9b-115">-Name</span></span>
<span data-ttu-id="03a9b-116">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="03a9b-116">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a9b-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="03a9b-117">-UpdateName</span></span>
<span data-ttu-id="03a9b-118">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="03a9b-118">Name of the update.</span></span>

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

### <span data-ttu-id="03a9b-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="03a9b-119">-Location</span></span>
<span data-ttu-id="03a9b-120">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="03a9b-120">The name of the update location.</span></span>

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

### <span data-ttu-id="03a9b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a9b-121">-ResourceGroupName</span></span>
<span data-ttu-id="03a9b-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="03a9b-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="03a9b-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="03a9b-123">-ResourceId</span></span>
<span data-ttu-id="03a9b-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="03a9b-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a9b-125">-Atla</span><span class="sxs-lookup"><span data-stu-id="03a9b-125">-Skip</span></span>
<span data-ttu-id="03a9b-126">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="03a9b-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a9b-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="03a9b-127">-Top</span></span>
<span data-ttu-id="03a9b-128">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="03a9b-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="03a9b-129">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="03a9b-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a9b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a9b-130">CommonParameters</span></span>
<span data-ttu-id="03a9b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03a9b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a9b-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a9b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a9b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03a9b-133">INPUTS</span></span>

## <span data-ttu-id="03a9b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03a9b-134">OUTPUTS</span></span>

### <span data-ttu-id="03a9b-135">Microsoft. AzureStack. Management. Update. admin. modeller. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="03a9b-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="03a9b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03a9b-136">NOTES</span></span>

## <span data-ttu-id="03a9b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03a9b-137">RELATED LINKS</span></span>
