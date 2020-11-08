---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105828"
---
# <span data-ttu-id="dd201-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="dd201-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="dd201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd201-102">SYNOPSIS</span></span>
<span data-ttu-id="dd201-103">Azure sanal makinesinin ana bilgisayar önbelleği modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dd201-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="dd201-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd201-104">SYNTAX</span></span>

### <span data-ttu-id="dd201-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="dd201-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="dd201-106">Yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="dd201-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd201-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd201-107">DESCRIPTION</span></span>
<span data-ttu-id="dd201-108">**Set-AzureOSDisk** cmdlet 'i Azure sanal makinesindeki işletim sistemi diskinin ana bilgisayar önbelleği modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dd201-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="dd201-109">Desteklenen ana bilgisayar önbelleği modları ReadOnly ve ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="dd201-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="dd201-110">Bu cmdlet 'i çalışan bir sanal makinede çalıştırırsanız, bu sanal makine yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="dd201-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="dd201-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd201-111">EXAMPLES</span></span>

### <span data-ttu-id="dd201-112">Örnek 1: ardışık düzeni kullanarak ana bilgisayar önbellek modunu ReadOnly olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="dd201-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="dd201-113">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine02 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="dd201-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="dd201-114">Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="dd201-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dd201-115">Geçerli cmdlet, bu sanal makinenin işletim sistemi diskinin ana bilgisayar önbelleği modunu ReadOnly olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dd201-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="dd201-116">Örnek 2: Ana bilgisayar önbellek modunu ReadWrite olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="dd201-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="dd201-117">İlk komut, VirtualMachine02 adındaki sanal makineyi ContosoService adındaki hizmette alır ve değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="dd201-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="dd201-118">İkinci komut, bu sanal makinenin işletim sistemi diskinin ana bilgisayar önbelleği modunu ReadWrite olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dd201-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="dd201-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd201-119">PARAMETERS</span></span>

### <span data-ttu-id="dd201-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="dd201-120">-HostCaching</span></span>
<span data-ttu-id="dd201-121">İşletim sistemi diskinin ana bilgisayar önbelleği özniteliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="dd201-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="dd201-122">Valid values are:</span></span> 

- <span data-ttu-id="dd201-123">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="dd201-123">ReadOnly</span></span> 
- <span data-ttu-id="dd201-124">Yazma</span><span class="sxs-lookup"><span data-stu-id="dd201-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd201-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="dd201-125">-InformationAction</span></span>
<span data-ttu-id="dd201-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dd201-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dd201-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dd201-128">'A</span><span class="sxs-lookup"><span data-stu-id="dd201-128">Continue</span></span>
- <span data-ttu-id="dd201-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="dd201-129">Ignore</span></span>
- <span data-ttu-id="dd201-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="dd201-130">Inquire</span></span>
- <span data-ttu-id="dd201-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="dd201-131">SilentlyContinue</span></span>
- <span data-ttu-id="dd201-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="dd201-132">Stop</span></span>
- <span data-ttu-id="dd201-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="dd201-133">Suspend</span></span>

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

### <span data-ttu-id="dd201-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="dd201-134">-InformationVariable</span></span>
<span data-ttu-id="dd201-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dd201-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="dd201-136">-Profile</span></span>
<span data-ttu-id="dd201-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd201-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="dd201-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd201-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dd201-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="dd201-140">İşletim sistemi diski için, gigabayt cinsinden yeni bir boyut belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="dd201-141">Boyut geçerli boyuttan büyük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd201-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd201-142">-VM</span><span class="sxs-lookup"><span data-stu-id="dd201-142">-VM</span></span>
<span data-ttu-id="dd201-143">Bu cmdlet 'in işletim sistemi diskini değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd201-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="dd201-144">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd201-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="dd201-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd201-145">CommonParameters</span></span>
<span data-ttu-id="dd201-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd201-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd201-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd201-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd201-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd201-148">INPUTS</span></span>

## <span data-ttu-id="dd201-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd201-149">OUTPUTS</span></span>

## <span data-ttu-id="dd201-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd201-150">NOTES</span></span>

## <span data-ttu-id="dd201-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd201-151">RELATED LINKS</span></span>

[<span data-ttu-id="dd201-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dd201-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="dd201-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="dd201-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="dd201-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dd201-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="dd201-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="dd201-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="dd201-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="dd201-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="dd201-157">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dd201-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


