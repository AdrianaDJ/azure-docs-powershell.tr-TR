---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105948"
---
# <span data-ttu-id="4c572-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="4c572-101">Show-AzurePortal</span></span>

## <span data-ttu-id="4c572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c572-102">SYNOPSIS</span></span>
<span data-ttu-id="4c572-103">Azure yönetim portalı 'nı gösterin.</span><span class="sxs-lookup"><span data-stu-id="4c572-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="4c572-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c572-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c572-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c572-105">DESCRIPTION</span></span>
<span data-ttu-id="4c572-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c572-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4c572-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4c572-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4c572-108">**Show-AzurePortal** cmdlet 'ı, Azure yönetim portalını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c572-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="4c572-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c572-109">EXAMPLES</span></span>

### <span data-ttu-id="4c572-110">Örnek 1: Web sitesi hakkındaki bilgileri gösterme</span><span class="sxs-lookup"><span data-stu-id="4c572-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="4c572-111">Bu örnekte, Sitem adlı bir Web sitesi hakkında bilgi gösterilen Azure portalında bir tarayıcı açılır.</span><span class="sxs-lookup"><span data-stu-id="4c572-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="4c572-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c572-112">PARAMETERS</span></span>

### <span data-ttu-id="4c572-113">-Ortam</span><span class="sxs-lookup"><span data-stu-id="4c572-113">-Environment</span></span>
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

### <span data-ttu-id="4c572-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c572-114">-Name</span></span>
<span data-ttu-id="4c572-115">Portalda gösterilecek web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c572-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="4c572-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c572-116">-Profile</span></span>
<span data-ttu-id="4c572-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c572-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c572-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4c572-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c572-119">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4c572-119">-Realm</span></span>
<span data-ttu-id="4c572-120">Azure portalını görüntülerken Federasyon kimlik doğrulaması için kullanılacak kuruluş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c572-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="4c572-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c572-121">CommonParameters</span></span>
<span data-ttu-id="4c572-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c572-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c572-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c572-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c572-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c572-124">INPUTS</span></span>

## <span data-ttu-id="4c572-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c572-125">OUTPUTS</span></span>

## <span data-ttu-id="4c572-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c572-126">NOTES</span></span>

## <span data-ttu-id="4c572-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c572-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c572-128">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4c572-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


