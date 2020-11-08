---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105935"
---
# <span data-ttu-id="81b71-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="81b71-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="81b71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b71-102">SYNOPSIS</span></span>
<span data-ttu-id="81b71-103">Bir etki alanı adının Traffic Manager profili olarak kullanılıp kullanılmayacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="81b71-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="81b71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81b71-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="81b71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81b71-105">DESCRIPTION</span></span>
<span data-ttu-id="81b71-106">**Test-AzureTrafficManagerDomainName** cmdlet 'i bir etki alanı adının Microsoft Azure Traffic Manager profili olarak kullanılıp kullanılmayacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="81b71-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="81b71-107">Etki alanı adı kullanılabiliyorsa, bu cmdlet $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="81b71-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="81b71-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81b71-108">EXAMPLES</span></span>

### <span data-ttu-id="81b71-109">Örnek 1: etki alanı adının kullanılabilir olup olmadığını denetleme</span><span class="sxs-lookup"><span data-stu-id="81b71-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="81b71-110">Bu komut, ContosoApp.trafficmanager.net etki alanı adı 'nın bir Traffic Manager profili olarak kullanılabildiğini denetler.</span><span class="sxs-lookup"><span data-stu-id="81b71-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="81b71-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81b71-111">PARAMETERS</span></span>

### <span data-ttu-id="81b71-112">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="81b71-112">-DomainName</span></span>
<span data-ttu-id="81b71-113">Sınanacak etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81b71-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="81b71-114">Aşağıdaki dizeyi eklemelisiniz:</span><span class="sxs-lookup"><span data-stu-id="81b71-114">You must include the following string:</span></span> 

<span data-ttu-id="81b71-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="81b71-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b71-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="81b71-116">-Profile</span></span>
<span data-ttu-id="81b71-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81b71-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="81b71-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="81b71-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81b71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b71-119">CommonParameters</span></span>
<span data-ttu-id="81b71-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81b71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b71-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b71-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b71-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81b71-122">INPUTS</span></span>

## <span data-ttu-id="81b71-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81b71-123">OUTPUTS</span></span>

### <span data-ttu-id="81b71-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81b71-124">System.Boolean</span></span>
<span data-ttu-id="81b71-125">Bu cmdlet $True veya $False oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81b71-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="81b71-126">Etki alanı adı kullanılabiliyorsa, bu cmdlet $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="81b71-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="81b71-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81b71-127">NOTES</span></span>

## <span data-ttu-id="81b71-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81b71-128">RELATED LINKS</span></span>

