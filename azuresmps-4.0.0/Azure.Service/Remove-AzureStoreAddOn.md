---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106455"
---
# <span data-ttu-id="3c179-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3c179-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="3c179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c179-102">SYNOPSIS</span></span>
<span data-ttu-id="3c179-103">Var olan bir eklenti örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c179-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="3c179-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c179-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c179-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c179-105">DESCRIPTION</span></span>
<span data-ttu-id="3c179-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3c179-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3c179-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3c179-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3c179-108">Var olan bir eklenti örneğini geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c179-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="3c179-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c179-109">EXAMPLES</span></span>

### <span data-ttu-id="3c179-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c179-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="3c179-111">Bu örnekte, geçerli abonelikteki MyAddOn adındaki bir eklenti kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="3c179-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="3c179-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c179-112">PARAMETERS</span></span>

### <span data-ttu-id="3c179-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c179-113">-Name</span></span>
<span data-ttu-id="3c179-114">Kaldırılacak eklenti örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c179-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="3c179-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c179-115">-PassThru</span></span>
<span data-ttu-id="3c179-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c179-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c179-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3c179-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c179-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c179-118">-Profile</span></span>
<span data-ttu-id="3c179-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c179-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c179-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3c179-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c179-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c179-121">CommonParameters</span></span>
<span data-ttu-id="3c179-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c179-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c179-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c179-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c179-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c179-124">INPUTS</span></span>

## <span data-ttu-id="3c179-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c179-125">OUTPUTS</span></span>

## <span data-ttu-id="3c179-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c179-126">NOTES</span></span>

## <span data-ttu-id="3c179-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c179-127">RELATED LINKS</span></span>

[<span data-ttu-id="3c179-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3c179-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="3c179-129">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3c179-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="3c179-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="3c179-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


