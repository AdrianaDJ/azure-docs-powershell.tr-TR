---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572133"
---
# <span data-ttu-id="fa496-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="fa496-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="fa496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa496-102">SYNOPSIS</span></span>
<span data-ttu-id="fa496-103">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="fa496-103">Get the list of update locations.</span></span>

## <span data-ttu-id="fa496-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa496-104">SYNTAX</span></span>

### <span data-ttu-id="fa496-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa496-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="fa496-106">Al</span><span class="sxs-lookup"><span data-stu-id="fa496-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="fa496-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fa496-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fa496-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa496-108">DESCRIPTION</span></span>
<span data-ttu-id="fa496-109">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="fa496-109">Get the list of update locations.</span></span> <span data-ttu-id="fa496-110">Verilen konumlar, Get-AzsUpdate kullanarak belirli bir konumda kullanılabilir güncelleştirmeleri almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa496-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="fa496-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa496-111">EXAMPLES</span></span>

### <span data-ttu-id="fa496-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa496-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="fa496-113">Güncelleştirme konumları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="fa496-113">Get the list of update locations.</span></span>

## <span data-ttu-id="fa496-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa496-114">PARAMETERS</span></span>

### <span data-ttu-id="fa496-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa496-115">-Name</span></span>
<span data-ttu-id="fa496-116">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="fa496-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa496-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa496-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa496-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fa496-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="fa496-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa496-119">-ResourceId</span></span>
<span data-ttu-id="fa496-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fa496-120">The resource id.</span></span>

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

### <span data-ttu-id="fa496-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa496-121">CommonParameters</span></span>
<span data-ttu-id="fa496-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa496-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa496-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa496-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa496-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa496-124">INPUTS</span></span>

## <span data-ttu-id="fa496-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa496-125">OUTPUTS</span></span>

### <span data-ttu-id="fa496-126">Microsoft. AzureStack. Management. Update. admin. modeller. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="fa496-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="fa496-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa496-127">NOTES</span></span>

## <span data-ttu-id="fa496-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa496-128">RELATED LINKS</span></span>

