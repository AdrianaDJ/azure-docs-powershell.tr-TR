---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106128"
---
# <span data-ttu-id="0606b-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0606b-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="0606b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0606b-102">SYNOPSIS</span></span>
<span data-ttu-id="0606b-103">Zamanlayıcı iş koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="0606b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0606b-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0606b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0606b-105">DESCRIPTION</span></span>
<span data-ttu-id="0606b-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0606b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0606b-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0606b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0606b-108">**Remove-AzureSchedulerJobCollection** cmdlet 'i, bir zamanlayıcı iş koleksiyonunu ve bu koleksiyonun altındaki işleri siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="0606b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0606b-109">EXAMPLES</span></span>

### <span data-ttu-id="0606b-110">Örnek 1: bir konum için iş koleksiyonunu silme</span><span class="sxs-lookup"><span data-stu-id="0606b-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="0606b-111">Bu komut, Kuzey merkezi JobCollection01 adındaki zamanlayıcı iş koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="0606b-112">Komut JobCollection01 altındaki işleri de siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="0606b-113">Örnek 2: bir iş konumunu silme</span><span class="sxs-lookup"><span data-stu-id="0606b-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="0606b-114">Bu komut, JobCollection02 adındaki zamanlayıcı iş koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="0606b-115">Komut JobCollection02 altındaki işleri de siler.</span><span class="sxs-lookup"><span data-stu-id="0606b-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="0606b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0606b-116">PARAMETERS</span></span>

### <span data-ttu-id="0606b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0606b-117">-Force</span></span>
<span data-ttu-id="0606b-118">Bu cmdlet 'in zamanlayıcı iş koleksiyonunu onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0606b-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0606b-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0606b-119">-JobCollectionName</span></span>
<span data-ttu-id="0606b-120">Silinecek zamanlayıcı iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0606b-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="0606b-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="0606b-121">-Location</span></span>
<span data-ttu-id="0606b-122">Bulut hizmetini barındıran konumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0606b-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="0606b-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0606b-123">Valid values are:</span></span> 

- <span data-ttu-id="0606b-124">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="0606b-124">Anywhere Asia</span></span>
- <span data-ttu-id="0606b-125">Her yerde</span><span class="sxs-lookup"><span data-stu-id="0606b-125">Anywhere Europe</span></span>
- <span data-ttu-id="0606b-126">Her yerde</span><span class="sxs-lookup"><span data-stu-id="0606b-126">Anywhere US</span></span>
- <span data-ttu-id="0606b-127">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="0606b-127">East Asia</span></span>
- <span data-ttu-id="0606b-128">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="0606b-128">East US</span></span>
- <span data-ttu-id="0606b-129">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="0606b-129">North Central US</span></span>
- <span data-ttu-id="0606b-130">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="0606b-130">North Europe</span></span>
- <span data-ttu-id="0606b-131">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="0606b-131">South Central US</span></span>
- <span data-ttu-id="0606b-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="0606b-132">Southeast Asia</span></span>
- <span data-ttu-id="0606b-133">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="0606b-133">West Europe</span></span>
- <span data-ttu-id="0606b-134">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="0606b-134">West US</span></span>

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

### <span data-ttu-id="0606b-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="0606b-135">-Profile</span></span>
<span data-ttu-id="0606b-136">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0606b-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0606b-137">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0606b-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0606b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0606b-138">CommonParameters</span></span>
<span data-ttu-id="0606b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0606b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0606b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0606b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0606b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0606b-141">INPUTS</span></span>

## <span data-ttu-id="0606b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0606b-142">OUTPUTS</span></span>

## <span data-ttu-id="0606b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0606b-143">NOTES</span></span>

## <span data-ttu-id="0606b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0606b-144">RELATED LINKS</span></span>

[<span data-ttu-id="0606b-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0606b-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0606b-146">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0606b-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="0606b-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0606b-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


