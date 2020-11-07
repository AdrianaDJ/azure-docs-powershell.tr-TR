---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934964"
---
# <span data-ttu-id="a5127-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5127-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="a5127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5127-102">SYNOPSIS</span></span>
<span data-ttu-id="a5127-103">Yedekleme yapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5127-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="a5127-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5127-104">SYNTAX</span></span>

### <span data-ttu-id="a5127-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5127-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a5127-106">Al</span><span class="sxs-lookup"><span data-stu-id="a5127-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5127-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a5127-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a5127-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5127-108">DESCRIPTION</span></span>
<span data-ttu-id="a5127-109">Yedekleme yapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5127-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="a5127-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5127-110">EXAMPLES</span></span>

### <span data-ttu-id="a5127-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5127-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="a5127-112">Azure yığın yedekleme yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="a5127-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="a5127-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5127-113">PARAMETERS</span></span>

### <span data-ttu-id="a5127-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="a5127-114">-Location</span></span>
<span data-ttu-id="a5127-115">Yedekleme konumu.</span><span class="sxs-lookup"><span data-stu-id="a5127-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5127-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5127-116">-ResourceGroupName</span></span>
<span data-ttu-id="a5127-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5127-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="a5127-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5127-118">-ResourceId</span></span>
<span data-ttu-id="a5127-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a5127-119">The resource id.</span></span>

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

### <span data-ttu-id="a5127-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="a5127-120">-Skip</span></span>
<span data-ttu-id="a5127-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="a5127-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a5127-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="a5127-122">-Top</span></span>
<span data-ttu-id="a5127-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="a5127-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a5127-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a5127-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a5127-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5127-125">CommonParameters</span></span>
<span data-ttu-id="a5127-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5127-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5127-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5127-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5127-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5127-128">INPUTS</span></span>

## <span data-ttu-id="a5127-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5127-129">OUTPUTS</span></span>

### <span data-ttu-id="a5127-130">Microsoft. AzureStack. Management. Backup. admin. modeller. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="a5127-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="a5127-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5127-131">NOTES</span></span>

## <span data-ttu-id="a5127-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5127-132">RELATED LINKS</span></span>

