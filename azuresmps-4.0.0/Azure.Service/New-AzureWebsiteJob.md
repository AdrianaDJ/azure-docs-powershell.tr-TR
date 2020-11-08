---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106183"
---
# <span data-ttu-id="00402-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="00402-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="00402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00402-102">SYNOPSIS</span></span>
<span data-ttu-id="00402-103">Web sitesi için Web işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00402-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="00402-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00402-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00402-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00402-105">DESCRIPTION</span></span>
<span data-ttu-id="00402-106">**New-AzureWebsiteJob** cmdlet 'i Web sitesi için Web işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00402-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="00402-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00402-107">EXAMPLES</span></span>

### <span data-ttu-id="00402-108">Örnek 1: Web sitesi için yeni Web işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="00402-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="00402-109">MyWebsite Web sitesinde job.bat aramak için sürekli bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00402-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="00402-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00402-110">PARAMETERS</span></span>

### <span data-ttu-id="00402-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="00402-111">-JobFile</span></span>
<span data-ttu-id="00402-112">Web işi dosyası.</span><span class="sxs-lookup"><span data-stu-id="00402-112">The web job file.</span></span>

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

### <span data-ttu-id="00402-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="00402-113">-JobName</span></span>
<span data-ttu-id="00402-114">Web işi adı.</span><span class="sxs-lookup"><span data-stu-id="00402-114">The web job name.</span></span>

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

### <span data-ttu-id="00402-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="00402-115">-JobType</span></span>
<span data-ttu-id="00402-116">Web işi türü.</span><span class="sxs-lookup"><span data-stu-id="00402-116">The web job type.</span></span>
<span data-ttu-id="00402-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="00402-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00402-118">Tetiklenen</span><span class="sxs-lookup"><span data-stu-id="00402-118">Triggered</span></span> 
- <span data-ttu-id="00402-119">Eğri</span><span class="sxs-lookup"><span data-stu-id="00402-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00402-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="00402-120">-Name</span></span>
<span data-ttu-id="00402-121">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="00402-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="00402-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="00402-122">-Profile</span></span>
<span data-ttu-id="00402-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00402-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00402-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="00402-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00402-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="00402-125">-Slot</span></span>
<span data-ttu-id="00402-126">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="00402-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="00402-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00402-127">CommonParameters</span></span>
<span data-ttu-id="00402-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00402-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00402-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00402-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00402-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00402-130">INPUTS</span></span>

## <span data-ttu-id="00402-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00402-131">OUTPUTS</span></span>

## <span data-ttu-id="00402-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00402-132">NOTES</span></span>

## <span data-ttu-id="00402-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00402-133">RELATED LINKS</span></span>

[<span data-ttu-id="00402-134">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="00402-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="00402-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="00402-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="00402-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="00402-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="00402-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="00402-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="00402-138">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="00402-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


