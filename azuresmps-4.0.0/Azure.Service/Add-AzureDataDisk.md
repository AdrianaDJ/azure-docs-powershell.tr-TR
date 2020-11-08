---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105735"
---
# <span data-ttu-id="c3266-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3266-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="c3266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3266-102">SYNOPSIS</span></span>
<span data-ttu-id="c3266-103">Sanal makineye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="c3266-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="c3266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3266-104">SYNTAX</span></span>

### <span data-ttu-id="c3266-105">CreateNew (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3266-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c3266-106">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="c3266-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3266-107">Importfrom</span><span class="sxs-lookup"><span data-stu-id="c3266-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c3266-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3266-108">DESCRIPTION</span></span>
<span data-ttu-id="c3266-109">**Add-AzureDataDisk** cmdlet 'ı bir Azure sanal makine nesnesine yeni veya varolan bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="c3266-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="c3266-110">Belirtilen boyutta ve etikete sahip yeni bir veri disketi oluşturmak için *CreateNew* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3266-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="c3266-111">Görüntü deposundan var olan bir diski eklemek için *Içeri aktarma* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3266-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="c3266-112">Depolama hesabındaki bir blob 'dan var olan bir diski eklemek için *ımportfrom* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3266-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="c3266-113">Ekli veri diskinin ana bilgisayar önbelleği modunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3266-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="c3266-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3266-114">EXAMPLES</span></span>

### <span data-ttu-id="c3266-115">Örnek 1: depodan veri diski Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="c3266-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c3266-116">Bu komut, VirtualMachine07 adlı sanal makine için, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice bulut hizmetinde bir sanal makine nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="c3266-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c3266-117">Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3266-118">Bu komut, depodan varolan bir veri diskini sanal makineye iliştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="c3266-119">Veri diskinin LUN 'U 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="c3266-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="c3266-120">Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="c3266-121">Örnek 2: yeni veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="c3266-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c3266-122">Bu komut, VirtualMachine08 adındaki sanal makine için bir sanal makine nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="c3266-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="c3266-123">Komut bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="c3266-124">Bu komut, MyNewDisk. vhd adlı yeni bir veri diskine iliştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="c3266-125">Cmdlet, diski geçerli aboneliğin varsayılan depolama hesabında VHD kapsayıcısında oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3266-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="c3266-126">Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="c3266-127">Örnek 3: belirtilen konumdan veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="c3266-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="c3266-128">Bu komut, veritabanı adlı sanal makine için bir sanal makine nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="c3266-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="c3266-129">Komut bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="c3266-130">Bu komut, Disk14. vhd adlı varolan bir veri disketini belirtilen konumdan iliştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="c3266-131">Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3266-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="c3266-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3266-132">PARAMETERS</span></span>

### <span data-ttu-id="c3266-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="c3266-133">-CreateNew</span></span>
<span data-ttu-id="c3266-134">Bu cmdlet 'in veri disketi oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3266-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="c3266-135">-DiskLabel</span></span>
<span data-ttu-id="c3266-136">Yeni veri diskinin disk etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c3266-137">-DiskName</span></span>
<span data-ttu-id="c3266-138">Disk deposundaki bir veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c3266-139">-DiskSizeInGB</span></span>
<span data-ttu-id="c3266-140">Yeni bir veri diskinin mantıksal disk boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="c3266-141">-HostCaching</span></span>
<span data-ttu-id="c3266-142">Diskin ana bilgisayar düzeyi önbelleğe alma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="c3266-143">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c3266-143">Valid values are:</span></span> 

- <span data-ttu-id="c3266-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c3266-144">None</span></span> 
- <span data-ttu-id="c3266-145">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="c3266-145">ReadOnly</span></span> 
- <span data-ttu-id="c3266-146">Yazma</span><span class="sxs-lookup"><span data-stu-id="c3266-146">ReadWrite</span></span>

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

### <span data-ttu-id="c3266-147">-Import</span><span class="sxs-lookup"><span data-stu-id="c3266-147">-Import</span></span>
<span data-ttu-id="c3266-148">Bu cmdlet 'in görüntü deposundan var olan bir veri diskini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3266-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-149">-Importfrom</span><span class="sxs-lookup"><span data-stu-id="c3266-149">-ImportFrom</span></span>
<span data-ttu-id="c3266-150">Bu cmdlet 'in depolama hesabındaki bir blob 'dan var olan veri diskini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3266-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-151">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c3266-151">-InformationAction</span></span>
<span data-ttu-id="c3266-152">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c3266-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c3266-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3266-154">'A</span><span class="sxs-lookup"><span data-stu-id="c3266-154">Continue</span></span>
- <span data-ttu-id="c3266-155">Manıza</span><span class="sxs-lookup"><span data-stu-id="c3266-155">Ignore</span></span>
- <span data-ttu-id="c3266-156">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="c3266-156">Inquire</span></span>
- <span data-ttu-id="c3266-157">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="c3266-157">SilentlyContinue</span></span>
- <span data-ttu-id="c3266-158">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="c3266-158">Stop</span></span>
- <span data-ttu-id="c3266-159">Biliriz</span><span class="sxs-lookup"><span data-stu-id="c3266-159">Suspend</span></span>

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

### <span data-ttu-id="c3266-160">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="c3266-160">-InformationVariable</span></span>
<span data-ttu-id="c3266-161">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c3266-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="c3266-162">-LUN</span></span>
<span data-ttu-id="c3266-163">Sanal makinedeki veri sürücüsünün mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="c3266-164">Geçerli değerler: 0 ile 15 arası.</span><span class="sxs-lookup"><span data-stu-id="c3266-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="c3266-165">Her veri diskinin benzersiz bir LUN 'U olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3266-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="c3266-166">-MediaLocation</span></span>
<span data-ttu-id="c3266-167">Bu cmdlet 'in veri diskini sakladığı bir Azure depolama hesabında blob 'un konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="c3266-168">Konum belirtmezseniz cmdlet, veri diskini geçerli aboneliğin varsayılan depolama hesabında VHD kapsayıcısında depolar.</span><span class="sxs-lookup"><span data-stu-id="c3266-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="c3266-169">VHD kapsayıcısı yoksa, cmdlet bir VHD kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3266-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3266-170">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3266-170">-Profile</span></span>
<span data-ttu-id="c3266-171">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3266-172">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c3266-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3266-173">-VM</span><span class="sxs-lookup"><span data-stu-id="c3266-173">-VM</span></span>
<span data-ttu-id="c3266-174">Bu cmdlet 'in veri diskine ilişolduğu sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3266-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="c3266-175">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3266-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="c3266-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3266-176">CommonParameters</span></span>
<span data-ttu-id="c3266-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3266-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3266-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3266-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3266-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3266-179">INPUTS</span></span>

## <span data-ttu-id="c3266-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3266-180">OUTPUTS</span></span>

## <span data-ttu-id="c3266-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3266-181">NOTES</span></span>

## <span data-ttu-id="c3266-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3266-182">RELATED LINKS</span></span>

[<span data-ttu-id="c3266-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3266-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="c3266-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c3266-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c3266-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3266-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="c3266-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c3266-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="c3266-187">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c3266-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


