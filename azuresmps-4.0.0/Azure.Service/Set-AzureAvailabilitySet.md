---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E0590AD4-F67B-48EF-8657-8890A2204CB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 607cd288bcc9c86209a3ae0af569e964205f5cb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106067"
---
# <span data-ttu-id="699e4-101">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="699e4-101">Set-AzureAvailabilitySet</span></span>

## <span data-ttu-id="699e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="699e4-102">SYNOPSIS</span></span>
<span data-ttu-id="699e4-103">Azure sanal makinesindeki kullanılabilirlik kümesinin adını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="699e4-103">Sets the name of the availability set on an Azure virtual machine.</span></span>

## <span data-ttu-id="699e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="699e4-104">SYNTAX</span></span>

```
Set-AzureAvailabilitySet [-AvailabilitySetName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="699e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="699e4-105">DESCRIPTION</span></span>
<span data-ttu-id="699e4-106">**Set-AzureAvailabilitySet** cmdlet 'i, dağıtımdan sonra bir Azure sanal makinesindeki kullanılabilirlik kümesinin adını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="699e4-106">The **Set-AzureAvailabilitySet** cmdlet sets the name of the availability set on an Azure virtual machine after deployment.</span></span>

## <span data-ttu-id="699e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="699e4-107">EXAMPLES</span></span>

### <span data-ttu-id="699e4-108">Örnek 1: kullanılabilirlik kümesinin adını değiştirme</span><span class="sxs-lookup"><span data-stu-id="699e4-108">Example 1: Modify the name of an availability set</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine24" | Set-AzureAvailabilitySet -AvailabilitySetName "AvailabilitySet14" | Update-AzureVM
```

<span data-ttu-id="699e4-109">İlk komut, VirtualMachine07 adındaki sanal makineyi, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette alır.</span><span class="sxs-lookup"><span data-stu-id="699e4-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="699e4-110">Komut, ardışık düzen işlecini kullanarak nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="699e4-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="699e4-111">Bu cmdlet, bu sanal makinenin kullanılabilirlik kümesinin adını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="699e4-111">That cmdlet modifies the name of the availability set for that virtual machine.</span></span>
<span data-ttu-id="699e4-112">Komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="699e4-112">The command updates the virtual machine.</span></span>

## <span data-ttu-id="699e4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="699e4-113">PARAMETERS</span></span>

### <span data-ttu-id="699e4-114">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="699e4-114">-AvailabilitySetName</span></span>
<span data-ttu-id="699e4-115">Sanal makinenin ait olduğu kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="699e4-115">Specifies the name of the availability set to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699e4-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="699e4-116">-InformationAction</span></span>
<span data-ttu-id="699e4-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="699e4-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="699e4-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="699e4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="699e4-119">'A</span><span class="sxs-lookup"><span data-stu-id="699e4-119">Continue</span></span>
- <span data-ttu-id="699e4-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="699e4-120">Ignore</span></span>
- <span data-ttu-id="699e4-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="699e4-121">Inquire</span></span>
- <span data-ttu-id="699e4-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="699e4-122">SilentlyContinue</span></span>
- <span data-ttu-id="699e4-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="699e4-123">Stop</span></span>
- <span data-ttu-id="699e4-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="699e4-124">Suspend</span></span>

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

### <span data-ttu-id="699e4-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="699e4-125">-InformationVariable</span></span>
<span data-ttu-id="699e4-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="699e4-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="699e4-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="699e4-127">-Profile</span></span>
<span data-ttu-id="699e4-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="699e4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="699e4-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="699e4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="699e4-130">-VM</span><span class="sxs-lookup"><span data-stu-id="699e4-130">-VM</span></span>
<span data-ttu-id="699e4-131">Bu cmdlet 'in değiştirdiği sanal makine yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="699e4-131">Specifies the virtual machine configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="699e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699e4-132">CommonParameters</span></span>
<span data-ttu-id="699e4-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="699e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699e4-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699e4-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="699e4-135">INPUTS</span></span>

## <span data-ttu-id="699e4-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="699e4-136">OUTPUTS</span></span>

## <span data-ttu-id="699e4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="699e4-137">NOTES</span></span>

## <span data-ttu-id="699e4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="699e4-138">RELATED LINKS</span></span>

[<span data-ttu-id="699e4-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="699e4-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="699e4-140">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="699e4-140">Remove-AzureAvailabilitySet</span></span>](./Remove-AzureAvailabilitySet.md)


