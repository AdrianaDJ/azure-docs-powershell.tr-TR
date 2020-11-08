---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106415"
---
# <span data-ttu-id="74bb3-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="74bb3-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="74bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="74bb3-103">Var olan bir eklenti örneğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="74bb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74bb3-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74bb3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="74bb3-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="74bb3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="74bb3-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="74bb3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="74bb3-108">Bu cmdlet geçerli abonelikten var olan bir eklenti örneğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="74bb3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74bb3-109">EXAMPLES</span></span>

### <span data-ttu-id="74bb3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74bb3-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="74bb3-111">Bu örnekte, yeni bir plan KIMLIĞIYLE birlikte eklenti güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="74bb3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="74bb3-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="74bb3-113">Bu örnek, yeni bir plan kodu ve Promosyon koduyla bir eklentiyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="74bb3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74bb3-114">PARAMETERS</span></span>

### <span data-ttu-id="74bb3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="74bb3-115">-Name</span></span>
<span data-ttu-id="74bb3-116">Eklenti örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="74bb3-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="74bb3-117">-PassThru</span></span>
<span data-ttu-id="74bb3-118">Belirtilmişse, komut başarılı olduysa ve başarısız olursa false döndürür.</span><span class="sxs-lookup"><span data-stu-id="74bb3-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74bb3-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="74bb3-119">-Plan</span></span>
<span data-ttu-id="74bb3-120">Plan KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="74bb3-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="74bb3-121">-Profile</span></span>
<span data-ttu-id="74bb3-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74bb3-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="74bb3-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74bb3-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="74bb3-124">-PromotionCode</span></span>
<span data-ttu-id="74bb3-125">Promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="74bb3-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="74bb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bb3-126">CommonParameters</span></span>
<span data-ttu-id="74bb3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74bb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bb3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74bb3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bb3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74bb3-129">INPUTS</span></span>

## <span data-ttu-id="74bb3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74bb3-130">OUTPUTS</span></span>

## <span data-ttu-id="74bb3-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74bb3-131">NOTES</span></span>

## <span data-ttu-id="74bb3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74bb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="74bb3-133">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="74bb3-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="74bb3-134">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="74bb3-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="74bb3-135">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="74bb3-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


