---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106166"
---
# <span data-ttu-id="26953-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="26953-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="26953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26953-102">SYNOPSIS</span></span>
<span data-ttu-id="26953-103">Azure sanal makinesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26953-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="26953-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26953-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="26953-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26953-105">DESCRIPTION</span></span>
<span data-ttu-id="26953-106">**Remove-AzureDataDisk** cmdlet 'i Azure sanal makinesinden veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26953-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="26953-107">Varsayılan olarak, bu cmdlet veri diski blob 'unu depolama hesabından kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="26953-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="26953-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26953-108">EXAMPLES</span></span>

### <span data-ttu-id="26953-109">Örnek 1: veri diskini kaldırma</span><span class="sxs-lookup"><span data-stu-id="26953-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="26953-110">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine07 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="26953-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="26953-111">Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="26953-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26953-112">Geçerli cmdlet, LUN 0 olan veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26953-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="26953-113">Örnek 2: veri diskini ve sanal sabit disk dosyasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="26953-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="26953-114">Bu komut, VirtualMachine07 adındaki sanal makineyi ContosoService adındaki hizmette alır.</span><span class="sxs-lookup"><span data-stu-id="26953-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="26953-115">Komut sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="26953-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="26953-116">Geçerli cmdlet, LUN 0 olan veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26953-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="26953-117">Komut, *Deletevhd* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="26953-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="26953-118">Bu nedenle temel sanal sabit disk de silinir.</span><span class="sxs-lookup"><span data-stu-id="26953-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="26953-119">Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26953-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="26953-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26953-120">PARAMETERS</span></span>

### <span data-ttu-id="26953-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="26953-121">-DeleteVHD</span></span>
<span data-ttu-id="26953-122">Bu cmdlet 'in veri diskini ve sanal sabit diski (VHD) blob depolamadan kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26953-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26953-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="26953-123">-InformationAction</span></span>
<span data-ttu-id="26953-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26953-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="26953-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="26953-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26953-126">'A</span><span class="sxs-lookup"><span data-stu-id="26953-126">Continue</span></span>
- <span data-ttu-id="26953-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="26953-127">Ignore</span></span>
- <span data-ttu-id="26953-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="26953-128">Inquire</span></span>
- <span data-ttu-id="26953-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="26953-129">SilentlyContinue</span></span>
- <span data-ttu-id="26953-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="26953-130">Stop</span></span>
- <span data-ttu-id="26953-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="26953-131">Suspend</span></span>

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

### <span data-ttu-id="26953-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="26953-132">-InformationVariable</span></span>
<span data-ttu-id="26953-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="26953-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="26953-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="26953-134">-LUN</span></span>
<span data-ttu-id="26953-135">Sanal makinedeki veri sürücüsünün mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="26953-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="26953-136">Geçerli değerler: 0 ile 15 arası.</span><span class="sxs-lookup"><span data-stu-id="26953-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26953-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="26953-137">-Profile</span></span>
<span data-ttu-id="26953-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26953-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26953-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="26953-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26953-140">-VM</span><span class="sxs-lookup"><span data-stu-id="26953-140">-VM</span></span>
<span data-ttu-id="26953-141">Veri diskine eklenmiş olan sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26953-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="26953-142">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="26953-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="26953-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26953-143">CommonParameters</span></span>
<span data-ttu-id="26953-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26953-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26953-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26953-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26953-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26953-146">INPUTS</span></span>

## <span data-ttu-id="26953-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26953-147">OUTPUTS</span></span>

## <span data-ttu-id="26953-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26953-148">NOTES</span></span>

## <span data-ttu-id="26953-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26953-149">RELATED LINKS</span></span>

[<span data-ttu-id="26953-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="26953-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="26953-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="26953-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="26953-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="26953-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="26953-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="26953-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="26953-154">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="26953-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


