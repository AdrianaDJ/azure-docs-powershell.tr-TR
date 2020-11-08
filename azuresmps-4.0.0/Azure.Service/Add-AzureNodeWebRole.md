---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106392"
---
# <span data-ttu-id="0f02e-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="0f02e-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="0f02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f02e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f02e-103">Node.js uygulaması için gerekli dosyaları ve klasörleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f02e-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="0f02e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f02e-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f02e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f02e-105">DESCRIPTION</span></span>
<span data-ttu-id="0f02e-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0f02e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0f02e-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0f02e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0f02e-108">**Add-AzureNodeWebRole** , bazen, bir Node.js uygulamasının IIS aracılığıyla bulutta barındırılması için scafkatlama olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="0f02e-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="0f02e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f02e-109">EXAMPLES</span></span>

### <span data-ttu-id="0f02e-110">Örnek 1: tek örnekli web rolü</span><span class="sxs-lookup"><span data-stu-id="0f02e-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="0f02e-111">Bu örnek, **MyWebRole** adındaki tek bir Web rolü için geçerli uygulamaya scafkatlama ekler.</span><span class="sxs-lookup"><span data-stu-id="0f02e-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="0f02e-112">Örnek 2: birden çok örnek Web rolü</span><span class="sxs-lookup"><span data-stu-id="0f02e-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="0f02e-113">Bu örnek, **MyWebRole** adlı yeni bir Web rolü için, rol örneği sayısı 2 olan bir rol örneği ekler.</span><span class="sxs-lookup"><span data-stu-id="0f02e-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="0f02e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f02e-114">PARAMETERS</span></span>

### <span data-ttu-id="0f02e-115">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="0f02e-115">-Instances</span></span>
<span data-ttu-id="0f02e-116">Bu web rolü için rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f02e-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="0f02e-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="0f02e-117">The default is 1.</span></span>

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

### <span data-ttu-id="0f02e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f02e-118">-Name</span></span>
<span data-ttu-id="0f02e-119">Web rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f02e-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="0f02e-120">Ayrıca, Web rolünde barındırılan node.js uygulamasının scaflesi içeren dizinin adını da belirler.</span><span class="sxs-lookup"><span data-stu-id="0f02e-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="0f02e-121">Varsayılan WebRole # ' dır, burada # hizmette Web rollerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f02e-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="0f02e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f02e-122">-Profile</span></span>
<span data-ttu-id="0f02e-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f02e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f02e-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0f02e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f02e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f02e-125">CommonParameters</span></span>
<span data-ttu-id="0f02e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f02e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f02e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f02e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f02e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f02e-128">INPUTS</span></span>

## <span data-ttu-id="0f02e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f02e-129">OUTPUTS</span></span>

## <span data-ttu-id="0f02e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f02e-130">NOTES</span></span>

## <span data-ttu-id="0f02e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f02e-131">RELATED LINKS</span></span>

[<span data-ttu-id="0f02e-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="0f02e-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="0f02e-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="0f02e-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


