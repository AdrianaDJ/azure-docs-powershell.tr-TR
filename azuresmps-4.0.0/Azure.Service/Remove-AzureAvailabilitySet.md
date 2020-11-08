---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106168"
---
# <span data-ttu-id="8eba9-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8eba9-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="8eba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eba9-102">SYNOPSIS</span></span>
<span data-ttu-id="8eba9-103">Bir Azure sanal makinesinden kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8eba9-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="8eba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8eba9-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8eba9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8eba9-105">DESCRIPTION</span></span>
<span data-ttu-id="8eba9-106">**Remove-AzureAvailabilitySet** cmdlet 'i, bir Azure sanal makinesinden kullanılabilirlik kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8eba9-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="8eba9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8eba9-107">EXAMPLES</span></span>

### <span data-ttu-id="8eba9-108">2</span><span class="sxs-lookup"><span data-stu-id="8eba9-108">1:</span></span>
```

```

## <span data-ttu-id="8eba9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8eba9-109">PARAMETERS</span></span>

### <span data-ttu-id="8eba9-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8eba9-110">-InformationAction</span></span>
<span data-ttu-id="8eba9-111">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8eba9-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8eba9-112">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8eba9-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8eba9-113">'A</span><span class="sxs-lookup"><span data-stu-id="8eba9-113">Continue</span></span>
- <span data-ttu-id="8eba9-114">Manıza</span><span class="sxs-lookup"><span data-stu-id="8eba9-114">Ignore</span></span>
- <span data-ttu-id="8eba9-115">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="8eba9-115">Inquire</span></span>
- <span data-ttu-id="8eba9-116">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="8eba9-116">SilentlyContinue</span></span>
- <span data-ttu-id="8eba9-117">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="8eba9-117">Stop</span></span>
- <span data-ttu-id="8eba9-118">Biliriz</span><span class="sxs-lookup"><span data-stu-id="8eba9-118">Suspend</span></span>

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

### <span data-ttu-id="8eba9-119">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="8eba9-119">-InformationVariable</span></span>
<span data-ttu-id="8eba9-120">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8eba9-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8eba9-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="8eba9-121">-Profile</span></span>
<span data-ttu-id="8eba9-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8eba9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8eba9-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8eba9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8eba9-124">-VM</span><span class="sxs-lookup"><span data-stu-id="8eba9-124">-VM</span></span>
<span data-ttu-id="8eba9-125">Bu cmdlet 'in bir kullanılabilirlik kümesini kaldırdığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8eba9-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

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

### <span data-ttu-id="8eba9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eba9-126">CommonParameters</span></span>
<span data-ttu-id="8eba9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8eba9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eba9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eba9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eba9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8eba9-129">INPUTS</span></span>

## <span data-ttu-id="8eba9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8eba9-130">OUTPUTS</span></span>

## <span data-ttu-id="8eba9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8eba9-131">NOTES</span></span>

## <span data-ttu-id="8eba9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8eba9-132">RELATED LINKS</span></span>

[<span data-ttu-id="8eba9-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8eba9-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


