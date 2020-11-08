---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106013"
---
# <span data-ttu-id="d89a6-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-101">Update-AzureVM</span></span>

## <span data-ttu-id="d89a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d89a6-103">Azure sanal makinesinin yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="d89a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d89a6-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d89a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d89a6-105">DESCRIPTION</span></span>
<span data-ttu-id="d89a6-106">**Update-AzureVM** cmdlet 'i belirtilen sanal makinenin güncelleştirme bilgilerini kabul eder ve güncelleştirmeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d89a6-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="d89a6-107">Veri disklerini ekleyip kaldırabilir, verilerin veya işletim sistemi disklerinin önbellek modunu değiştirebilir, ağ uç noktalarını değiştirebilir veya sanal makinenin boyutunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d89a6-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="d89a6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d89a6-108">EXAMPLES</span></span>

### <span data-ttu-id="d89a6-109">Örnek 1: sanal makinenin boyutunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d89a6-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="d89a6-110">Bu komut, ContosoService03 adındaki hizmette çalışan VirtualMachine04 adındaki sanal makinenin boyutunu Orta olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="d89a6-111">Örnek 2: sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="d89a6-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="d89a6-112">Bu komut, ContosoService03 adındaki hizmette çalışan VirtualMachine05 adındaki sanal makineye yeni bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="d89a6-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="d89a6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d89a6-113">PARAMETERS</span></span>

### <span data-ttu-id="d89a6-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d89a6-114">-InformationAction</span></span>
<span data-ttu-id="d89a6-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d89a6-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d89a6-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d89a6-117">'A</span><span class="sxs-lookup"><span data-stu-id="d89a6-117">Continue</span></span>
- <span data-ttu-id="d89a6-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="d89a6-118">Ignore</span></span>
- <span data-ttu-id="d89a6-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d89a6-119">Inquire</span></span>
- <span data-ttu-id="d89a6-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d89a6-120">SilentlyContinue</span></span>
- <span data-ttu-id="d89a6-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d89a6-121">Stop</span></span>
- <span data-ttu-id="d89a6-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d89a6-122">Suspend</span></span>

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

### <span data-ttu-id="d89a6-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d89a6-123">-InformationVariable</span></span>
<span data-ttu-id="d89a6-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d89a6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d89a6-125">-Name</span></span>
<span data-ttu-id="d89a6-126">Güncelleştirilecek sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-126">Specifies the name of the virtual machine to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89a6-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="d89a6-127">-Profile</span></span>
<span data-ttu-id="d89a6-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d89a6-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d89a6-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d89a6-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d89a6-130">-ServiceName</span></span>
<span data-ttu-id="d89a6-131">Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-131">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89a6-132">-VM</span><span class="sxs-lookup"><span data-stu-id="d89a6-132">-VM</span></span>
<span data-ttu-id="d89a6-133">Güncelleştirilmiş ayarları içeren sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89a6-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d89a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89a6-134">CommonParameters</span></span>
<span data-ttu-id="d89a6-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d89a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89a6-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89a6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89a6-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d89a6-137">INPUTS</span></span>

## <span data-ttu-id="d89a6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d89a6-138">OUTPUTS</span></span>

## <span data-ttu-id="d89a6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d89a6-139">NOTES</span></span>

## <span data-ttu-id="d89a6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d89a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="d89a6-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d89a6-142">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="d89a6-143">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="d89a6-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="d89a6-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="d89a6-145">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="d89a6-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="d89a6-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="d89a6-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="d89a6-148">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d89a6-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


