---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 364b22c834ae7476e64f972b289e20d3caa5ba80
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934223"
---
# <span data-ttu-id="fc076-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="fc076-101">Get-AzsBackup</span></span>

## <span data-ttu-id="fc076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc076-102">SYNOPSIS</span></span>
<span data-ttu-id="fc076-103">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc076-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="fc076-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc076-104">SYNTAX</span></span>

### <span data-ttu-id="fc076-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc076-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc076-106">Al</span><span class="sxs-lookup"><span data-stu-id="fc076-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="fc076-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fc076-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="fc076-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="fc076-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fc076-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc076-109">DESCRIPTION</span></span>
<span data-ttu-id="fc076-110">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc076-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="fc076-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc076-111">EXAMPLES</span></span>

### <span data-ttu-id="fc076-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="fc076-112">EXAMPLE 1</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="fc076-113">Tüm Azure yığın yedekleri hakkında bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="fc076-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="fc076-114">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="fc076-114">EXAMPLE 2</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="fc076-115">Belirtilen Azure Stack Backup için bilgi alın.</span><span class="sxs-lookup"><span data-stu-id="fc076-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="fc076-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc076-116">PARAMETERS</span></span>

### <span data-ttu-id="fc076-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="fc076-117">-Location</span></span>
<span data-ttu-id="fc076-118">Konum yedeklendi.</span><span class="sxs-lookup"><span data-stu-id="fc076-118">Location backed up.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc076-119">-Name</span></span>
<span data-ttu-id="fc076-120">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="fc076-120">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="fc076-121">-ParentResource</span></span>
<span data-ttu-id="fc076-122">Yedekleme konumu geçirilirse, bu yedekleme konumundaki tüm yedeklemelerin listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="fc076-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: ParentResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc076-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc076-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc076-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc076-125">-ResourceId</span></span>
<span data-ttu-id="fc076-126">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fc076-126">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="fc076-127">-Top</span></span>
<span data-ttu-id="fc076-128">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="fc076-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fc076-129">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="fc076-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-130">-Atla</span><span class="sxs-lookup"><span data-stu-id="fc076-130">-Skip</span></span>
<span data-ttu-id="fc076-131">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="fc076-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc076-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc076-132">CommonParameters</span></span>
<span data-ttu-id="fc076-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc076-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc076-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc076-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc076-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc076-135">INPUTS</span></span>

## <span data-ttu-id="fc076-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc076-136">OUTPUTS</span></span>

### <span data-ttu-id="fc076-137">Microsoft. AzureStack. Management. Backup. admin. modeller. Backup</span><span class="sxs-lookup"><span data-stu-id="fc076-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="fc076-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc076-138">NOTES</span></span>

## <span data-ttu-id="fc076-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc076-139">RELATED LINKS</span></span>
