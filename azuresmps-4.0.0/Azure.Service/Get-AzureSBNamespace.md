---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105613"
---
# <span data-ttu-id="b4531-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="b4531-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="b4531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4531-102">SYNOPSIS</span></span>
<span data-ttu-id="b4531-103">Ad boşluğunu alır.</span><span class="sxs-lookup"><span data-stu-id="b4531-103">Gets the namespace.</span></span>


## <span data-ttu-id="b4531-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4531-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4531-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4531-105">DESCRIPTION</span></span>
<span data-ttu-id="b4531-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b4531-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b4531-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b4531-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b4531-108">**Get-AzureSBNamespace** cmdlet 'i, geçerli abonelikle Ilişkilendirilmiş hizmet veri yolu hizmeti ad alanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4531-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="b4531-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4531-109">EXAMPLES</span></span>

### <span data-ttu-id="b4531-110">Örnek 1: hizmet veri yolu ad alanını alma</span><span class="sxs-lookup"><span data-stu-id="b4531-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="b4531-111">Bu örnekte, geçerli abonelikle ilişkilendirilmiş hizmet veri yolu hizmeti ad alanları alınır.</span><span class="sxs-lookup"><span data-stu-id="b4531-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="b4531-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4531-112">PARAMETERS</span></span>

### <span data-ttu-id="b4531-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4531-113">-Name</span></span>
<span data-ttu-id="b4531-114">Bakılacak hizmet veri yolu ad alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4531-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="b4531-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4531-115">-Profile</span></span>
<span data-ttu-id="b4531-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4531-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4531-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b4531-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4531-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4531-118">CommonParameters</span></span>
<span data-ttu-id="b4531-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4531-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4531-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4531-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4531-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4531-121">INPUTS</span></span>

## <span data-ttu-id="b4531-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4531-122">OUTPUTS</span></span>

## <span data-ttu-id="b4531-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4531-123">NOTES</span></span>

## <span data-ttu-id="b4531-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4531-124">RELATED LINKS</span></span>

[<span data-ttu-id="b4531-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="b4531-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


