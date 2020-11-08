---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106218"
---
# <span data-ttu-id="864e5-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="864e5-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="864e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="864e5-102">SYNOPSIS</span></span>
<span data-ttu-id="864e5-103">Yeni bir hizmet için gerekli dosyaları ve yapılandırmayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="864e5-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="864e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="864e5-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="864e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="864e5-105">DESCRIPTION</span></span>
<span data-ttu-id="864e5-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="864e5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="864e5-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="864e5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="864e5-108">**New-AzureServiceProject** cmdlet 'i geçerli dizindeki yeni bir Azure hizmeti için gerekli dosyaları ve yapılandırmayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="864e5-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="864e5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="864e5-109">EXAMPLES</span></span>

### <span data-ttu-id="864e5-110">Örnek 1: hizmet için scafkatlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="864e5-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="864e5-111">Bu örnek, geçerli dizindeki MyService1 adlı yeni bir Azure hizmeti için scafkatlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="864e5-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="864e5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="864e5-112">PARAMETERS</span></span>

### <span data-ttu-id="864e5-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="864e5-113">-Profile</span></span>
<span data-ttu-id="864e5-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="864e5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="864e5-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="864e5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="864e5-116">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="864e5-116">-ServiceName</span></span>
<span data-ttu-id="864e5-117">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="864e5-117">Specifies the name of the service.</span></span>
<span data-ttu-id="864e5-118">Hizmetinizin ana bilgisayar adının ilk bölümünü (örneğin, name.cloudapp.net) ve hizmetinizi içerecek dizini belirler.</span><span class="sxs-lookup"><span data-stu-id="864e5-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="864e5-119">Ad yalnızca harf, rakam ve tire karakterini (-) içerebilir.</span><span class="sxs-lookup"><span data-stu-id="864e5-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="864e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864e5-120">CommonParameters</span></span>
<span data-ttu-id="864e5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="864e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864e5-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864e5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864e5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="864e5-123">INPUTS</span></span>

## <span data-ttu-id="864e5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="864e5-124">OUTPUTS</span></span>

## <span data-ttu-id="864e5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="864e5-125">NOTES</span></span>

## <span data-ttu-id="864e5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="864e5-126">RELATED LINKS</span></span>

[<span data-ttu-id="864e5-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="864e5-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="864e5-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="864e5-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="864e5-129">Yayımla-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="864e5-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="864e5-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="864e5-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="864e5-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="864e5-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


