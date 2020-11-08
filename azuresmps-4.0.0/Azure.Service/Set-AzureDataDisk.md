---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106066"
---
# <span data-ttu-id="63e54-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="63e54-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="63e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e54-102">SYNOPSIS</span></span>
<span data-ttu-id="63e54-103">Azure sanal makinesinde varolan bir veri diskinin ana bilgisayarını önbelleğe almasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="63e54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63e54-104">SYNTAX</span></span>

### <span data-ttu-id="63e54-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="63e54-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="63e54-106">Yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="63e54-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="63e54-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="63e54-107">DESCRIPTION</span></span>
<span data-ttu-id="63e54-108">**Set-AzureDataDisk** cmdlet 'ı, Azure sanal makinesindeki mevcut bir veri diskinin önbellek özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="63e54-109">Hangi veri diskinin mantıksal birim numarasıyla (LUN) güncelleştirileceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="63e54-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="63e54-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63e54-110">EXAMPLES</span></span>

### <span data-ttu-id="63e54-111">Örnek 1: veri diskinin önbelleğe alınmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="63e54-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="63e54-112">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adlı hizmette çalışan sanal makineleri alır.</span><span class="sxs-lookup"><span data-stu-id="63e54-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="63e54-113">Komut, ardışık düzen işlecini kullanarak bunları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="63e54-114">Bu cmdlet, VirtualMachine07 adındaki sanal makinenin LUN 2 ' deki veri diskini ReadOnly Host önbelleğe almayı kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="63e54-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="63e54-115">Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="63e54-116">Örnek 2: sanal makinedeki tüm veri disklerinin ana bilgisayar önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="63e54-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="63e54-117">Bu komut, ContosoService bulut hizmetinde VirtualMachine07 adındaki sanal makine için bir nesne alır.</span><span class="sxs-lookup"><span data-stu-id="63e54-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="63e54-118">Komut bu sanal makinenin veri disklerini alan **Get-AzureDataDisk** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="63e54-119">Geçerli cmdlet, her veri disklerinin ana bilgisayar önbellekleme modunu ReadWrite olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="63e54-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="63e54-120">Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="63e54-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63e54-121">PARAMETERS</span></span>

### <span data-ttu-id="63e54-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="63e54-122">-DiskName</span></span>
<span data-ttu-id="63e54-123">Bu cmdlet 'in değiştirdiği veri diski yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e54-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="63e54-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="63e54-125">Disk önbelleğe alma, diskler 4 ve üstü için desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="63e54-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="63e54-126">VM 'inize birden çok disk eklenirse, 4 ' ten küçük olan her disk önbelleğe almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="63e54-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="63e54-127">Bir Azure diskinin önbellek ayarını değiştirmek, hedef diski ayırır ve yeniden iliştirir.</span><span class="sxs-lookup"><span data-stu-id="63e54-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="63e54-128">İşletim sistemi diski ise VM yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="63e54-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="63e54-129">Disk önbelleği ayarını değiştirmeden önce bu durdurmadan etkilenebilecek tüm uygulamaları/hizmetleri durdurun.</span><span class="sxs-lookup"><span data-stu-id="63e54-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="63e54-130">Bu önerilerin olmaması verilerin bozulmasına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="63e54-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="63e54-131">Diskin ana bilgisayar düzeyi önbelleğe alma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="63e54-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="63e54-132">Valid values are:</span></span>

- <span data-ttu-id="63e54-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="63e54-133">None</span></span>
- <span data-ttu-id="63e54-134">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="63e54-134">ReadOnly</span></span>
- <span data-ttu-id="63e54-135">Yazma</span><span class="sxs-lookup"><span data-stu-id="63e54-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e54-136">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="63e54-136">-InformationAction</span></span>
<span data-ttu-id="63e54-137">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="63e54-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="63e54-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63e54-139">'A</span><span class="sxs-lookup"><span data-stu-id="63e54-139">Continue</span></span>
- <span data-ttu-id="63e54-140">Manıza</span><span class="sxs-lookup"><span data-stu-id="63e54-140">Ignore</span></span>
- <span data-ttu-id="63e54-141">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="63e54-141">Inquire</span></span>
- <span data-ttu-id="63e54-142">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="63e54-142">SilentlyContinue</span></span>
- <span data-ttu-id="63e54-143">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="63e54-143">Stop</span></span>
- <span data-ttu-id="63e54-144">Biliriz</span><span class="sxs-lookup"><span data-stu-id="63e54-144">Suspend</span></span>

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

### <span data-ttu-id="63e54-145">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="63e54-145">-InformationVariable</span></span>
<span data-ttu-id="63e54-146">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="63e54-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="63e54-147">-LUN</span></span>
<span data-ttu-id="63e54-148">Sanal makinedeki veri sürücüsünün LUN öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="63e54-149">Geçerli değerler: 0 ile 15 arası.</span><span class="sxs-lookup"><span data-stu-id="63e54-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e54-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="63e54-150">-Profile</span></span>
<span data-ttu-id="63e54-151">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63e54-152">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="63e54-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63e54-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="63e54-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="63e54-154">Veri diskinin yeni boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="63e54-155">Yeni boyut geçerli boyuttan büyük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="63e54-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e54-156">-VM</span><span class="sxs-lookup"><span data-stu-id="63e54-156">-VM</span></span>
<span data-ttu-id="63e54-157">Veri diskine eklenmiş olan sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63e54-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="63e54-158">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="63e54-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="63e54-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e54-159">CommonParameters</span></span>
<span data-ttu-id="63e54-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63e54-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e54-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e54-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e54-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63e54-162">INPUTS</span></span>

## <span data-ttu-id="63e54-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63e54-163">OUTPUTS</span></span>

## <span data-ttu-id="63e54-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63e54-164">NOTES</span></span>

## <span data-ttu-id="63e54-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63e54-165">RELATED LINKS</span></span>

[<span data-ttu-id="63e54-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="63e54-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="63e54-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="63e54-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="63e54-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="63e54-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="63e54-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="63e54-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="63e54-170">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="63e54-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


