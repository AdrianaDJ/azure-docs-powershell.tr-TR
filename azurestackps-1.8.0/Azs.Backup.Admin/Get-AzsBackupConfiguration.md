---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934811"
---
# <span data-ttu-id="1841c-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1841c-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="1841c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1841c-102">SYNOPSIS</span></span>
<span data-ttu-id="1841c-103">Yedekleme yapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1841c-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1841c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1841c-104">SYNTAX</span></span>

### <span data-ttu-id="1841c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1841c-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1841c-106">Al</span><span class="sxs-lookup"><span data-stu-id="1841c-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1841c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1841c-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1841c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1841c-108">DESCRIPTION</span></span>
<span data-ttu-id="1841c-109">Yedekleme yapılandırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1841c-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="1841c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1841c-110">EXAMPLES</span></span>

### <span data-ttu-id="1841c-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1841c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="1841c-112">Azure yığın yedekleme yapılandırmasını edinin.</span><span class="sxs-lookup"><span data-stu-id="1841c-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="1841c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1841c-113">PARAMETERS</span></span>

### <span data-ttu-id="1841c-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="1841c-114">-Location</span></span>
<span data-ttu-id="1841c-115">Yedekleme konumu.</span><span class="sxs-lookup"><span data-stu-id="1841c-115">Backup location.</span></span>

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

### <span data-ttu-id="1841c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1841c-116">-ResourceGroupName</span></span>
<span data-ttu-id="1841c-117">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1841c-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="1841c-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1841c-118">-ResourceId</span></span>
<span data-ttu-id="1841c-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1841c-119">The resource id.</span></span>

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

### <span data-ttu-id="1841c-120">-Atla</span><span class="sxs-lookup"><span data-stu-id="1841c-120">-Skip</span></span>
<span data-ttu-id="1841c-121">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="1841c-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1841c-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="1841c-122">-Top</span></span>
<span data-ttu-id="1841c-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="1841c-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1841c-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1841c-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1841c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1841c-125">CommonParameters</span></span>
<span data-ttu-id="1841c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1841c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1841c-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1841c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1841c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1841c-128">INPUTS</span></span>

## <span data-ttu-id="1841c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1841c-129">OUTPUTS</span></span>

### <span data-ttu-id="1841c-130">Microsoft. AzureStack. Management. Backup. admin. modeller. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="1841c-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="1841c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1841c-131">NOTES</span></span>

## <span data-ttu-id="1841c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1841c-132">RELATED LINKS</span></span>
