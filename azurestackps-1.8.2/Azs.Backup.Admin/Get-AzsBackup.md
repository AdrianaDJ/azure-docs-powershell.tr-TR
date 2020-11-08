---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106602"
---
# <span data-ttu-id="7934c-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="7934c-101">Get-AzsBackup</span></span>

## <span data-ttu-id="7934c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7934c-102">SYNOPSIS</span></span>
<span data-ttu-id="7934c-103">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="7934c-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="7934c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7934c-104">SYNTAX</span></span>

### <span data-ttu-id="7934c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7934c-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="7934c-106">Al</span><span class="sxs-lookup"><span data-stu-id="7934c-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7934c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="7934c-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="7934c-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="7934c-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7934c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7934c-109">DESCRIPTION</span></span>
<span data-ttu-id="7934c-110">Ad temelinde bir konumdan yedekleme döndürür.</span><span class="sxs-lookup"><span data-stu-id="7934c-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="7934c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7934c-111">EXAMPLES</span></span>

### <span data-ttu-id="7934c-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7934c-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="7934c-113">Tüm Azure yığın yedeklemelerini hakkında bilgi alın.</span><span class="sxs-lookup"><span data-stu-id="7934c-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="7934c-114">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7934c-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="7934c-115">Belirtilen Azure yığın yedeklemesi için bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="7934c-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="7934c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7934c-116">PARAMETERS</span></span>

### <span data-ttu-id="7934c-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="7934c-117">-Location</span></span>
<span data-ttu-id="7934c-118">Konum yedeklendi.</span><span class="sxs-lookup"><span data-stu-id="7934c-118">Location backed up.</span></span>

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

### <span data-ttu-id="7934c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7934c-119">-Name</span></span>
<span data-ttu-id="7934c-120">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="7934c-120">Name of the backup.</span></span>

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

### <span data-ttu-id="7934c-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="7934c-121">-ParentResource</span></span>
<span data-ttu-id="7934c-122">Yedekleme konumu geçirilirse, bu yedekleme konumundaki tüm yedeklemelerin listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="7934c-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7934c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7934c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7934c-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7934c-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="7934c-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7934c-125">-ResourceId</span></span>
<span data-ttu-id="7934c-126">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7934c-126">The resource id.</span></span>

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

### <span data-ttu-id="7934c-127">-Atla</span><span class="sxs-lookup"><span data-stu-id="7934c-127">-Skip</span></span>
<span data-ttu-id="7934c-128">{{Dolguyu atla açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="7934c-128">{{Fill Skip Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7934c-129">-Üst</span><span class="sxs-lookup"><span data-stu-id="7934c-129">-Top</span></span>
<span data-ttu-id="7934c-130">{{Dolgu üst açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="7934c-130">{{Fill Top Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7934c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7934c-131">CommonParameters</span></span>
<span data-ttu-id="7934c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7934c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7934c-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7934c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7934c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7934c-134">INPUTS</span></span>

## <span data-ttu-id="7934c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7934c-135">OUTPUTS</span></span>

### <span data-ttu-id="7934c-136">Microsoft. AzureStack. Management. Backup. admin. modeller. Backup</span><span class="sxs-lookup"><span data-stu-id="7934c-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="7934c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7934c-137">NOTES</span></span>

## <span data-ttu-id="7934c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7934c-138">RELATED LINKS</span></span>

