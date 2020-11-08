---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105443"
---
# <span data-ttu-id="a151f-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a151f-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="a151f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a151f-102">SYNOPSIS</span></span>
<span data-ttu-id="a151f-103">Zamanlayıcı iş koleksiyonunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a151f-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="a151f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a151f-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a151f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a151f-105">DESCRIPTION</span></span>
<span data-ttu-id="a151f-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a151f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a151f-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a151f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a151f-108">**Set-AzureSchedulerJobCollection** cmdlet 'i bir zamanlayıcı iş koleksiyonunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a151f-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="a151f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a151f-109">EXAMPLES</span></span>

### <span data-ttu-id="a151f-110">Örnek 1: bir koleksiyonun en yüksek iş sayısını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a151f-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="a151f-111">Bu komut JobCollection01 adındaki mevcut zamanlayıcı iş koleksiyonunda maksimum iş sayısını 30 olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a151f-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="a151f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a151f-112">PARAMETERS</span></span>

### <span data-ttu-id="a151f-113">Frekans</span><span class="sxs-lookup"><span data-stu-id="a151f-113">-Frequency</span></span>
<span data-ttu-id="a151f-114">Bu Zamanlayıcı iş koleksiyonundaki herhangi bir işte belirtien yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="a151f-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a151f-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a151f-116">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="a151f-116">Minute</span></span>
- <span data-ttu-id="a151f-117">Saati</span><span class="sxs-lookup"><span data-stu-id="a151f-117">Hour</span></span>
- <span data-ttu-id="a151f-118">Günündeki</span><span class="sxs-lookup"><span data-stu-id="a151f-118">Day</span></span>
- <span data-ttu-id="a151f-119">Haftada</span><span class="sxs-lookup"><span data-stu-id="a151f-119">Week</span></span>
- <span data-ttu-id="a151f-120">Ay</span><span class="sxs-lookup"><span data-stu-id="a151f-120">Month</span></span>
- <span data-ttu-id="a151f-121">Yılındaki</span><span class="sxs-lookup"><span data-stu-id="a151f-121">Year</span></span>

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

### <span data-ttu-id="a151f-122">-Aralık</span><span class="sxs-lookup"><span data-stu-id="a151f-122">-Interval</span></span>
<span data-ttu-id="a151f-123">*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="a151f-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a151f-124">-JobCollectionName</span></span>
<span data-ttu-id="a151f-125">Güncelleştirilecek zamanlayıcı iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="a151f-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="a151f-126">-Location</span></span>
<span data-ttu-id="a151f-127">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="a151f-128">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a151f-128">Valid values are:</span></span> 

- <span data-ttu-id="a151f-129">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="a151f-129">Anywhere Asia</span></span>
- <span data-ttu-id="a151f-130">Her yerde</span><span class="sxs-lookup"><span data-stu-id="a151f-130">Anywhere Europe</span></span>
- <span data-ttu-id="a151f-131">Her yerde</span><span class="sxs-lookup"><span data-stu-id="a151f-131">Anywhere US</span></span>
- <span data-ttu-id="a151f-132">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="a151f-132">East Asia</span></span>
- <span data-ttu-id="a151f-133">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="a151f-133">East US</span></span>
- <span data-ttu-id="a151f-134">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="a151f-134">North Central US</span></span>
- <span data-ttu-id="a151f-135">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="a151f-135">North Europe</span></span>
- <span data-ttu-id="a151f-136">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="a151f-136">South Central US</span></span>
- <span data-ttu-id="a151f-137">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="a151f-137">Southeast Asia</span></span>
- <span data-ttu-id="a151f-138">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="a151f-138">West Europe</span></span>
- <span data-ttu-id="a151f-139">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="a151f-139">West US</span></span>

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

### <span data-ttu-id="a151f-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="a151f-140">-MaxJobCount</span></span>
<span data-ttu-id="a151f-141">Zamanlayıcı iş koleksiyonunda oluşturulabilecek en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="a151f-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a151f-142">-PassThru</span></span>
<span data-ttu-id="a151f-143">Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a151f-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="a151f-144">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a151f-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a151f-145">-Plan</span><span class="sxs-lookup"><span data-stu-id="a151f-145">-Plan</span></span>
<span data-ttu-id="a151f-146">Zamanlayıcı işi koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="a151f-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="a151f-147">-Profile</span></span>
<span data-ttu-id="a151f-148">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a151f-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a151f-149">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a151f-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a151f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a151f-150">CommonParameters</span></span>
<span data-ttu-id="a151f-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a151f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a151f-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a151f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a151f-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a151f-153">INPUTS</span></span>

## <span data-ttu-id="a151f-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a151f-154">OUTPUTS</span></span>

## <span data-ttu-id="a151f-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a151f-155">NOTES</span></span>

## <span data-ttu-id="a151f-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a151f-156">RELATED LINKS</span></span>

[<span data-ttu-id="a151f-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a151f-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a151f-158">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a151f-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="a151f-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a151f-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


