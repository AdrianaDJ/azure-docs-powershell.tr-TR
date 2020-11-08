---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105536"
---
# <span data-ttu-id="78a0e-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="78a0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="78a0e-103">Traffic Manager profilinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="78a0e-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="78a0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78a0e-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78a0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="78a0e-106">**Get-AzureTrafficManagerProfile** cmdlet 'ı Microsoft Azure Traffic Manager profilinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="78a0e-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="78a0e-107">*Name* parametresini belirtmezseniz cmdlet, geçerli abonelikteki Traffic Manager profillerini listeler.</span><span class="sxs-lookup"><span data-stu-id="78a0e-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="78a0e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78a0e-108">EXAMPLES</span></span>

### <span data-ttu-id="78a0e-109">Örnek 1: abonelikteki Traffic Manager profillerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="78a0e-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="78a0e-110">Bu komut aboneliğinizdeki Traffic Manager profillerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="78a0e-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="78a0e-111">Örnek 2: Traffic Manager profili alma</span><span class="sxs-lookup"><span data-stu-id="78a0e-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="78a0e-112">Bu komut Myprofıle adlı Traffic Manager profilini alır.</span><span class="sxs-lookup"><span data-stu-id="78a0e-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="78a0e-113">Örnek 3: Traffic Manager profiline uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="78a0e-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="78a0e-114">Bu komut bir Traffic Manager profiline uç nokta ekler ve ardından profili kaydeder.</span><span class="sxs-lookup"><span data-stu-id="78a0e-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="78a0e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78a0e-115">PARAMETERS</span></span>

### <span data-ttu-id="78a0e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="78a0e-116">-Name</span></span>
<span data-ttu-id="78a0e-117">Alınacak Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a0e-117">Specifies the name of the Traffic Manager profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a0e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="78a0e-118">-Profile</span></span>
<span data-ttu-id="78a0e-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="78a0e-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="78a0e-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="78a0e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78a0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a0e-121">CommonParameters</span></span>
<span data-ttu-id="78a0e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78a0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a0e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a0e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a0e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78a0e-124">INPUTS</span></span>

## <span data-ttu-id="78a0e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78a0e-125">OUTPUTS</span></span>

### <span data-ttu-id="78a0e-126">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="78a0e-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="78a0e-127">Bu cmdlet, Traffic Manager profil nesnesi veya nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="78a0e-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="78a0e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78a0e-128">NOTES</span></span>

## <span data-ttu-id="78a0e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78a0e-129">RELATED LINKS</span></span>

[<span data-ttu-id="78a0e-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78a0e-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="78a0e-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="78a0e-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="78a0e-133">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="78a0e-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="78a0e-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78a0e-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


