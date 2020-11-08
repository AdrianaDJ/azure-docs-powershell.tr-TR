---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106374"
---
# <span data-ttu-id="4f517-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="4f517-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="4f517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f517-102">SYNOPSIS</span></span>
<span data-ttu-id="4f517-103">Web sitesinin hata ayıklamasını verir.</span><span class="sxs-lookup"><span data-stu-id="4f517-103">Enables the website's debug.</span></span>

## <span data-ttu-id="4f517-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f517-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f517-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f517-105">DESCRIPTION</span></span>
<span data-ttu-id="4f517-106">Visual Studio 'da Web sitesinin hata ayıklama özelliğini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4f517-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="4f517-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f517-107">EXAMPLES</span></span>

### <span data-ttu-id="4f517-108">Visual Studio 2013 hata ayıklamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4f517-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="4f517-109">VS 2013 ' de hata ayıklamayı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f517-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="4f517-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f517-110">PARAMETERS</span></span>

### <span data-ttu-id="4f517-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f517-111">-Name</span></span>
<span data-ttu-id="4f517-112">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4f517-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="4f517-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f517-113">-PassThru</span></span>
<span data-ttu-id="4f517-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4f517-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f517-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4f517-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f517-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f517-116">-Profile</span></span>
<span data-ttu-id="4f517-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f517-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f517-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4f517-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f517-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4f517-119">-Slot</span></span>
<span data-ttu-id="4f517-120">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="4f517-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="4f517-121">-Version</span><span class="sxs-lookup"><span data-stu-id="4f517-121">-Version</span></span>
<span data-ttu-id="4f517-122">Visual Studio sürümü.</span><span class="sxs-lookup"><span data-stu-id="4f517-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="4f517-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f517-123">CommonParameters</span></span>
<span data-ttu-id="4f517-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f517-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f517-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f517-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f517-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f517-126">INPUTS</span></span>

## <span data-ttu-id="4f517-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f517-127">OUTPUTS</span></span>

## <span data-ttu-id="4f517-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f517-128">NOTES</span></span>

## <span data-ttu-id="4f517-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f517-129">RELATED LINKS</span></span>

[<span data-ttu-id="4f517-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="4f517-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="4f517-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4f517-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="4f517-132">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4f517-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="4f517-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4f517-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="4f517-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4f517-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


