---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105691"
---
# <span data-ttu-id="646e5-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="646e5-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="646e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="646e5-102">SYNOPSIS</span></span>
<span data-ttu-id="646e5-103">Web sitesinin hata ayıklamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="646e5-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="646e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="646e5-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="646e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="646e5-105">DESCRIPTION</span></span>
<span data-ttu-id="646e5-106">Visual Studio 'da Web sitesinin hata ayıklamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="646e5-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="646e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="646e5-107">EXAMPLES</span></span>

### <span data-ttu-id="646e5-108">--------------Devre dışı bırakma--------------</span><span class="sxs-lookup"><span data-stu-id="646e5-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="646e5-109">MyWebsite Web sitesinde Web sitesi hata ayıklamasını devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="646e5-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="646e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="646e5-110">PARAMETERS</span></span>

### <span data-ttu-id="646e5-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="646e5-111">-Name</span></span>
<span data-ttu-id="646e5-112">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="646e5-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="646e5-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="646e5-113">-PassThru</span></span>
<span data-ttu-id="646e5-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="646e5-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="646e5-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="646e5-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="646e5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="646e5-116">-Profile</span></span>
<span data-ttu-id="646e5-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="646e5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="646e5-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="646e5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="646e5-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="646e5-119">-Slot</span></span>
<span data-ttu-id="646e5-120">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="646e5-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="646e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646e5-121">CommonParameters</span></span>
<span data-ttu-id="646e5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="646e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646e5-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646e5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="646e5-124">INPUTS</span></span>

## <span data-ttu-id="646e5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="646e5-125">OUTPUTS</span></span>

## <span data-ttu-id="646e5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="646e5-126">NOTES</span></span>

## <span data-ttu-id="646e5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="646e5-127">RELATED LINKS</span></span>

[<span data-ttu-id="646e5-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="646e5-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="646e5-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="646e5-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="646e5-130">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="646e5-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="646e5-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="646e5-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="646e5-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="646e5-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


