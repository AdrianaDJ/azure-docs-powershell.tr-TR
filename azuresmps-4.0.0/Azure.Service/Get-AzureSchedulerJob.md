---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106311"
---
# <span data-ttu-id="04756-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="04756-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="04756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04756-102">SYNOPSIS</span></span>
<span data-ttu-id="04756-103">Planlayıcı işlerinin listesini veya belirli bir zamanlayıcı işini alır.</span><span class="sxs-lookup"><span data-stu-id="04756-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="04756-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04756-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04756-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="04756-105">DESCRIPTION</span></span>
<span data-ttu-id="04756-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04756-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="04756-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="04756-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="04756-108">**Get-AzureSchedulerJobCollection** cmdlet 'i zamanlayıcı işlerinin bir listesini veya belirli bir zamanlayıcı işini alır.</span><span class="sxs-lookup"><span data-stu-id="04756-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="04756-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04756-109">EXAMPLES</span></span>

### <span data-ttu-id="04756-110">Örnek 1: koleksiyondaki tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="04756-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="04756-111">Bu komut, JobCollection01 adındaki iş koleksiyonunun parçası olan Zamanlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="04756-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="04756-112">Örnek 2: adlandırılmış iş edinme</span><span class="sxs-lookup"><span data-stu-id="04756-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="04756-113">Bu komut, belirtilen konumdaki JobCollection01 adındaki koleksiyonda Job01 adındaki işi alır.</span><span class="sxs-lookup"><span data-stu-id="04756-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="04756-114">Örnek 3: koleksiyonda devre dışı işler alma</span><span class="sxs-lookup"><span data-stu-id="04756-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="04756-115">Bu komut, belirtilen konumda JobCollection01 'in parçası olan tüm devre dışı Planlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="04756-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="04756-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04756-116">PARAMETERS</span></span>

### <span data-ttu-id="04756-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="04756-117">-JobCollectionName</span></span>
<span data-ttu-id="04756-118">Alınacak zamanlayıcı işini içeren koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04756-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04756-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="04756-119">-JobName</span></span>
<span data-ttu-id="04756-120">Alınacak zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04756-120">Specifies the name of a scheduler job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04756-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="04756-121">-JobState</span></span>
<span data-ttu-id="04756-122">Alınacak zamanlayıcı işlerinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="04756-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="04756-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04756-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04756-124">Etkin</span><span class="sxs-lookup"><span data-stu-id="04756-124">Enabled</span></span>
- <span data-ttu-id="04756-125">DISABLED</span><span class="sxs-lookup"><span data-stu-id="04756-125">Disabled</span></span>
- <span data-ttu-id="04756-126">Hatalı</span><span class="sxs-lookup"><span data-stu-id="04756-126">Faulted</span></span>
- <span data-ttu-id="04756-127">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="04756-127">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04756-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="04756-128">-Location</span></span>
<span data-ttu-id="04756-129">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04756-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="04756-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04756-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04756-131">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="04756-131">Anywhere Asia</span></span>
- <span data-ttu-id="04756-132">Her yerde</span><span class="sxs-lookup"><span data-stu-id="04756-132">Anywhere Europe</span></span>
- <span data-ttu-id="04756-133">Her yerde</span><span class="sxs-lookup"><span data-stu-id="04756-133">Anywhere US</span></span>
- <span data-ttu-id="04756-134">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="04756-134">East Asia</span></span>
- <span data-ttu-id="04756-135">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="04756-135">East US</span></span>
- <span data-ttu-id="04756-136">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="04756-136">North Central US</span></span>
- <span data-ttu-id="04756-137">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="04756-137">North Europe</span></span>
- <span data-ttu-id="04756-138">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="04756-138">South Central US</span></span>
- <span data-ttu-id="04756-139">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="04756-139">Southeast Asia</span></span>
- <span data-ttu-id="04756-140">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="04756-140">West Europe</span></span>
- <span data-ttu-id="04756-141">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="04756-141">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04756-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="04756-142">-Profile</span></span>
<span data-ttu-id="04756-143">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04756-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04756-144">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="04756-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04756-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04756-145">CommonParameters</span></span>
<span data-ttu-id="04756-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04756-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04756-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04756-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04756-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04756-148">INPUTS</span></span>

## <span data-ttu-id="04756-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04756-149">OUTPUTS</span></span>

## <span data-ttu-id="04756-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04756-150">NOTES</span></span>

## <span data-ttu-id="04756-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04756-151">RELATED LINKS</span></span>

[<span data-ttu-id="04756-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="04756-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


