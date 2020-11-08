---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106129"
---
# <span data-ttu-id="e2e10-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e2e10-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="e2e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e10-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e10-103">Zamanlayıcı işini siler.</span><span class="sxs-lookup"><span data-stu-id="e2e10-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="e2e10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2e10-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2e10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2e10-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e10-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2e10-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e2e10-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e2e10-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e2e10-108">**Remove-AzureSchedulerJob** cmdlet 'i bir zamanlayıcı işini siler.</span><span class="sxs-lookup"><span data-stu-id="e2e10-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="e2e10-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2e10-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e10-110">Örnek 1: zamanlayıcı işini silme</span><span class="sxs-lookup"><span data-stu-id="e2e10-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="e2e10-111">Bu komut, Job17 adındaki işi siler.</span><span class="sxs-lookup"><span data-stu-id="e2e10-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="e2e10-112">Bu iş, JobCollection01 adındaki ve belirtilen konumda yer alan iş koleksiyonunun bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e2e10-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="e2e10-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2e10-113">PARAMETERS</span></span>

### <span data-ttu-id="e2e10-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e2e10-114">-Force</span></span>
<span data-ttu-id="e2e10-115">Bu cmdlet 'in zamanlayıcı işini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2e10-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e10-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e2e10-116">-JobCollectionName</span></span>
<span data-ttu-id="e2e10-117">Silinecek zamanlayıcı işini içeren koleksiyonun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e10-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="e2e10-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="e2e10-118">-JobName</span></span>
<span data-ttu-id="e2e10-119">Silinecek zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e10-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="e2e10-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="e2e10-120">-Location</span></span>
<span data-ttu-id="e2e10-121">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e10-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="e2e10-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e2e10-122">Valid values are:</span></span> 

- <span data-ttu-id="e2e10-123">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="e2e10-123">Anywhere Asia</span></span>
- <span data-ttu-id="e2e10-124">Her yerde</span><span class="sxs-lookup"><span data-stu-id="e2e10-124">Anywhere Europe</span></span>
- <span data-ttu-id="e2e10-125">Her yerde</span><span class="sxs-lookup"><span data-stu-id="e2e10-125">Anywhere US</span></span>
- <span data-ttu-id="e2e10-126">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="e2e10-126">East Asia</span></span>
- <span data-ttu-id="e2e10-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="e2e10-127">East US</span></span>
- <span data-ttu-id="e2e10-128">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="e2e10-128">North Central US</span></span>
- <span data-ttu-id="e2e10-129">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="e2e10-129">North Europe</span></span>
- <span data-ttu-id="e2e10-130">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="e2e10-130">South Central US</span></span>
- <span data-ttu-id="e2e10-131">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="e2e10-131">Southeast Asia</span></span>
- <span data-ttu-id="e2e10-132">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="e2e10-132">West Europe</span></span>
- <span data-ttu-id="e2e10-133">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="e2e10-133">West US</span></span>

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

### <span data-ttu-id="e2e10-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2e10-134">-Profile</span></span>
<span data-ttu-id="e2e10-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e10-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2e10-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2e10-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2e10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e10-137">CommonParameters</span></span>
<span data-ttu-id="e2e10-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2e10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e10-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e10-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e10-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2e10-140">INPUTS</span></span>

## <span data-ttu-id="e2e10-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2e10-141">OUTPUTS</span></span>

## <span data-ttu-id="e2e10-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2e10-142">NOTES</span></span>

## <span data-ttu-id="e2e10-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2e10-143">RELATED LINKS</span></span>

[<span data-ttu-id="e2e10-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e2e10-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


