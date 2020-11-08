---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098609"
---
# <span data-ttu-id="1f14e-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="1f14e-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="1f14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f14e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f14e-103">Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="1f14e-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="1f14e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f14e-104">SYNTAX</span></span>

### <span data-ttu-id="1f14e-105">Yol tabanlı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f14e-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="1f14e-106">Bilgisayar adı tabanlı</span><span class="sxs-lookup"><span data-stu-id="1f14e-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="1f14e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f14e-107">DESCRIPTION</span></span>
<span data-ttu-id="1f14e-108">**Invoke-AzStorageSyncCompatibilityCheck** cmdlet 'i, sisteminiz Ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler. Yerel veya uzak yol verildiğinde, sistem ve dosya ad boşluğunda bir dizi doğrulama gerçekleştirir ve bulduğu tüm uyumluluk sorunlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f14e-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="1f14e-109">Sistem denetimleri:</span><span class="sxs-lookup"><span data-stu-id="1f14e-109">System checks:</span></span>
- <span data-ttu-id="1f14e-110">İşletim sistemi Uyumluluk dosyası ad alanı denetimleri:</span><span class="sxs-lookup"><span data-stu-id="1f14e-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="1f14e-111">Desteklenmeyen karakterler</span><span class="sxs-lookup"><span data-stu-id="1f14e-111">Unsupported characters</span></span>
- <span data-ttu-id="1f14e-112">En büyük dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="1f14e-112">Maximum file size</span></span>
- <span data-ttu-id="1f14e-113">Maksimum yol uzunluğu</span><span class="sxs-lookup"><span data-stu-id="1f14e-113">Maximum path length</span></span>
- <span data-ttu-id="1f14e-114">Maksimum dosya uzunluğu</span><span class="sxs-lookup"><span data-stu-id="1f14e-114">Maximum file length</span></span>
- <span data-ttu-id="1f14e-115">En büyük veri kümesi boyutu</span><span class="sxs-lookup"><span data-stu-id="1f14e-115">Maximum dataset size</span></span>
- <span data-ttu-id="1f14e-116">En fazla Dizin derinliği</span><span class="sxs-lookup"><span data-stu-id="1f14e-116">Maximum directory depth</span></span>

## <span data-ttu-id="1f14e-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f14e-117">EXAMPLES</span></span>

### <span data-ttu-id="1f14e-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f14e-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="1f14e-119">Bu komut, sistemin ve C:\DATA'TEKI dosya ve klasörlerin uyumluluğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="1f14e-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="1f14e-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1f14e-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="1f14e-121">Bu komut C:\VERILERDEKI dosyaların ve klasörlerin uyumluluğunu denetler, ancak sistem uyumluluğu denetimi gerçekleştirmez.</span><span class="sxs-lookup"><span data-stu-id="1f14e-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="1f14e-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1f14e-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="1f14e-123">Bu komut, c: \ verilerdeki dosyaların ve klasörlerin uyumluluğunu denetler ve ardından sonuçları C:\resultsdizinine CSV dosyası olarak aktarır.</span><span class="sxs-lookup"><span data-stu-id="1f14e-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="1f14e-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f14e-124">PARAMETERS</span></span>

### <span data-ttu-id="1f14e-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="1f14e-125">-ComputerName</span></span>
<span data-ttu-id="1f14e-126">Bu bilgisayarı denetleme.</span><span class="sxs-lookup"><span data-stu-id="1f14e-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14e-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="1f14e-127">-Credential</span></span>
<span data-ttu-id="1f14e-128">Doğrulama için kimlik bilgileriniz.</span><span class="sxs-lookup"><span data-stu-id="1f14e-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14e-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="1f14e-129">-Path</span></span>
<span data-ttu-id="1f14e-130">Doğruladığımız paylaşımın UNC yolu.</span><span class="sxs-lookup"><span data-stu-id="1f14e-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14e-131">-Skipnamespacedenetimlerini</span><span class="sxs-lookup"><span data-stu-id="1f14e-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="1f14e-132">Dosya ad alanı doğrulamalarını atlamak için bu bayrağı ayarlayın ve yalnızca sistem doğrulamaları gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="1f14e-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14e-133">-Skipsystemdenetimleri</span><span class="sxs-lookup"><span data-stu-id="1f14e-133">-SkipSystemChecks</span></span>
<span data-ttu-id="1f14e-134">Sistem doğrulamalarını atlayıp yalnızca dosya ad alanı doğrulamaları gerçekleştirmek için bu bayrağı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1f14e-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f14e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f14e-135">CommonParameters</span></span>
<span data-ttu-id="1f14e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f14e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f14e-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f14e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f14e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f14e-138">INPUTS</span></span>

### <span data-ttu-id="1f14e-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f14e-139">None</span></span>

## <span data-ttu-id="1f14e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f14e-140">OUTPUTS</span></span>

### <span data-ttu-id="1f14e-141">Microsoft. Azure. Commands. Storagesehd. Evaluation. model. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="1f14e-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="1f14e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f14e-142">NOTES</span></span>
* <span data-ttu-id="1f14e-143">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, storageseşit</span><span class="sxs-lookup"><span data-stu-id="1f14e-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="1f14e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f14e-144">RELATED LINKS</span></span>