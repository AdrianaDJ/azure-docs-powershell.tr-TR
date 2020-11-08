---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277370"
---
# <span data-ttu-id="851ff-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="851ff-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="851ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851ff-102">SYNOPSIS</span></span>
<span data-ttu-id="851ff-103">Importexport için DriverList nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="851ff-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="851ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="851ff-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="851ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="851ff-105">DESCRIPTION</span></span>
<span data-ttu-id="851ff-106">Importexport için DriverList nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="851ff-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="851ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="851ff-107">EXAMPLES</span></span>

### <span data-ttu-id="851ff-108">Örnek 1: ımportexport işi için yeni bir sürücü listesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="851ff-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="851ff-109">Bu cmdlet 'ler ımportexport işi için yeni bir sürücü listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="851ff-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="851ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="851ff-110">PARAMETERS</span></span>

### <span data-ttu-id="851ff-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="851ff-111">-BitLockerKey</span></span>
<span data-ttu-id="851ff-112">Sürücüyü şifrelemek için kullanılan BitLocker anahtarı.</span><span class="sxs-lookup"><span data-stu-id="851ff-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="851ff-113">-BytesSucceeded</span></span>
<span data-ttu-id="851ff-114">Sürücü için başarıyla aktarılan baytlar.</span><span class="sxs-lookup"><span data-stu-id="851ff-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="851ff-115">-CopyStatus</span></span>
<span data-ttu-id="851ff-116">Veri aktarım süreci hakkında ayrıntılı durum.</span><span class="sxs-lookup"><span data-stu-id="851ff-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="851ff-117">Bu alan, sürücü aktarma durumunda olana kadar yanıtta döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="851ff-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="851ff-118">-DriveHeaderHash</span></span>
<span data-ttu-id="851ff-119">Sürücü üstbilgisi karma değeri.</span><span class="sxs-lookup"><span data-stu-id="851ff-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-120">-DriveID</span><span class="sxs-lookup"><span data-stu-id="851ff-120">-DriveId</span></span>
<span data-ttu-id="851ff-121">Sürücünün boşluk içermeyen donanım seri numarası.</span><span class="sxs-lookup"><span data-stu-id="851ff-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="851ff-122">-ErrorLogUri</span></span>
<span data-ttu-id="851ff-123">Veri aktarma işlemi için hata günlüğünü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="851ff-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="851ff-124">-ManifestFile</span></span>
<span data-ttu-id="851ff-125">Sürücüdeki bildirim dosyasının göreli yolu.</span><span class="sxs-lookup"><span data-stu-id="851ff-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="851ff-126">-ManifestHash</span></span>
<span data-ttu-id="851ff-127">Sürücüdeki bildirim dosyasının Base16 ile kodlanmış MD5 karması.</span><span class="sxs-lookup"><span data-stu-id="851ff-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="851ff-128">-ManifestUri</span></span>
<span data-ttu-id="851ff-129">Sürücü bildirim dosyasını içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="851ff-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="851ff-130">-PercentComplete</span></span>
<span data-ttu-id="851ff-131">Sürücü için tamamlanan yüzde.</span><span class="sxs-lookup"><span data-stu-id="851ff-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="851ff-132">-State</span></span>
<span data-ttu-id="851ff-133">Sürücünün geçerli durumu.</span><span class="sxs-lookup"><span data-stu-id="851ff-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="851ff-134">-VerboseLogUri</span></span>
<span data-ttu-id="851ff-135">Veri aktarma işlemi için ayrıntılı günlüğü içeren blob 'a işaret eden bir URI.</span><span class="sxs-lookup"><span data-stu-id="851ff-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851ff-136">CommonParameters</span></span>
<span data-ttu-id="851ff-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="851ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851ff-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="851ff-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851ff-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="851ff-139">INPUTS</span></span>

## <span data-ttu-id="851ff-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="851ff-140">OUTPUTS</span></span>

### <span data-ttu-id="851ff-141">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="851ff-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="851ff-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="851ff-142">NOTES</span></span>

<span data-ttu-id="851ff-143">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="851ff-143">ALIASES</span></span>

## <span data-ttu-id="851ff-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="851ff-144">RELATED LINKS</span></span>

