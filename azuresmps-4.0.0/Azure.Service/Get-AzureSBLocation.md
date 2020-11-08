---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106312"
---
# <span data-ttu-id="c5945-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="c5945-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="c5945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5945-102">SYNOPSIS</span></span>
<span data-ttu-id="c5945-103">Hizmet veri yolunun konumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c5945-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="c5945-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5945-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5945-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5945-105">DESCRIPTION</span></span>
<span data-ttu-id="c5945-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c5945-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5945-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c5945-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c5945-108">**Get-AzureSBLocation** cmdlet 'ı, hizmet veri yolunun kullanılabileceği konumları döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5945-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="c5945-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5945-109">EXAMPLES</span></span>

### <span data-ttu-id="c5945-110">Örnek 1: hizmet veri yolu konumunu alma</span><span class="sxs-lookup"><span data-stu-id="c5945-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="c5945-111">Bu örnekte, hizmet veri yolunun konumu alınır.</span><span class="sxs-lookup"><span data-stu-id="c5945-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="c5945-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5945-112">PARAMETERS</span></span>

### <span data-ttu-id="c5945-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5945-113">-Profile</span></span>
<span data-ttu-id="c5945-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5945-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5945-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c5945-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5945-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5945-116">CommonParameters</span></span>
<span data-ttu-id="c5945-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5945-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5945-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5945-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5945-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5945-119">INPUTS</span></span>

## <span data-ttu-id="c5945-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5945-120">OUTPUTS</span></span>

## <span data-ttu-id="c5945-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5945-121">NOTES</span></span>

## <span data-ttu-id="c5945-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5945-122">RELATED LINKS</span></span>

[<span data-ttu-id="c5945-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="c5945-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


