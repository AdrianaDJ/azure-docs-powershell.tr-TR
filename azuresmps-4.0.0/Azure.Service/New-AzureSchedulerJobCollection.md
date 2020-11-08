---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105980"
---
# <span data-ttu-id="21268-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="21268-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="21268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21268-102">SYNOPSIS</span></span>
<span data-ttu-id="21268-103">Zamanlayıcı iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21268-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="21268-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21268-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="21268-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21268-105">DESCRIPTION</span></span>
<span data-ttu-id="21268-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="21268-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="21268-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="21268-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="21268-108">**New-AzureSchedulerJobCollection** cmdlet 'i bir zamanlayıcı iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21268-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="21268-109">*Plan* parametresi için bir değer belirtmezseniz, cmdlet standart iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21268-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="21268-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21268-110">EXAMPLES</span></span>

### <span data-ttu-id="21268-111">Örnek 1: varsayılan değerleri içeren bir zamanlayıcı iş koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="21268-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="21268-112">Bu komut, JobCollection01 adlı standart bir zamanlayıcı iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21268-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="21268-113">Yeni koleksiyonda standart zamanlayıcı iş koleksiyonu için varsayılan iş sayısı ve maksimum yinelenme değerleri vardır.</span><span class="sxs-lookup"><span data-stu-id="21268-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="21268-114">Örnek 2: belirtilen değerlerle bir zamanlayıcı iş koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="21268-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="21268-115">Bu komut, JobCollection02 adlı standart bir zamanlayıcı iş koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21268-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="21268-116">Yeni koleksiyonun en fazla 30 iş sayısı ve saat başına 12 en fazla yinelemesi vardır.</span><span class="sxs-lookup"><span data-stu-id="21268-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="21268-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21268-117">PARAMETERS</span></span>

### <span data-ttu-id="21268-118">Frekans</span><span class="sxs-lookup"><span data-stu-id="21268-118">-Frequency</span></span>
<span data-ttu-id="21268-119">Bu Zamanlayıcı iş koleksiyonundaki herhangi bir işte belirtien yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21268-120">-Aralık</span><span class="sxs-lookup"><span data-stu-id="21268-120">-Interval</span></span>
<span data-ttu-id="21268-121">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21268-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="21268-122">-JobCollectionName</span></span>
<span data-ttu-id="21268-123">Yeni zamanlayıcı iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="21268-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="21268-124">-Location</span></span>
<span data-ttu-id="21268-125">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="21268-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="21268-126">Valid values are:</span></span> 

- <span data-ttu-id="21268-127">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="21268-127">Anywhere Asia</span></span>
- <span data-ttu-id="21268-128">Her yerde</span><span class="sxs-lookup"><span data-stu-id="21268-128">Anywhere Europe</span></span>
- <span data-ttu-id="21268-129">Her yerde</span><span class="sxs-lookup"><span data-stu-id="21268-129">Anywhere US</span></span>
- <span data-ttu-id="21268-130">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="21268-130">East Asia</span></span>
- <span data-ttu-id="21268-131">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="21268-131">East US</span></span>
- <span data-ttu-id="21268-132">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="21268-132">North Central US</span></span>
- <span data-ttu-id="21268-133">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="21268-133">North Europe</span></span>
- <span data-ttu-id="21268-134">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="21268-134">South Central US</span></span>
- <span data-ttu-id="21268-135">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="21268-135">Southeast Asia</span></span>
- <span data-ttu-id="21268-136">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="21268-136">West Europe</span></span>
- <span data-ttu-id="21268-137">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="21268-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21268-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="21268-138">-MaxJobCount</span></span>
<span data-ttu-id="21268-139">Zamanlayıcı iş koleksiyonunda oluşturulabilecek en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21268-140">-Plan</span><span class="sxs-lookup"><span data-stu-id="21268-140">-Plan</span></span>
<span data-ttu-id="21268-141">Zamanlayıcı işi koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="21268-142">-Profil</span><span class="sxs-lookup"><span data-stu-id="21268-142">-Profile</span></span>
<span data-ttu-id="21268-143">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21268-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="21268-144">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="21268-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="21268-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21268-145">CommonParameters</span></span>
<span data-ttu-id="21268-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21268-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21268-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21268-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21268-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21268-148">INPUTS</span></span>

## <span data-ttu-id="21268-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21268-149">OUTPUTS</span></span>

## <span data-ttu-id="21268-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21268-150">NOTES</span></span>

## <span data-ttu-id="21268-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21268-151">RELATED LINKS</span></span>

[<span data-ttu-id="21268-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="21268-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="21268-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="21268-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="21268-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="21268-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


