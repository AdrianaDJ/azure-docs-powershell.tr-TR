---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106512"
---
# <span data-ttu-id="2bbf0-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="2bbf0-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="2bbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbf0-103">Geçerli abonelikteki Azure Web barındırma planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="2bbf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bbf0-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bbf0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="2bbf0-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2bbf0-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2bbf0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2bbf0-108">**Get-AzureWebHostingPlan** cmdlet 'i geçerli abonelikteki Azure Web barındırma planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="2bbf0-109">Varsayılan olarak **Get-AzureWebHostingPlan** , geçerli abonelikteki tüm Azure barındırma planlarını alır ve planlar hakkında temel bilgiler sağlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="2bbf0-110">*Web alanı* ve *ad* parametrelerini kullandığınızda **Get-AzureWebHostingPlan** , belirli bir barındırma planı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="2bbf0-111">Geçerli aboneliği bulmak için **Get-Azuyeniden gönderme scripscripts** cmdlet 'inin *Current* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="2bbf0-112">Geçerli aboneliği değiştirmek için, **Select-azuyeniden komut** dosyası cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="2bbf0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bbf0-113">EXAMPLES</span></span>

### <span data-ttu-id="2bbf0-114">Örnek 1: abonelikteki tüm Web barındırma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="2bbf0-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="2bbf0-115">Bu komut, geçerli abonelikteki tüm Azure Web barındırma planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="2bbf0-116">Örnek 2: bir abonelikte belirli bir Web barındırma planı alma</span><span class="sxs-lookup"><span data-stu-id="2bbf0-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="2bbf0-117">Bu komut, geçerli abonelikteki westeuropewebspace adındaki Web alanında Default0 adlı web barındırma planını alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="2bbf0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bbf0-118">PARAMETERS</span></span>

### <span data-ttu-id="2bbf0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bbf0-119">-Name</span></span>
<span data-ttu-id="2bbf0-120">Abonelikteki bir planın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="2bbf0-121">Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm planları alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="2bbf0-122">Bu parametre joker karakterleri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-122">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="2bbf0-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="2bbf0-123">-Profile</span></span>
<span data-ttu-id="2bbf0-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bbf0-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2bbf0-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="2bbf0-126">-WebSpaceName</span></span>
<span data-ttu-id="2bbf0-127">Abonelikteki bir Web sayfasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="2bbf0-128">Varsayılan olarak, bu cmdlet belirtilen Web alanındaki tüm Web sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="2bbf0-129">Bu parametre joker karakterleri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bbf0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbf0-130">CommonParameters</span></span>
<span data-ttu-id="2bbf0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbf0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bbf0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbf0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bbf0-133">INPUTS</span></span>

###  
<span data-ttu-id="2bbf0-134">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2bbf0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bbf0-135">OUTPUTS</span></span>

### <span data-ttu-id="2bbf0-136">Microsoft. Windowsazde. Commands. Utilities. WebEntities. Services. WebEntities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="2bbf0-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="2bbf0-137">Varsayılan olarak **Get-AzureWebHostingPlan** , **webhostingplan** nesnelerinin dizisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="2bbf0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bbf0-138">NOTES</span></span>

## <span data-ttu-id="2bbf0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bbf0-139">RELATED LINKS</span></span>

