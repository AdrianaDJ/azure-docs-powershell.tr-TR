---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105838"
---
# <span data-ttu-id="0d1b1-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0d1b1-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="0d1b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1b1-103">Web sitesi için Web işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="0d1b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d1b1-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d1b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d1b1-105">DESCRIPTION</span></span>
<span data-ttu-id="0d1b1-106">**Stop-AzureWebsiteJob** cmdlet 'i Web sitesi için Web işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="0d1b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d1b1-107">EXAMPLES</span></span>

### <span data-ttu-id="0d1b1-108">Örnek 1: Web sitesi için Web işini durdurma</span><span class="sxs-lookup"><span data-stu-id="0d1b1-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="0d1b1-109">MyWebSite için MyWebJob adlı Web işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="0d1b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d1b1-110">PARAMETERS</span></span>

### <span data-ttu-id="0d1b1-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="0d1b1-111">-JobName</span></span>
<span data-ttu-id="0d1b1-112">Web işi adı.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-112">The web job name.</span></span>

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

### <span data-ttu-id="0d1b1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d1b1-113">-Name</span></span>
<span data-ttu-id="0d1b1-114">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="0d1b1-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d1b1-115">-PassThru</span></span>
<span data-ttu-id="0d1b1-116">İşin başarıyla durdurulduğunu gösteren bir Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="0d1b1-117">Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="0d1b1-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d1b1-118">-Profile</span></span>
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

### <span data-ttu-id="0d1b1-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="0d1b1-119">-Slot</span></span>
<span data-ttu-id="0d1b1-120">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="0d1b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1b1-121">CommonParameters</span></span>
<span data-ttu-id="0d1b1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d1b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1b1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1b1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1b1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d1b1-124">INPUTS</span></span>

## <span data-ttu-id="0d1b1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d1b1-125">OUTPUTS</span></span>

## <span data-ttu-id="0d1b1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d1b1-126">NOTES</span></span>

## <span data-ttu-id="0d1b1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d1b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d1b1-128">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0d1b1-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="0d1b1-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0d1b1-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="0d1b1-130">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0d1b1-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="0d1b1-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0d1b1-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="0d1b1-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0d1b1-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


