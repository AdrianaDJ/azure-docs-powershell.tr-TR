---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591263"
---
# <span data-ttu-id="cd892-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="cd892-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="cd892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd892-102">SYNOPSIS</span></span>
<span data-ttu-id="cd892-103">Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="cd892-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd892-104">SYNTAX</span></span>

### <span data-ttu-id="cd892-105">Yol tabanlı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd892-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="cd892-106">Bilgisayar adı tabanlı</span><span class="sxs-lookup"><span data-stu-id="cd892-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="cd892-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd892-107">DESCRIPTION</span></span>
<span data-ttu-id="cd892-108">**Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet 'i, sisteminiz Ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler. Yerel veya uzak yol verildiğinde, sistem ve dosya ad boşluğunda bir dizi doğrulama gerçekleştirir ve bulduğu tüm uyumluluk sorunlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cd892-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="cd892-109">Sistem denetimleri:</span><span class="sxs-lookup"><span data-stu-id="cd892-109">System checks:</span></span>
- <span data-ttu-id="cd892-110">İşletim sistemi Uyumluluk dosyası ad alanı denetimleri:</span><span class="sxs-lookup"><span data-stu-id="cd892-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="cd892-111">Desteklenmeyen karakterler</span><span class="sxs-lookup"><span data-stu-id="cd892-111">Unsupported characters</span></span>
- <span data-ttu-id="cd892-112">En büyük dosya boyutu</span><span class="sxs-lookup"><span data-stu-id="cd892-112">Maximum file size</span></span>
- <span data-ttu-id="cd892-113">Maksimum yol uzunluğu</span><span class="sxs-lookup"><span data-stu-id="cd892-113">Maximum path length</span></span>
- <span data-ttu-id="cd892-114">Maksimum dosya uzunluğu</span><span class="sxs-lookup"><span data-stu-id="cd892-114">Maximum file length</span></span>
- <span data-ttu-id="cd892-115">En büyük veri kümesi boyutu</span><span class="sxs-lookup"><span data-stu-id="cd892-115">Maximum dataset size</span></span>
- <span data-ttu-id="cd892-116">En fazla Dizin derinliği</span><span class="sxs-lookup"><span data-stu-id="cd892-116">Maximum directory depth</span></span>

## <span data-ttu-id="cd892-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd892-117">EXAMPLES</span></span>

### <span data-ttu-id="cd892-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd892-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="cd892-119">Bu komut, sistemin ve C:\DATA'TEKI dosya ve klasörlerin uyumluluğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="cd892-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="cd892-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cd892-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="cd892-121">Bu komut C:\VERILERDEKI dosyaların ve klasörlerin uyumluluğunu denetler, ancak sistem uyumluluğu denetimi gerçekleştirmez.</span><span class="sxs-lookup"><span data-stu-id="cd892-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="cd892-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cd892-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="cd892-123">Bu komut, c: \ verilerdeki dosyaların ve klasörlerin uyumluluğunu denetler ve ardından sonuçları C:\resultsdizinine CSV dosyası olarak aktarır.</span><span class="sxs-lookup"><span data-stu-id="cd892-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="cd892-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd892-124">PARAMETERS</span></span>

### <span data-ttu-id="cd892-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="cd892-125">-ComputerName</span></span>
<span data-ttu-id="cd892-126">Bu bilgisayarı denetleme.</span><span class="sxs-lookup"><span data-stu-id="cd892-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="cd892-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="cd892-127">-Credential</span></span>
<span data-ttu-id="cd892-128">Doğrulama için kimlik bilgileriniz.</span><span class="sxs-lookup"><span data-stu-id="cd892-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="cd892-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="cd892-129">-Path</span></span>
<span data-ttu-id="cd892-130">Doğruladığımız paylaşımın UNC yolu.</span><span class="sxs-lookup"><span data-stu-id="cd892-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="cd892-131">-Quiet</span><span class="sxs-lookup"><span data-stu-id="cd892-131">-Quiet</span></span>
<span data-ttu-id="cd892-132">Çıkış raporunu konsola yazmayı bastırır.</span><span class="sxs-lookup"><span data-stu-id="cd892-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="cd892-133">-Skipnamespacedenetimlerini</span><span class="sxs-lookup"><span data-stu-id="cd892-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="cd892-134">Dosya ad alanı doğrulamalarını atlamak için bu bayrağı ayarlayın ve yalnızca sistem doğrulamaları gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="cd892-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="cd892-135">-Skipsystemdenetimleri</span><span class="sxs-lookup"><span data-stu-id="cd892-135">-SkipSystemChecks</span></span>
<span data-ttu-id="cd892-136">Sistem doğrulamalarını atlayıp yalnızca dosya ad alanı doğrulamaları gerçekleştirmek için bu bayrağı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd892-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="cd892-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd892-137">CommonParameters</span></span>
<span data-ttu-id="cd892-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd892-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd892-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd892-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd892-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd892-140">INPUTS</span></span>

### <span data-ttu-id="cd892-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cd892-141">None</span></span>

## <span data-ttu-id="cd892-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd892-142">OUTPUTS</span></span>

### <span data-ttu-id="cd892-143">Microsoft. Azure. Commands. Storagesehd. Evaluation. model. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="cd892-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="cd892-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd892-144">NOTES</span></span>
* <span data-ttu-id="cd892-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, storagessync, FileSync</span><span class="sxs-lookup"><span data-stu-id="cd892-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="cd892-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd892-146">RELATED LINKS</span></span>
