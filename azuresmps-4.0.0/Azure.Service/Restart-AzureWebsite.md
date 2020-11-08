---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105470"
---
# <span data-ttu-id="3a60b-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a60b-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="3a60b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a60b-103">Belirtilen Web sitesini durdurur ve yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3a60b-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="3a60b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a60b-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a60b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a60b-105">DESCRIPTION</span></span>
<span data-ttu-id="3a60b-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a60b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3a60b-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3a60b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3a60b-108">**Restart-AzureWebsite** cmdlet 'i durur ve belirtilen Web sitesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3a60b-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="3a60b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a60b-109">EXAMPLES</span></span>

### <span data-ttu-id="3a60b-110">Örnek 1: Web sitesini yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="3a60b-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="3a60b-111">Bu örnek MyWebsite adlı bir Web sitesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="3a60b-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="3a60b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a60b-112">PARAMETERS</span></span>

### <span data-ttu-id="3a60b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a60b-113">-Name</span></span>
<span data-ttu-id="3a60b-114">Yeniden başlatılacak Azure Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a60b-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="3a60b-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a60b-115">-PassThru</span></span>
<span data-ttu-id="3a60b-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a60b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a60b-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3a60b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a60b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a60b-118">-Profile</span></span>
<span data-ttu-id="3a60b-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a60b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a60b-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3a60b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a60b-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="3a60b-121">-Slot</span></span>
<span data-ttu-id="3a60b-122">Web sitesinin yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a60b-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="3a60b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a60b-123">CommonParameters</span></span>
<span data-ttu-id="3a60b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a60b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a60b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a60b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a60b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a60b-126">INPUTS</span></span>

## <span data-ttu-id="3a60b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a60b-127">OUTPUTS</span></span>

## <span data-ttu-id="3a60b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a60b-128">NOTES</span></span>

## <span data-ttu-id="3a60b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a60b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3a60b-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a60b-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="3a60b-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a60b-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="3a60b-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a60b-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="3a60b-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3a60b-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


