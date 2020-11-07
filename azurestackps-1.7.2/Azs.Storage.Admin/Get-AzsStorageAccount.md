---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934419"
---
# <span data-ttu-id="265d6-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="265d6-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="265d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="265d6-102">SYNOPSIS</span></span>
<span data-ttu-id="265d6-103">İstenen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="265d6-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="265d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="265d6-104">SYNTAX</span></span>

### <span data-ttu-id="265d6-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="265d6-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="265d6-106">Al</span><span class="sxs-lookup"><span data-stu-id="265d6-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="265d6-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="265d6-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="265d6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="265d6-108">DESCRIPTION</span></span>
<span data-ttu-id="265d6-109">İstenen depolama hesabını döndürür.</span><span class="sxs-lookup"><span data-stu-id="265d6-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="265d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="265d6-110">EXAMPLES</span></span>

### <span data-ttu-id="265d6-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="265d6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="265d6-112">Depolama hesaplarının bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="265d6-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="265d6-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="265d6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="265d6-114">Belirtilen depolama hesabının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="265d6-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="265d6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="265d6-115">PARAMETERS</span></span>

### <span data-ttu-id="265d6-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="265d6-116">-FarmName</span></span>
<span data-ttu-id="265d6-117">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="265d6-117">Farm Id.</span></span>

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

### <span data-ttu-id="265d6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="265d6-118">-Name</span></span>
<span data-ttu-id="265d6-119">Kiracıya görünmeyen iç depolama hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="265d6-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="265d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="265d6-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="265d6-121">Resource group name.</span></span>

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

### <span data-ttu-id="265d6-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="265d6-122">-ResourceId</span></span>
<span data-ttu-id="265d6-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="265d6-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="265d6-124">-Atla</span><span class="sxs-lookup"><span data-stu-id="265d6-124">-Skip</span></span>
<span data-ttu-id="265d6-125">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="265d6-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="265d6-126">-Özet</span><span class="sxs-lookup"><span data-stu-id="265d6-126">-Summary</span></span>
<span data-ttu-id="265d6-127">Yardım için anahtar veya ayrıntılı bilgi verilir.</span><span class="sxs-lookup"><span data-stu-id="265d6-127">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="265d6-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="265d6-128">-Top</span></span>
<span data-ttu-id="265d6-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="265d6-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="265d6-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="265d6-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="265d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265d6-131">CommonParameters</span></span>
<span data-ttu-id="265d6-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="265d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265d6-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="265d6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265d6-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="265d6-134">INPUTS</span></span>

## <span data-ttu-id="265d6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="265d6-135">OUTPUTS</span></span>

### <span data-ttu-id="265d6-136">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="265d6-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="265d6-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="265d6-137">NOTES</span></span>

## <span data-ttu-id="265d6-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="265d6-138">RELATED LINKS</span></span>

