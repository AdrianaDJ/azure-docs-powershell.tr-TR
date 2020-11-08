---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106310"
---
# <span data-ttu-id="75c56-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="75c56-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="75c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c56-102">SYNOPSIS</span></span>
<span data-ttu-id="75c56-103">Zamanlayıcı işi için geçmiş alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="75c56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75c56-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="75c56-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75c56-105">DESCRIPTION</span></span>
<span data-ttu-id="75c56-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="75c56-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="75c56-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="75c56-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="75c56-108">**Get-AzureSchedulerJobHistory** cmdlet 'i bir zamanlayıcı işinin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="75c56-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75c56-109">EXAMPLES</span></span>

### <span data-ttu-id="75c56-110">Örnek 1: bir işin adını kullanarak geçmişi alma</span><span class="sxs-lookup"><span data-stu-id="75c56-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="75c56-111">Bu komut, Job01 adlı işin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="75c56-112">Bu iş, belirtilen konumda JobCollection01 adlı iş koleksiyonuna aittir.</span><span class="sxs-lookup"><span data-stu-id="75c56-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="75c56-113">Örnek 2: bir işin adını kullanarak geçmişi alma</span><span class="sxs-lookup"><span data-stu-id="75c56-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="75c56-114">Bu komut, durumu başarısız olan Job12 adlı işin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="75c56-115">Bu iş, belirtilen konumda JobCollection01 adlı iş koleksiyonuna aittir.</span><span class="sxs-lookup"><span data-stu-id="75c56-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="75c56-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75c56-116">PARAMETERS</span></span>

### <span data-ttu-id="75c56-117">-Önce</span><span class="sxs-lookup"><span data-stu-id="75c56-117">-First</span></span>
<span data-ttu-id="75c56-118">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="75c56-119">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="75c56-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c56-120">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="75c56-120">-IncludeTotalCount</span></span>
<span data-ttu-id="75c56-121">Veri kümesindeki toplam nesne sayısını (tamsayı) ve ardından seçilen nesneleri raporlar.</span><span class="sxs-lookup"><span data-stu-id="75c56-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="75c56-122">Cmdlet toplam sayısını belirleyemiyorsa, "bilinmeyen toplam sayı" görüntüler.</span><span class="sxs-lookup"><span data-stu-id="75c56-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="75c56-123">Tamsayı, toplam sayı değerinin güvenilirliğini belirten bir doğruluk özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="75c56-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="75c56-124">0,0 ile 0,0 1,0 arasındaki doğruluk değeri aralığı, cmdlet 'in nesneleri saymadığı anlamına gelir; 1,0, Count 'un tam olduğu ve 0,0 ile 1,0 arasındaki bir değer giderek gittikçe güvenilir bir tahmini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="75c56-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c56-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="75c56-125">-JobCollectionName</span></span>
<span data-ttu-id="75c56-126">Zamanlayıcı iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c56-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="75c56-127">Bu cmdlet, bu parametrenin belirttiği koleksiyona ait olan bir işin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="75c56-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="75c56-128">-JobName</span></span>
<span data-ttu-id="75c56-129">Geçmişin alınacağı zamanlayıcı işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c56-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="75c56-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="75c56-130">-JobStatus</span></span>
<span data-ttu-id="75c56-131">Geçmişin alınacağı zamanlayıcı işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c56-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="75c56-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75c56-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75c56-133">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="75c56-133">Completed</span></span>
- <span data-ttu-id="75c56-134">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="75c56-134">Failed</span></span>

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

### <span data-ttu-id="75c56-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="75c56-135">-Location</span></span>
<span data-ttu-id="75c56-136">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c56-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="75c56-137">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="75c56-137">Valid values are:</span></span> 

- <span data-ttu-id="75c56-138">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="75c56-138">Anywhere Asia</span></span>
- <span data-ttu-id="75c56-139">Her yerde</span><span class="sxs-lookup"><span data-stu-id="75c56-139">Anywhere Europe</span></span>
- <span data-ttu-id="75c56-140">Her yerde</span><span class="sxs-lookup"><span data-stu-id="75c56-140">Anywhere US</span></span>
- <span data-ttu-id="75c56-141">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="75c56-141">East Asia</span></span>
- <span data-ttu-id="75c56-142">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="75c56-142">East US</span></span>
- <span data-ttu-id="75c56-143">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="75c56-143">North Central US</span></span>
- <span data-ttu-id="75c56-144">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="75c56-144">North Europe</span></span>
- <span data-ttu-id="75c56-145">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="75c56-145">South Central US</span></span>
- <span data-ttu-id="75c56-146">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="75c56-146">Southeast Asia</span></span>
- <span data-ttu-id="75c56-147">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="75c56-147">West Europe</span></span>
- <span data-ttu-id="75c56-148">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="75c56-148">West US</span></span>

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

### <span data-ttu-id="75c56-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="75c56-149">-Profile</span></span>
<span data-ttu-id="75c56-150">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c56-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75c56-151">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="75c56-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75c56-152">-Atla</span><span class="sxs-lookup"><span data-stu-id="75c56-152">-Skip</span></span>
<span data-ttu-id="75c56-153">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="75c56-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="75c56-154">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="75c56-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c56-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c56-155">CommonParameters</span></span>
<span data-ttu-id="75c56-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75c56-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c56-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c56-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c56-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75c56-158">INPUTS</span></span>

## <span data-ttu-id="75c56-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75c56-159">OUTPUTS</span></span>

## <span data-ttu-id="75c56-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75c56-160">NOTES</span></span>

## <span data-ttu-id="75c56-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75c56-161">RELATED LINKS</span></span>

[<span data-ttu-id="75c56-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="75c56-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="75c56-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="75c56-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


