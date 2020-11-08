---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105458"
---
# <span data-ttu-id="764c7-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="764c7-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="764c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="764c7-102">SYNOPSIS</span></span>
<span data-ttu-id="764c7-103">Belirli bir Web sitesi için günlükleri indirir ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="764c7-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="764c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="764c7-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="764c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="764c7-105">DESCRIPTION</span></span>
<span data-ttu-id="764c7-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="764c7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="764c7-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="764c7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="764c7-108">**Save-AzureWebsiteLog** cmdlet 'i belirtilen Web sitesi için günlükleri indirir.</span><span class="sxs-lookup"><span data-stu-id="764c7-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="764c7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="764c7-109">EXAMPLES</span></span>

### <span data-ttu-id="764c7-110">Örnek 1: Web sitesi için günlükleri Indirme ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="764c7-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="764c7-111">Bu örnekte, geçerli dizindeki logs.zip Web sitesi sitem için çalışma zamanı ve dağıtım günlükleri indirilir.</span><span class="sxs-lookup"><span data-stu-id="764c7-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="764c7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="764c7-112">PARAMETERS</span></span>

### <span data-ttu-id="764c7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="764c7-113">-Name</span></span>
<span data-ttu-id="764c7-114">Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="764c7-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="764c7-115">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="764c7-115">-Output</span></span>
<span data-ttu-id="764c7-116">İndirilen dosyanın depolanacağı yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="764c7-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="764c7-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="764c7-117">-PassThru</span></span>
<span data-ttu-id="764c7-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="764c7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="764c7-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="764c7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="764c7-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="764c7-120">-Profile</span></span>
<span data-ttu-id="764c7-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="764c7-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="764c7-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="764c7-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="764c7-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="764c7-123">-Slot</span></span>
<span data-ttu-id="764c7-124">Yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="764c7-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="764c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764c7-125">CommonParameters</span></span>
<span data-ttu-id="764c7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="764c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764c7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764c7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="764c7-128">INPUTS</span></span>

## <span data-ttu-id="764c7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="764c7-129">OUTPUTS</span></span>

## <span data-ttu-id="764c7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="764c7-130">NOTES</span></span>

## <span data-ttu-id="764c7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="764c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="764c7-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="764c7-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


