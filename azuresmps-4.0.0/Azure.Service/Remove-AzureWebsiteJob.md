---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105482"
---
# <span data-ttu-id="2252e-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2252e-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="2252e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2252e-102">SYNOPSIS</span></span>
<span data-ttu-id="2252e-103">Web sitesi için varolan bir Web işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2252e-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="2252e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2252e-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2252e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2252e-105">DESCRIPTION</span></span>
<span data-ttu-id="2252e-106">Web sitesi için varolan bir Web işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2252e-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="2252e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2252e-107">EXAMPLES</span></span>

### <span data-ttu-id="2252e-108">Örnek 1: Web sitesi için varolan Web işini kaldırma</span><span class="sxs-lookup"><span data-stu-id="2252e-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="2252e-109">Mywebsitesi MyWebJob adlı Web işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2252e-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="2252e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2252e-110">PARAMETERS</span></span>

### <span data-ttu-id="2252e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2252e-111">-Force</span></span>
<span data-ttu-id="2252e-112">Bu cmdlet 'in Web işini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2252e-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2252e-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2252e-113">-JobName</span></span>
<span data-ttu-id="2252e-114">Web işi adı.</span><span class="sxs-lookup"><span data-stu-id="2252e-114">The web job name.</span></span>

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

### <span data-ttu-id="2252e-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="2252e-115">-JobType</span></span>
<span data-ttu-id="2252e-116">Web işi türü.</span><span class="sxs-lookup"><span data-stu-id="2252e-116">The web job type.</span></span>
<span data-ttu-id="2252e-117">Veya sürekli olarak tetiklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2252e-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="2252e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2252e-118">-Name</span></span>
<span data-ttu-id="2252e-119">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="2252e-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="2252e-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="2252e-120">-Profile</span></span>
<span data-ttu-id="2252e-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2252e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2252e-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2252e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2252e-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="2252e-123">-Slot</span></span>
<span data-ttu-id="2252e-124">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="2252e-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="2252e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2252e-125">CommonParameters</span></span>
<span data-ttu-id="2252e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2252e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2252e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2252e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2252e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2252e-128">INPUTS</span></span>

## <span data-ttu-id="2252e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2252e-129">OUTPUTS</span></span>

## <span data-ttu-id="2252e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2252e-130">NOTES</span></span>

## <span data-ttu-id="2252e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2252e-131">RELATED LINKS</span></span>

[<span data-ttu-id="2252e-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2252e-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2252e-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2252e-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="2252e-134">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2252e-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="2252e-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2252e-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="2252e-136">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2252e-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


