---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106335"
---
# <span data-ttu-id="58419-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58419-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="58419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58419-102">SYNOPSIS</span></span>
<span data-ttu-id="58419-103">Kullanılabilir Azure Media Services hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="58419-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="58419-104">**Not:** Bu sürüm kullanımdan kalktı, lütfen [daha yeni sürüme](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)bakın.</span><span class="sxs-lookup"><span data-stu-id="58419-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="58419-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58419-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="58419-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="58419-106">DESCRIPTION</span></span>
<span data-ttu-id="58419-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="58419-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="58419-108">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="58419-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="58419-109">Tüm hesapları listelemek için `Get-AzureMediaServicesAccount` cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="58419-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="58419-110">Belirli bir hesap hakkında daha ayrıntılı bilgi edinmek için `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="58419-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="58419-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58419-111">EXAMPLES</span></span>

### <span data-ttu-id="58419-112">Örnek 1: tüm medya hizmetleri hesaplarını listeler</span><span class="sxs-lookup"><span data-stu-id="58419-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="58419-113">Bu komut, kullanılabilir tüm medya hizmetleri hesaplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="58419-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="58419-114">Örnek 2: Medya Hizmetleri hesabı hakkında ayrıntılı bilgi alma</span><span class="sxs-lookup"><span data-stu-id="58419-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="58419-115">Bu komut, bir medya Hizmetleri hesabının özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="58419-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="58419-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58419-116">PARAMETERS</span></span>

### <span data-ttu-id="58419-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="58419-117">-Name</span></span>
<span data-ttu-id="58419-118">Medya Hizmetleri hesap adı.</span><span class="sxs-lookup"><span data-stu-id="58419-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="58419-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="58419-119">-Profile</span></span>
<span data-ttu-id="58419-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58419-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58419-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="58419-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58419-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58419-122">CommonParameters</span></span>
<span data-ttu-id="58419-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58419-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58419-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58419-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58419-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58419-125">INPUTS</span></span>

## <span data-ttu-id="58419-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58419-126">OUTPUTS</span></span>

## <span data-ttu-id="58419-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58419-127">NOTES</span></span>

## <span data-ttu-id="58419-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58419-128">RELATED LINKS</span></span>

[<span data-ttu-id="58419-129">Medya Hizmetleri için Azure PowerShell kullanma</span><span class="sxs-lookup"><span data-stu-id="58419-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


