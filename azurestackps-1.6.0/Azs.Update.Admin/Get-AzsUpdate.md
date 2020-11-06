---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572213"
---
# <span data-ttu-id="3f567-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="3f567-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="3f567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f567-102">SYNOPSIS</span></span>
<span data-ttu-id="3f567-103">Kullanılabilir güncelleştirmelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="3f567-103">Get the list of available updates.</span></span>

## <span data-ttu-id="3f567-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f567-104">SYNTAX</span></span>

### <span data-ttu-id="3f567-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f567-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f567-106">Al</span><span class="sxs-lookup"><span data-stu-id="3f567-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f567-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3f567-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3f567-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f567-108">DESCRIPTION</span></span>
<span data-ttu-id="3f567-109">Kullanılabilir güncelleştirmelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="3f567-109">Get the list of available updates.</span></span> <span data-ttu-id="3f567-110">Bu modülden döndürülen güncelleştirmeler, uygulanabilirse, ' Install-AzsUpdate ' ile geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="3f567-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="3f567-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f567-111">EXAMPLES</span></span>

### <span data-ttu-id="3f567-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f567-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="3f567-113">Kullanılabilir güncelleştirmelerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="3f567-113">Get the list of available updates.</span></span>

### <span data-ttu-id="3f567-114">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3f567-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="3f567-115">Belirli bir güncelleştirmeyi edinin.</span><span class="sxs-lookup"><span data-stu-id="3f567-115">Get the specific update.</span></span>

## <span data-ttu-id="3f567-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f567-116">PARAMETERS</span></span>

### <span data-ttu-id="3f567-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="3f567-117">-Location</span></span>
<span data-ttu-id="3f567-118">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="3f567-118">The name of the update location.</span></span>

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

### <span data-ttu-id="3f567-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f567-119">-Name</span></span>
<span data-ttu-id="3f567-120">Güncelleştirmenin adı.</span><span class="sxs-lookup"><span data-stu-id="3f567-120">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f567-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f567-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f567-122">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3f567-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3f567-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3f567-123">-ResourceId</span></span>
<span data-ttu-id="3f567-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3f567-124">The resource id.</span></span>

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

### <span data-ttu-id="3f567-125">-Atla</span><span class="sxs-lookup"><span data-stu-id="3f567-125">-Skip</span></span>
<span data-ttu-id="3f567-126">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="3f567-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3f567-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="3f567-127">-Top</span></span>
<span data-ttu-id="3f567-128">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="3f567-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3f567-129">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3f567-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3f567-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f567-130">CommonParameters</span></span>
<span data-ttu-id="3f567-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f567-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f567-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f567-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f567-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f567-133">INPUTS</span></span>

## <span data-ttu-id="3f567-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f567-134">OUTPUTS</span></span>

### <span data-ttu-id="3f567-135">Microsoft. AzureStack. Management. Update. admin. modeller. Update</span><span class="sxs-lookup"><span data-stu-id="3f567-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="3f567-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f567-136">NOTES</span></span>

## <span data-ttu-id="3f567-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f567-137">RELATED LINKS</span></span>

