---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105711"
---
# <span data-ttu-id="1753d-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="1753d-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="1753d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1753d-102">SYNOPSIS</span></span>
<span data-ttu-id="1753d-103">Web çalışanı rolü ekler.</span><span class="sxs-lookup"><span data-stu-id="1753d-103">Adds a web worker role.</span></span>

## <span data-ttu-id="1753d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1753d-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1753d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1753d-105">DESCRIPTION</span></span>
<span data-ttu-id="1753d-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1753d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1753d-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1753d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1753d-108">**Add-AzureWebRole** cmdlet 'i Web çalışanı rolü ekler.</span><span class="sxs-lookup"><span data-stu-id="1753d-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="1753d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1753d-109">EXAMPLES</span></span>

### <span data-ttu-id="1753d-110">Örnek 1: varsayılan rol ekleme</span><span class="sxs-lookup"><span data-stu-id="1753d-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="1753d-111">Bu komut, ad olarak Webrole1 varsayılan yapılandırmasına sahip web rolü ekler ve tek bir örnek.</span><span class="sxs-lookup"><span data-stu-id="1753d-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="1753d-112">Örnek 2: adı olan bir rol ekleme</span><span class="sxs-lookup"><span data-stu-id="1753d-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="1753d-113">Bu komut, geçerli uygulamaya MyWebRole adında tek bir Web rolü ekler.</span><span class="sxs-lookup"><span data-stu-id="1753d-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="1753d-114">Örnek 3: ad ve örnek sayısına sahip bir rol ekleme</span><span class="sxs-lookup"><span data-stu-id="1753d-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="1753d-115">Bu komut, geçerli uygulamaya MyWebRole adlı bir Web rolü ekler.</span><span class="sxs-lookup"><span data-stu-id="1753d-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="1753d-116">Cmdlet 'in rol örneği sayısı 2 ' dir.</span><span class="sxs-lookup"><span data-stu-id="1753d-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="1753d-117">Örnek 4: ad ve şablon içeren bir rol ekleme</span><span class="sxs-lookup"><span data-stu-id="1753d-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="1753d-118">Bu komut, geçerli uygulamaya MyWebRole adında tek bir Web rolü ekler.</span><span class="sxs-lookup"><span data-stu-id="1753d-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="1753d-119">Komut, scafkatlama şablonu olarak MyWebTemplateFolder adlı bir klasör belirtir.</span><span class="sxs-lookup"><span data-stu-id="1753d-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="1753d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1753d-120">PARAMETERS</span></span>

### <span data-ttu-id="1753d-121">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="1753d-121">-Instances</span></span>
<span data-ttu-id="1753d-122">Örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1753d-122">Specifies the number of instances.</span></span>

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

### <span data-ttu-id="1753d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1753d-123">-Name</span></span>
<span data-ttu-id="1753d-124">Web rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1753d-124">Specifies the name of the web role.</span></span>

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

### <span data-ttu-id="1753d-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="1753d-125">-Profile</span></span>
<span data-ttu-id="1753d-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1753d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1753d-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1753d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1753d-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="1753d-128">-TemplateFolder</span></span>
<span data-ttu-id="1753d-129">Şablon klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1753d-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="1753d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1753d-130">CommonParameters</span></span>
<span data-ttu-id="1753d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1753d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1753d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1753d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1753d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1753d-133">INPUTS</span></span>

## <span data-ttu-id="1753d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1753d-134">OUTPUTS</span></span>

## <span data-ttu-id="1753d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1753d-135">NOTES</span></span>

## <span data-ttu-id="1753d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1753d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1753d-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="1753d-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="1753d-138">Yeni-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="1753d-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


