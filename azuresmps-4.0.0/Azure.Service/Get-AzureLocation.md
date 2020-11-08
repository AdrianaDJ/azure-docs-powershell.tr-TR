---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106336"
---
# <span data-ttu-id="ec8fc-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="ec8fc-101">Get-AzureLocation</span></span>

## <span data-ttu-id="ec8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8fc-103">Geçerli Azure aboneliği için kullanılabilir veri merkezi konumlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="ec8fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec8fc-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec8fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8fc-106">**Get-AzureLocation** cmdlet 'i, geçerli Azure aboneliği Için kullanılabilir Azure veri merkezlerinin listesini ve bunların özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="ec8fc-107">Bu cmdlet 'i çalıştırmadan önce, Select-AzureSubscription ve Set-AzureSubscription cmdlet 'lerini kullanarak geçerli aboneliğinizi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="ec8fc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec8fc-108">EXAMPLES</span></span>

### <span data-ttu-id="ec8fc-109">Örnek 1: konumları al</span><span class="sxs-lookup"><span data-stu-id="ec8fc-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="ec8fc-110">Bu komut, geçerli aboneliğin kullanılabilir veri merkezlerinin listesini ve özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="ec8fc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec8fc-111">PARAMETERS</span></span>

### <span data-ttu-id="ec8fc-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ec8fc-112">-InformationAction</span></span>
<span data-ttu-id="ec8fc-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec8fc-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ec8fc-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec8fc-115">'A</span><span class="sxs-lookup"><span data-stu-id="ec8fc-115">Continue</span></span>
- <span data-ttu-id="ec8fc-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="ec8fc-116">Ignore</span></span>
- <span data-ttu-id="ec8fc-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ec8fc-117">Inquire</span></span>
- <span data-ttu-id="ec8fc-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ec8fc-118">SilentlyContinue</span></span>
- <span data-ttu-id="ec8fc-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ec8fc-119">Stop</span></span>
- <span data-ttu-id="ec8fc-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ec8fc-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8fc-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ec8fc-121">-InformationVariable</span></span>
<span data-ttu-id="ec8fc-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8fc-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec8fc-123">-Profile</span></span>
<span data-ttu-id="ec8fc-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec8fc-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec8fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8fc-126">CommonParameters</span></span>
<span data-ttu-id="ec8fc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec8fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8fc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8fc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8fc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec8fc-129">INPUTS</span></span>

## <span data-ttu-id="ec8fc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec8fc-130">OUTPUTS</span></span>

## <span data-ttu-id="ec8fc-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec8fc-131">NOTES</span></span>

## <span data-ttu-id="ec8fc-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec8fc-132">RELATED LINKS</span></span>

