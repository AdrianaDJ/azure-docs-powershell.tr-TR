---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761697"
---
# <span data-ttu-id="1c0ca-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="1c0ca-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="1c0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0ca-103">Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="1c0ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c0ca-104">SYNTAX</span></span>

### <span data-ttu-id="1c0ca-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c0ca-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1c0ca-106">Al</span><span class="sxs-lookup"><span data-stu-id="1c0ca-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c0ca-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1c0ca-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1c0ca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c0ca-108">DESCRIPTION</span></span>
<span data-ttu-id="1c0ca-109">Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="1c0ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c0ca-110">EXAMPLES</span></span>

### <span data-ttu-id="1c0ca-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c0ca-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="1c0ca-112">Geçerli aboneliğin ve verilen kaynak grubu adının altındaki tüm dizin kiracıları listeler.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="1c0ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c0ca-113">PARAMETERS</span></span>

### <span data-ttu-id="1c0ca-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c0ca-114">-Name</span></span>
<span data-ttu-id="1c0ca-115">Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="1c0ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c0ca-117">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1c0ca-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1c0ca-118">-ResourceId</span></span>
<span data-ttu-id="1c0ca-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-119">The resource id.</span></span>

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

### <span data-ttu-id="1c0ca-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="1c0ca-120">-Skip</span></span>
<span data-ttu-id="1c0ca-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1c0ca-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="1c0ca-122">-Top</span></span>
<span data-ttu-id="1c0ca-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1c0ca-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1c0ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0ca-125">CommonParameters</span></span>
<span data-ttu-id="1c0ca-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0ca-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0ca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0ca-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c0ca-128">INPUTS</span></span>

## <span data-ttu-id="1c0ca-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c0ca-129">OUTPUTS</span></span>

### <span data-ttu-id="1c0ca-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="1c0ca-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="1c0ca-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c0ca-131">NOTES</span></span>

## <span data-ttu-id="1c0ca-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c0ca-132">RELATED LINKS</span></span>

