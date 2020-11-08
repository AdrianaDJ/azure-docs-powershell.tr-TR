---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105612"
---
# <span data-ttu-id="40cb7-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="40cb7-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="40cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="40cb7-103">Planlayıcı iş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="40cb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40cb7-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="40cb7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="40cb7-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="40cb7-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="40cb7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="40cb7-108">**Get-AzureSchedulerJobCollection** cmdlet 'i bir veya daha fazla zamanlayıcı iş koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="40cb7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40cb7-109">EXAMPLES</span></span>

### <span data-ttu-id="40cb7-110">Örnek 1: tüm koleksiyonları al</span><span class="sxs-lookup"><span data-stu-id="40cb7-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="40cb7-111">Bu komut, geçerli abonelikteki tüm konumlarda tüm Zamanlayıcı işi koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="40cb7-112">Örnek 2: bir konumun tüm koleksiyonlarını alma</span><span class="sxs-lookup"><span data-stu-id="40cb7-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="40cb7-113">Bu komut, Kuzey Merkezi ABD adlı konumdaki tüm zamanlayıcı iş koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="40cb7-114">Örnek 3: ad kullanarak koleksiyon alma</span><span class="sxs-lookup"><span data-stu-id="40cb7-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="40cb7-115">Bu komut, JobCollection01 adındaki zamanlayıcı iş koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="40cb7-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="40cb7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40cb7-116">PARAMETERS</span></span>

### <span data-ttu-id="40cb7-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="40cb7-117">-JobCollectionName</span></span>
<span data-ttu-id="40cb7-118">Alınacak zamanlayıcı iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cb7-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="40cb7-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="40cb7-119">-Location</span></span>
<span data-ttu-id="40cb7-120">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cb7-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="40cb7-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="40cb7-121">Valid values are:</span></span> 

- <span data-ttu-id="40cb7-122">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="40cb7-122">Anywhere Asia</span></span>
- <span data-ttu-id="40cb7-123">Her yerde</span><span class="sxs-lookup"><span data-stu-id="40cb7-123">Anywhere Europe</span></span>
- <span data-ttu-id="40cb7-124">Her yerde</span><span class="sxs-lookup"><span data-stu-id="40cb7-124">Anywhere US</span></span>
- <span data-ttu-id="40cb7-125">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="40cb7-125">East Asia</span></span>
- <span data-ttu-id="40cb7-126">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="40cb7-126">East US</span></span>
- <span data-ttu-id="40cb7-127">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="40cb7-127">North Central US</span></span>
- <span data-ttu-id="40cb7-128">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="40cb7-128">North Europe</span></span>
- <span data-ttu-id="40cb7-129">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="40cb7-129">South Central US</span></span>
- <span data-ttu-id="40cb7-130">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="40cb7-130">Southeast Asia</span></span>
- <span data-ttu-id="40cb7-131">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="40cb7-131">West Europe</span></span>
- <span data-ttu-id="40cb7-132">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="40cb7-132">West US</span></span>

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

### <span data-ttu-id="40cb7-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="40cb7-133">-Profile</span></span>
<span data-ttu-id="40cb7-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40cb7-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40cb7-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="40cb7-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40cb7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cb7-136">CommonParameters</span></span>
<span data-ttu-id="40cb7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40cb7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cb7-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40cb7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cb7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40cb7-139">INPUTS</span></span>

## <span data-ttu-id="40cb7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40cb7-140">OUTPUTS</span></span>

## <span data-ttu-id="40cb7-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40cb7-141">NOTES</span></span>

## <span data-ttu-id="40cb7-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40cb7-142">RELATED LINKS</span></span>

[<span data-ttu-id="40cb7-143">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="40cb7-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="40cb7-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="40cb7-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="40cb7-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="40cb7-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


