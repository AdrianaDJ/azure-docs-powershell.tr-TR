---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105767"
---
# <span data-ttu-id="4c630-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4c630-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="4c630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c630-102">SYNOPSIS</span></span>
<span data-ttu-id="4c630-103">Web sitesi için Web işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="4c630-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="4c630-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c630-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c630-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c630-105">DESCRIPTION</span></span>
<span data-ttu-id="4c630-106">**Start-AzureWebsiteJob** cmdlet 'i Web sitesi için Web işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="4c630-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="4c630-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c630-107">EXAMPLES</span></span>

### <span data-ttu-id="4c630-108">Örnek 1: Web sitesi için Web işi başlatma</span><span class="sxs-lookup"><span data-stu-id="4c630-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="4c630-109">MyWebSite için MyWebJob adlı Web işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4c630-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="4c630-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c630-110">PARAMETERS</span></span>

### <span data-ttu-id="4c630-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="4c630-111">-JobName</span></span>
<span data-ttu-id="4c630-112">Web işi adı.</span><span class="sxs-lookup"><span data-stu-id="4c630-112">The web job name.</span></span>

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

### <span data-ttu-id="4c630-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="4c630-113">-JobType</span></span>
<span data-ttu-id="4c630-114">Web işi türü.</span><span class="sxs-lookup"><span data-stu-id="4c630-114">The web job type.</span></span>
<span data-ttu-id="4c630-115">Veya sürekli olarak tetiklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4c630-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="4c630-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c630-116">-Name</span></span>
<span data-ttu-id="4c630-117">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4c630-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="4c630-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4c630-118">-PassThru</span></span>
<span data-ttu-id="4c630-119">İşin başarıyla başlatıldığını gösteren bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c630-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="4c630-120">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="4c630-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="4c630-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c630-121">-Profile</span></span>
<span data-ttu-id="4c630-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c630-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c630-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4c630-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c630-124">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4c630-124">-Slot</span></span>
<span data-ttu-id="4c630-125">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="4c630-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="4c630-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c630-126">CommonParameters</span></span>
<span data-ttu-id="4c630-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c630-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c630-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c630-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c630-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c630-129">INPUTS</span></span>

## <span data-ttu-id="4c630-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c630-130">OUTPUTS</span></span>

## <span data-ttu-id="4c630-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c630-131">NOTES</span></span>

## <span data-ttu-id="4c630-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c630-132">RELATED LINKS</span></span>

[<span data-ttu-id="4c630-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4c630-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="4c630-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4c630-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="4c630-135">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4c630-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="4c630-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4c630-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="4c630-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4c630-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


