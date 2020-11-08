---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106390"
---
# <span data-ttu-id="2576e-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="2576e-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="2576e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2576e-102">SYNOPSIS</span></span>
<span data-ttu-id="2576e-103">Bir PHP uygulaması için gerekli dosyaları ve yapılandırmayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2576e-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="2576e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2576e-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2576e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2576e-105">DESCRIPTION</span></span>
<span data-ttu-id="2576e-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2576e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2576e-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2576e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2576e-108">**Add-AzurePHPWebRole** cmdlet 'i, bazen, IIS aracılığıyla Azure 'da BARıNDıRıLAN bir php uygulaması için, dosya ve yapılandırmayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2576e-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="2576e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2576e-109">EXAMPLES</span></span>

### <span data-ttu-id="2576e-110">Örnek 1: varsayılan değerleri kullanarak Web rolü ekleme</span><span class="sxs-lookup"><span data-stu-id="2576e-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="2576e-111">Bu örnek, 1 örneğiyle "WebRole1" adlı hizmetin varsayılan değerlerini kullanarak yeni web rolü için gerekli dosyaları ve yapılandırmayı ekler.</span><span class="sxs-lookup"><span data-stu-id="2576e-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="2576e-112">Örnek 2: birden çok örneğe sahip web rolü ekleme</span><span class="sxs-lookup"><span data-stu-id="2576e-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="2576e-113">Bu örnek, "MyWebRole" adını ve 2 ' nin rol örneği sayısını kullanarak, geçerli uygulamaya yeni bir Web rolü için gerekli dosyaları ve yapılandırmayı ekler.</span><span class="sxs-lookup"><span data-stu-id="2576e-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="2576e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2576e-114">PARAMETERS</span></span>

### <span data-ttu-id="2576e-115">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="2576e-115">-Instances</span></span>
<span data-ttu-id="2576e-116">Bu web rolü için rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2576e-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="2576e-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="2576e-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2576e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2576e-118">-Name</span></span>
<span data-ttu-id="2576e-119">Web rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2576e-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="2576e-120">Ad, PHP uygulaması için gerekli dosyaları ve yapılandırmayı içeren dizinin adını belirler.</span><span class="sxs-lookup"><span data-stu-id="2576e-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="2576e-121">Varsayılan WebRole # ' dır; burada #, hizmetin Web rollerinin sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="2576e-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2576e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2576e-122">-Profile</span></span>
<span data-ttu-id="2576e-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2576e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2576e-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2576e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2576e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2576e-125">CommonParameters</span></span>
<span data-ttu-id="2576e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2576e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2576e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2576e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2576e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2576e-128">INPUTS</span></span>

## <span data-ttu-id="2576e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2576e-129">OUTPUTS</span></span>

## <span data-ttu-id="2576e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2576e-130">NOTES</span></span>

## <span data-ttu-id="2576e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2576e-131">RELATED LINKS</span></span>

[<span data-ttu-id="2576e-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="2576e-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="2576e-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="2576e-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


