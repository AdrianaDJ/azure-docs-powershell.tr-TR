---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106557"
---
# <span data-ttu-id="c4d1e-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c4d1e-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="c4d1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d1e-103">Varsa, bir sanal makine nesnesinden statik VNet IP adresi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c4d1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4d1e-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4d1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d1e-106">**Get-AzureStaticVNetIP** cmdlet 'i bir sanal makine nesnesinden statik sanal ağ (VNet) IP adresi bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="c4d1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="c4d1e-108">2</span><span class="sxs-lookup"><span data-stu-id="c4d1e-108">1:</span></span>
```

```

## <span data-ttu-id="c4d1e-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4d1e-109">PARAMETERS</span></span>

### <span data-ttu-id="c4d1e-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c4d1e-110">-InformationAction</span></span>
<span data-ttu-id="c4d1e-111">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4d1e-112">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c4d1e-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4d1e-113">'A</span><span class="sxs-lookup"><span data-stu-id="c4d1e-113">Continue</span></span>
- <span data-ttu-id="c4d1e-114">Manıza</span><span class="sxs-lookup"><span data-stu-id="c4d1e-114">Ignore</span></span>
- <span data-ttu-id="c4d1e-115">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="c4d1e-115">Inquire</span></span>
- <span data-ttu-id="c4d1e-116">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="c4d1e-116">SilentlyContinue</span></span>
- <span data-ttu-id="c4d1e-117">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="c4d1e-117">Stop</span></span>
- <span data-ttu-id="c4d1e-118">Biliriz</span><span class="sxs-lookup"><span data-stu-id="c4d1e-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d1e-119">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="c4d1e-119">-InformationVariable</span></span>
<span data-ttu-id="c4d1e-120">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d1e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4d1e-121">-Profile</span></span>
<span data-ttu-id="c4d1e-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4d1e-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4d1e-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c4d1e-124">-VM</span></span>
<span data-ttu-id="c4d1e-125">Kalıcı bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d1e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d1e-126">CommonParameters</span></span>
<span data-ttu-id="c4d1e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4d1e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d1e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d1e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d1e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4d1e-129">INPUTS</span></span>

## <span data-ttu-id="c4d1e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4d1e-130">OUTPUTS</span></span>

## <span data-ttu-id="c4d1e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4d1e-131">NOTES</span></span>

## <span data-ttu-id="c4d1e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4d1e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4d1e-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c4d1e-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


