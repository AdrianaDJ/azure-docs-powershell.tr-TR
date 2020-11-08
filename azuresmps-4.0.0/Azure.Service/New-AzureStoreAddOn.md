---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106201"
---
# <span data-ttu-id="da171-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="da171-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="da171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da171-102">SYNOPSIS</span></span>
<span data-ttu-id="da171-103">Yeni bir eklenti örneği satın.</span><span class="sxs-lookup"><span data-stu-id="da171-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="da171-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da171-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da171-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da171-105">DESCRIPTION</span></span>
<span data-ttu-id="da171-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="da171-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="da171-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="da171-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="da171-108">Azure Mağazası 'ndan yeni bir eklenti örneği satın alım.</span><span class="sxs-lookup"><span data-stu-id="da171-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="da171-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da171-109">EXAMPLES</span></span>

### <span data-ttu-id="da171-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="da171-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="da171-111">Bu örnek, Batı US konumunda bir PlanID ile birlikte MyAddOn adlı bir eklenti satın alıyor.</span><span class="sxs-lookup"><span data-stu-id="da171-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="da171-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="da171-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="da171-113">Bu örnekte, bir eklenti satın almak için bir promosyon kodu kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="da171-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="da171-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da171-114">PARAMETERS</span></span>

### <span data-ttu-id="da171-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="da171-115">-AddOn</span></span>
<span data-ttu-id="da171-116">Eklenti KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-116">Specifies the add-on ID.</span></span>

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

### <span data-ttu-id="da171-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="da171-117">-Location</span></span>
<span data-ttu-id="da171-118">Eklenti örneği konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-118">Specifies the add-on instance location.</span></span>

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

### <span data-ttu-id="da171-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="da171-119">-Name</span></span>
<span data-ttu-id="da171-120">Eklenti örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-120">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="da171-121">-Plan</span><span class="sxs-lookup"><span data-stu-id="da171-121">-Plan</span></span>
<span data-ttu-id="da171-122">Plan KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-122">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="da171-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="da171-123">-Profile</span></span>
<span data-ttu-id="da171-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da171-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="da171-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da171-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="da171-126">-PromotionCode</span></span>
<span data-ttu-id="da171-127">Satınalmaya uygulanacak promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da171-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="da171-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da171-128">CommonParameters</span></span>
<span data-ttu-id="da171-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da171-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da171-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da171-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da171-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da171-131">INPUTS</span></span>

## <span data-ttu-id="da171-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da171-132">OUTPUTS</span></span>

## <span data-ttu-id="da171-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da171-133">NOTES</span></span>

## <span data-ttu-id="da171-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da171-134">RELATED LINKS</span></span>

[<span data-ttu-id="da171-135">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="da171-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="da171-136">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="da171-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="da171-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="da171-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


