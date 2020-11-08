---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105651"
---
# <span data-ttu-id="d279d-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d279d-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="d279d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d279d-102">SYNOPSIS</span></span>
<span data-ttu-id="d279d-103">Azure veri disklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="d279d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d279d-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d279d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d279d-105">DESCRIPTION</span></span>
<span data-ttu-id="d279d-106">**Get-AzureDataDisk** cmdlet 'i, bir Azure sanal makinesindeki veri disklerini temsil eden bir nesne alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="d279d-107">Belirli bir veri diski nesnesi almak için, diskin mantıksal birim numarasını (LUN) belirtin.</span><span class="sxs-lookup"><span data-stu-id="d279d-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="d279d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d279d-108">EXAMPLES</span></span>

### <span data-ttu-id="d279d-109">Örnek 1: sanal makine için tüm veri disklerini alma</span><span class="sxs-lookup"><span data-stu-id="d279d-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="d279d-110">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine07 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="d279d-111">Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d279d-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d279d-112">Geçerli cmdlet, bu sanal makinenin tüm veri disklerini alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="d279d-113">Örnek 2: bir vituralvirtual için belirli bir veri diski edinme machinevirtual</span><span class="sxs-lookup"><span data-stu-id="d279d-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="d279d-114">Bu komut, VirtualMachine07 adındaki sanal makineyi ContosoService adındaki hizmette alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="d279d-115">Komut sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d279d-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="d279d-116">Geçerli cmdlet, LUN 2 olan veri diskini alır.</span><span class="sxs-lookup"><span data-stu-id="d279d-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="d279d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d279d-117">PARAMETERS</span></span>

### <span data-ttu-id="d279d-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d279d-118">-InformationAction</span></span>
<span data-ttu-id="d279d-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d279d-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d279d-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d279d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d279d-121">'A</span><span class="sxs-lookup"><span data-stu-id="d279d-121">Continue</span></span>
- <span data-ttu-id="d279d-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="d279d-122">Ignore</span></span>
- <span data-ttu-id="d279d-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d279d-123">Inquire</span></span>
- <span data-ttu-id="d279d-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d279d-124">SilentlyContinue</span></span>
- <span data-ttu-id="d279d-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d279d-125">Stop</span></span>
- <span data-ttu-id="d279d-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d279d-126">Suspend</span></span>

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

### <span data-ttu-id="d279d-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d279d-127">-InformationVariable</span></span>
<span data-ttu-id="d279d-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d279d-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d279d-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="d279d-129">-Lun</span></span>
<span data-ttu-id="d279d-130">Sanal makinedeki veri sürücüsünün LUN öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d279d-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="d279d-131">Geçerli değerler: 0 ile 15 arası.</span><span class="sxs-lookup"><span data-stu-id="d279d-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d279d-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="d279d-132">-Profile</span></span>
<span data-ttu-id="d279d-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d279d-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d279d-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d279d-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d279d-135">-VM</span><span class="sxs-lookup"><span data-stu-id="d279d-135">-VM</span></span>
<span data-ttu-id="d279d-136">Bu cmdlet 'in veri disklerini aldığı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d279d-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="d279d-137">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d279d-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="d279d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d279d-138">CommonParameters</span></span>
<span data-ttu-id="d279d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d279d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d279d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d279d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d279d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d279d-141">INPUTS</span></span>

## <span data-ttu-id="d279d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d279d-142">OUTPUTS</span></span>

## <span data-ttu-id="d279d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d279d-143">NOTES</span></span>

## <span data-ttu-id="d279d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d279d-144">RELATED LINKS</span></span>

[<span data-ttu-id="d279d-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d279d-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="d279d-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d279d-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d279d-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d279d-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="d279d-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d279d-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


