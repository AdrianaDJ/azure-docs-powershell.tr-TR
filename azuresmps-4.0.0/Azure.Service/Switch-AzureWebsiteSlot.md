---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105939"
---
# <span data-ttu-id="fbe00-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="fbe00-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="fbe00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe00-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe00-103">Başka bir yuvalı Web sitesinin üretim yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="fbe00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbe00-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbe00-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe00-106">**Switch-AzureWebsiteSlot** cmdlet 'i, başka bir yuvaya sahip bir Web sitesinin üretim yuvasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="fbe00-107">Bu, yalnızca iki yuvalarla birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="fbe00-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="fbe00-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbe00-108">EXAMPLES</span></span>

### <span data-ttu-id="fbe00-109">Örnek 1: Web sitesi yuvasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="fbe00-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="fbe00-110">Azure Web sitesi MyWebsite yedekleme yuvasına üretim yuvası ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="fbe00-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="fbe00-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbe00-111">PARAMETERS</span></span>

### <span data-ttu-id="fbe00-112">-Force</span><span class="sxs-lookup"><span data-stu-id="fbe00-112">-Force</span></span>
<span data-ttu-id="fbe00-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fbe00-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbe00-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbe00-114">-Name</span></span>
<span data-ttu-id="fbe00-115">Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="fbe00-115">The name of the website.</span></span>

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

### <span data-ttu-id="fbe00-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="fbe00-116">-Profile</span></span>
<span data-ttu-id="fbe00-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbe00-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fbe00-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fbe00-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="fbe00-119">-Slot1</span></span>
<span data-ttu-id="fbe00-120">İlk yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-120">Specifies the first slot.</span></span>

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

### <span data-ttu-id="fbe00-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="fbe00-121">-Slot2</span></span>
<span data-ttu-id="fbe00-122">İkinci yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-122">Specifies the second slot.</span></span>

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

### <span data-ttu-id="fbe00-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbe00-123">-Confirm</span></span>
<span data-ttu-id="fbe00-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbe00-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe00-125">-WhatIf</span></span>
<span data-ttu-id="fbe00-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbe00-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe00-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbe00-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe00-128">CommonParameters</span></span>
<span data-ttu-id="fbe00-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbe00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe00-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe00-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe00-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbe00-131">INPUTS</span></span>

## <span data-ttu-id="fbe00-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbe00-132">OUTPUTS</span></span>

## <span data-ttu-id="fbe00-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbe00-133">NOTES</span></span>

## <span data-ttu-id="fbe00-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbe00-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbe00-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fbe00-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="fbe00-136">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fbe00-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="fbe00-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fbe00-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="fbe00-138">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fbe00-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


