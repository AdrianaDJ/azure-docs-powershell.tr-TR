---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105547"
---
# <span data-ttu-id="11458-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="11458-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="11458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11458-102">SYNOPSIS</span></span>
<span data-ttu-id="11458-103">Kullanılabilir Azure Mağazası eklentilerini alır.</span><span class="sxs-lookup"><span data-stu-id="11458-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="11458-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11458-104">SYNTAX</span></span>

### <span data-ttu-id="11458-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="11458-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="11458-106">GetAddOn</span><span class="sxs-lookup"><span data-stu-id="11458-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11458-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="11458-107">DESCRIPTION</span></span>
<span data-ttu-id="11458-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="11458-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="11458-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="11458-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="11458-110">Azure Mağazası 'ndan satın almak için tüm kullanılabilir eklentileri alır veya geçerli aboneliğin mevcut eklenti örneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="11458-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="11458-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11458-111">EXAMPLES</span></span>

### <span data-ttu-id="11458-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11458-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="11458-113">Bu örnekte, geçerli aboneliğin satın alınan tüm eklenti örnekleri alınır.</span><span class="sxs-lookup"><span data-stu-id="11458-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="11458-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="11458-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="11458-115">Bu örnekte, Azure Mağazası 'ndan Amerika Birleşik Devletleri 'nde satın almak için sağlanan tüm eklentiler alınır.</span><span class="sxs-lookup"><span data-stu-id="11458-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="11458-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="11458-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="11458-117">Bu örnekte, geçerli abonelikteki satın alınan eklenti örneğindeki MyAddOn adlı bir eklenti alınır.</span><span class="sxs-lookup"><span data-stu-id="11458-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="11458-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11458-118">PARAMETERS</span></span>

### <span data-ttu-id="11458-119">-Ülke</span><span class="sxs-lookup"><span data-stu-id="11458-119">-Country</span></span>
<span data-ttu-id="11458-120">Belirtilmişse yalnızca belirtilen ülkedeki Azure Mağazası eklenti örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="11458-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="11458-121">Varsayılan "US" dir.</span><span class="sxs-lookup"><span data-stu-id="11458-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11458-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="11458-122">-ListAvailable</span></span>
<span data-ttu-id="11458-123">Belirtilmişse, Azure Mağazası 'ndan satın almak için kullanılabilir eklentileri alır.</span><span class="sxs-lookup"><span data-stu-id="11458-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11458-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="11458-124">-Name</span></span>
<span data-ttu-id="11458-125">Belirtilen adla eşleşen eklentiyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="11458-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11458-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="11458-126">-Profile</span></span>
<span data-ttu-id="11458-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="11458-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11458-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="11458-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11458-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11458-129">CommonParameters</span></span>
<span data-ttu-id="11458-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11458-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11458-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11458-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11458-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11458-132">INPUTS</span></span>

## <span data-ttu-id="11458-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11458-133">OUTPUTS</span></span>

## <span data-ttu-id="11458-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11458-134">NOTES</span></span>

## <span data-ttu-id="11458-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11458-135">RELATED LINKS</span></span>

[<span data-ttu-id="11458-136">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="11458-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="11458-137">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="11458-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="11458-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="11458-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


