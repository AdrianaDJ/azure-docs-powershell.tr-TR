---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106506"
---
# <span data-ttu-id="e7568-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="e7568-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="e7568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7568-102">SYNOPSIS</span></span>
<span data-ttu-id="e7568-103">Belirtilen Web sitesi için günlükleri alır.</span><span class="sxs-lookup"><span data-stu-id="e7568-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="e7568-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7568-104">SYNTAX</span></span>

### <span data-ttu-id="e7568-105">Dolgusunu</span><span class="sxs-lookup"><span data-stu-id="e7568-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e7568-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="e7568-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7568-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7568-107">DESCRIPTION</span></span>
<span data-ttu-id="e7568-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e7568-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e7568-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e7568-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e7568-110">Belirtilen Web sitesi için günlük alır.</span><span class="sxs-lookup"><span data-stu-id="e7568-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="e7568-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7568-111">EXAMPLES</span></span>

### <span data-ttu-id="e7568-112">Örnek 1: günlük akışını başlatma</span><span class="sxs-lookup"><span data-stu-id="e7568-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="e7568-113">Bu örnek, tüm uygulama günlükleri için günlük akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="e7568-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="e7568-114">Örnek 2: http günlükleri için günlük akışını başlatma</span><span class="sxs-lookup"><span data-stu-id="e7568-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="e7568-115">Bu örnek http günlükleri için günlük akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="e7568-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="e7568-116">Örnek 3: hata günlükleri için günlük akışını başlatma</span><span class="sxs-lookup"><span data-stu-id="e7568-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="e7568-117">Bu örnek yalnızca akış akışını ve yalnızca hata günlüklerini göstermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="e7568-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="e7568-118">Örnek 4: kullanılabilir günlükleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e7568-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="e7568-119">Bu örnek, Web sitesindeki kullanılabilir tüm günlük yollarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e7568-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="e7568-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7568-120">PARAMETERS</span></span>

### <span data-ttu-id="e7568-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="e7568-121">-ListPath</span></span>
<span data-ttu-id="e7568-122">Günlük yollarının listeedilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7568-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7568-123">-İleti</span><span class="sxs-lookup"><span data-stu-id="e7568-123">-Message</span></span>
<span data-ttu-id="e7568-124">Günlük iletisini filtrelemek için kullanılacak bir dize belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7568-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="e7568-125">Yalnızca bu dizeyi içeren Günlükler alınır.</span><span class="sxs-lookup"><span data-stu-id="e7568-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7568-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7568-126">-Name</span></span>
<span data-ttu-id="e7568-127">Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e7568-127">The name of the website.</span></span>

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

### <span data-ttu-id="e7568-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="e7568-128">-Path</span></span>
<span data-ttu-id="e7568-129">Günlüğün alınacağı yol.</span><span class="sxs-lookup"><span data-stu-id="e7568-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="e7568-130">Varsayılan olarak bu, tüm yolları içermek anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e7568-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7568-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7568-131">-Profile</span></span>
<span data-ttu-id="e7568-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7568-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7568-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e7568-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7568-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="e7568-134">-Slot</span></span>
<span data-ttu-id="e7568-135">Yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7568-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="e7568-136">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="e7568-136">-Tail</span></span>
<span data-ttu-id="e7568-137">Günlüklerin kaydedilip kaydedilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7568-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7568-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7568-138">CommonParameters</span></span>
<span data-ttu-id="e7568-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7568-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7568-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7568-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7568-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7568-141">INPUTS</span></span>

## <span data-ttu-id="e7568-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7568-142">OUTPUTS</span></span>

## <span data-ttu-id="e7568-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7568-143">NOTES</span></span>

## <span data-ttu-id="e7568-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7568-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7568-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7568-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e7568-146">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7568-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e7568-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7568-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e7568-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7568-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


