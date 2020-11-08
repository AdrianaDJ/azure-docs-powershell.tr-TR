---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105770"
---
# <span data-ttu-id="a946d-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="a946d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a946d-102">SYNOPSIS</span></span>
<span data-ttu-id="a946d-103">Belirtilen Web sitesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a946d-103">Starts the specified website.</span></span>

## <span data-ttu-id="a946d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a946d-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a946d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a946d-105">DESCRIPTION</span></span>
<span data-ttu-id="a946d-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a946d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a946d-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a946d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a946d-108">**Start-AzureWebsite** cmdlet 'i Azure 'da çalışan belirli bir Web sitesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a946d-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="a946d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a946d-109">EXAMPLES</span></span>

## <span data-ttu-id="a946d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a946d-110">PARAMETERS</span></span>

### <span data-ttu-id="a946d-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="a946d-111">-Name</span></span>
<span data-ttu-id="a946d-112">Başlayacak Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a946d-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="a946d-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a946d-113">-PassThru</span></span>
<span data-ttu-id="a946d-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a946d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a946d-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a946d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a946d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="a946d-116">-Profile</span></span>
<span data-ttu-id="a946d-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a946d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a946d-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a946d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a946d-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a946d-119">-Slot</span></span>
<span data-ttu-id="a946d-120">Web sitesinin yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a946d-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="a946d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a946d-121">CommonParameters</span></span>
<span data-ttu-id="a946d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a946d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a946d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a946d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a946d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a946d-124">INPUTS</span></span>

## <span data-ttu-id="a946d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a946d-125">OUTPUTS</span></span>

## <span data-ttu-id="a946d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a946d-126">NOTES</span></span>

## <span data-ttu-id="a946d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a946d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a946d-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a946d-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="a946d-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="a946d-131">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="a946d-132">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a946d-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


